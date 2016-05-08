	Cette partie contient une description technique du serveur de communication. Elle y décrit le but du serveur, ainsi que son fonctionnement et le protocole utilisé pour la communication avec les autres éléments.

Le serveur de communication est un service composé d’un client (Utilisant la librairie Kryonet), d’un serveur WebSocket (Utilisant la librairie JavaWebSock) et un service d’API permettant de gérer des containers et serveurs Docker.

Ce service est découpé en 5 grandes parties:

* Le Client Kryonet: Celui-ci permet de s’identifier au backend, et s’y connecter pour permettre de recevoir les demandes de compilations en temps réel.

* Le Serveur WebSocket: Celui-ci permet d’identifier différents clients, et leur envoie les avancements en temps réel des différents containers sur lesquels les clients sont liés.

* Le Docker Manager: Celui-ci permet de gérer les différents conteneurs dockers, ainsi que la file d’attente affin d’accéder aux ressources.

* Un DAO: Celui-ci permet d’accéder aux données de la base de données, ainsi que de les modifier.

* Et enfin, d’un système de services, qui permet de gérer, de manière asynchrone plusieurs actions.

**A - Le client Kryonet**

Le client Kryonet est composé d’une classe Client, ainsi qu’une classe Interpretator, et plusieurs "actionneurs".

Elle a pour but de recevoir les demandes de compilations de la part du Backend et de les transférer au Docker Manager.

Le protocole est composé de deux commandes distinctes:

* Handshake: Ce packet est envoyé de la part du serveur de communication au Backend, et a pour but d’identifier le service. Le packet est un packet en JSON, et est sous la forme suivante: {"cmd":"HANDSHAKE","TOKEN":"SERVER_TOKEN"}. Le SERVER_TOKEN représente le token de connexion, permettant au Backend d’identifier le service, et lui permettre de se connecter.

* ExercisePacket: Ce packet est envoyé de la part du Backend vers le serveur de communication pour lui donner l’ordre d’exécuter un exercice. Celui-ci prend la forme suivante: {"cmd":"EXERCISE","id":"ID_EXERCICE"}. ID_EXERCICE représente l’identifiant, dans la base de données, de l’exercice. Il sera ensuite transféré au service d’exécution des exercices.

**B - Le serveur WebSocket**

Le serveur WebSocket  est comosé de la classe Server, ainsi qu’une classe Interpretator, et plusieurs "actionneurs".

Elle a pour but de prévenir les utilisateurs lors de la mise à jour de leur place dans la file d’attente, de la fin de correction d’un de leurs exercices, ou encore d’une notification exterieure (erreur lors de la compilation de l’exercice, etc…).

Le protocole est composé des commandes suivantes:

* AuthPacket: Ce packet est à destination du serveur de communication et permet d’identifier le client. Celui-ci prend la forme suivante: {"cmd":"AUTH","TOKEN":"TOKEN_UTILISATEUR"}TOKEN_UTILISATEUR représente le token généré par le Backend, et permet d’identifier le client.

* ExerciceExecutedPacket: Ce packet est à destination des clients, et permet de prévenir un utilisateur que son exercice a été exécuté et corrigé. Il prend la forme suivante:{"cmd":"EXERCICE_EXECUTED","id":"EXERCICE_ID"}EXERCICE_ID représente l’identifiant de l’exercice dans la base de données.

* PlaceInQueuePacket: Ce packet est à destination des clients, et permet au client de connaître sa place dans la file d’attente, si il y en a une. Il prend la forme suivante: {"cmd":"PLACE_IN_QUEUE","user_exercice_id":"EXERCICE_ID","place":"PLACE"}EXERCICE_ID représente l’ID de l’exercice, PLACE, la place actuelle de l’utilisateur dans la file d’attente.

* OkPacket: Ce packet est à destination des clients, et leur permet de savoir si la commande a bien été comprise et exécutée par le serveur. Il est systématiquement envoyé à chaque commande utilisateur si elle est exécutée correctement. Il prend la forme suivante:{"cmd":"OK"}

* ErrorPacket: Ce packet est à destination des clients, et permet de les prévenir en cas d’erreur. Il prend la forme suivante: {"cmd":"ERROR","error_code":"ERROR_CODE","target":"TARGET","target_id":"TARGET_ID"}ERROR_CODE représente le code d’erreur, TARGET représente la cible de l’erreur (EXERCICE, CONTAINER, OTHER), TARGET_ID représente l’ID (si il y en a une) de la TARGET.

**Codes erreurs:**

<table>
  <tr>
    <td>Errors</td>
    <td>Error ID</td>
    <td>Target</td>
    <td>TargetID</td>
  </tr>
  <tr>
    <td>AuthenticationError</td>
    <td>401</td>
    <td>OTHER</td>
    <td>N/A</td>
  </tr>
  <tr>
    <td>ExecutionError</td>
    <td>500</td>
    <td>CONTAINER/EXERCISE</td>
    <td>user_exercise_id or container_id</td>
  </tr>
  <tr>
    <td>InternalError</td>
    <td>500</td>
    <td>OTHER</td>
    <td>N/A</td>
  </tr>
  <tr>
    <td>NotFoundError</td>
    <td>404</td>
    <td>CONTAINER/EXERCISE</td>
    <td>user_exercise_id or container_id</td>
  </tr>
  <tr>
    <td>UnauthorizedError</td>
    <td>403</td>
    <td>CONTAINER/EXERCISE</td>
    <td>user_exercise_id or container_id</td>
  </tr>
</table>


**C - Le Docker Manager**

Le Docker manager est composé de trois classes distinctes: DockerManager, Container, DockerWrapper.

La classe DockerManager est un service (voir plus bas) et permet de gérer de manière asynchrone la disponibilité des conteneurs Docker. Elle régie la file d’attente, et les réponses aux utilisateurs lors d’une fin d’exécution.

La classe Container représente un container Docker, ainsi que toutes les actions concernant ce container.

La classe DockerWrapper permet d’englober plusieurs fonctions permettant la maîtrise d’un serveur Docker, ainsi que la gestion de ses Containers.

Le DockerManager reçoit des exercices à exécuter, et envoie une alerte au client souhaité lorsque l’exercice a été exécuté avec succès. Il met aussi à jour la place de l’utilisateur dans la liste d’attente et gère les connexions/reconnexions aux services Docker.

**D - Le DAO**

Le DAO est composé de plusieurs classes: Le DaoManager, le DatabaseManager et les classes de DAO (qui héritent de la classe DAO).

Le DaoManager est la classe qui gère les connexions des différents DAO à la base de données. Il est basé sur le design pattern Factory, et permet d’éviter la création de multiple DAO pour la même table. Il permet l’accès aux DAOs de manière simple.

Le DatabaseManager permet de gérer la connexion à la base de données, et gère la Pool de connexion à la base de données -qui utilise DBCP2-, il permet de se connecter et fournir les connecteurs aux différentes DAO.

Les DAOs permettent de gérer les données qui transitent entre la base de données et le service. Elles permettent d’interagir avec la base de données. Chaque DAO représente une ressource (table) de la base de données.

**E - Les services**

Les services permettent d’exécuter des tâches de manière Asynchrone. Il existe trois services principaux sur notre projet: AuthService, ExecService, DockerManager.

Le AuthService permet de gérer les demandes de connexion au serveur de communication. Il vérifie que l’utilisateur est correctement authentifié et donne accès aux autres options du serveur de communication.

Le ExecService permet d’exécuter les ordres d’exécution d’exercices en récupérant les données d’un exercice via les DAOs et en préparant la requête pour le DockerManager, puis envoie cette requête au DockerManager.

Le DockerManager est le service permettant de gérer les services Docker. Il reçoit des requêtes d’exécution de la part du ExecService, et exécute les requêtes en fonction des différents containers Docker à sa disposition.

