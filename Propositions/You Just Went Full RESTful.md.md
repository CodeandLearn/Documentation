[TOC]

# Introduction

Après avoir utilisé l'API pour les exercices il est nécessaire de repasser sur de nombreux aspects de la partie exercices et utilisateur pour la rendre fonctionnelle et agréable à utiliser avec le frontend.

Je proposerais ci-dessous des changements qui vont améliorer l'expérience utilisateur et le développement du frontend et des applications mobiles.

Dans les objets JSON je ne couvrirais que la partie `data` afin de ne pas être redondant. Certains objets comme l'objets `account` seront abrégé car ils existent déjà sous la forme désiré sur d'autres parties.

Cette documentation est basé sur la révision [b2f1d205](https://gitlab.com/CodeandLearn/Doc/tree/b2f1d205cda7479d1c8ea75c66e6e02ef211c71f/API_REST).

# Priorités

La liste ci dessous est ordonnée de l'élément le plus important vers l'élément le moins important.

1. Exercices (sauf commentaires);
2. User exercices (sauf commentaires);
3. Cours;
3. Account;
4. Forums;
5. Commentaires si vraiment nécessaire pour les exercices.

# Glossaire

* **Programme model**: C'est le programme sur lequelle la correction se basera pour définir si l'exercice a été correctement réalisé ou pas par l'utilisateur.
* **Réaliser**: Lorsqu'un utilisateur *réalise* un exercice on peut dire que c'est un simple utilisateur qui souhaite tester ses connaissances et être noté.

# Erreurs communes

Les erreurs communes se limitent souvent à l'utilisation de plusieurs langues pour le mot `exercices` lorsque `exercise` est attendu.

Les titres des sections pour les routes ne précisent pas la méthode et nécessite de scroller sur la documentation pour être certain d'être dans la bonne section, c'est un détail sur l'ergonomie de la documentation non négligeable mais pas non plus prioritaire.

# Rappel de l'architecture

Le site web est composé d'une partie qui sert d'interface graphique (frontend et mobile) et d'une partie de traitement des données (backend et servcomm). Le backend en réalité fait le plus gros du travail pour renvoyer les données et permettre l'exploitation de ces dernières pour un minimum d'effort afin de fournir les performances qui n'auront pas d'incidence sur l'expérience utilisateur.

Fournir un maximum de données aux interfaces permet de réduire le nombre de requête et la complexité du code ([voir ce controller](https://gitlab.com/CodeandLearn/Webapp/blob/3044489b18caa4b66593188b10d6a24dbeaf451f/app/js/exercise/controllers.js));

# `GET /exercises` --DONE

Cette route est actuellement utilisé pour lister tout les exercices avec ou sans modération. Il est nécessaire d'y apporter les informations de modération afin de pouvoir les classer correctement.

	[
		{
			"id:" 1,
			"course": {
				"id": 1,
				"name": "Getting started with C",
				"language": {
					"id": "1",
					"name": "C"
				}
			},
			"account": {
				...
			},
			"title": "Write a HelloWorld app",
			"instructions": "You are tasked to write a HelloWorld app that will print HelloWorld followed by a new line.",
			"mod": {
				"published": false,
				"message": "This exercise was not moderated yet"
			},
			"date": {
				"edited": 1234567890,
				"created": 1234567890
			},
			"grade": 1
		}
	]

La récupération de la `date` permet de classer les exercices par date mais ce n'est pas un champ très important et peut donc être ignoré dans conséquences.  
L'objet `mod` défini un status de modération où une `boolean` représente l'état de publication accompagné du message du modérateur.

Dans le cas ou aucun exercices n'est retourné il est souhaitable d'afficher un status `200` et de fournir une liste vide pour indiquer qu'aucun cours n'existe.

# `GET /exercise/{id}` --DONE


Lorsqu'un utilisateur récupére un exercice depuis son `id` on peut considérer que l'utilisateur cherche à le réaliser et il est donc nécessaire de fournir les fichiers par défaut ou de charger les fichier qui ont été écrit par l'utilisateur authentifié.

	{
		"id:" 1,
		"course": {
			"id": 1,
			"name": "Getting started with C",
			"language": {
				"id": "1",
				"name": "C"
			}
		},
		"account": {
			...
		},
		"title": "Write a HelloWorld app",
		"instructions": "You are tasked to write a HelloWorld app that will print HelloWorld followed by a new line.",
		"code": [
			{"name": "main.c", "content": "#include <stdio.h>\n\nint main() {\n\tprintf("\n");\nreturn (0);\n}"}
		],
		"mod": {
			"published": false,
			"message": "This exercise was not moderated yet"
		},
		"date": {
			"edited": 1234567890,
			"created": 1234567890
		},
		"grade": 1
	}

L'objet `code` doit forcément renseigner au moins:

* `name`: représentation du nom du fichier;
* `content`: représentation du contenu du fichier.

L'éditeur du frontend supporte deux options supplémentaire pour définir l'utilisation du fichier:

* `Boolean readonly`: défini si l'utilisateur est en droit de modifier le fichier;
* `Boolean cloasable`: défini si l'utilisateur peut fermer le fichier, et donc le supprimer de son environnement de travail.

La variable `grade` pourrait être représenté sous forme d'objet pour contenir la note maximum pouvant être attribué et la note que l'utilisateur a reçu lors d'un exécution précédente/

	{ "max": 10, "grade": 5 }

La répétition de `grade` n'est peut être pas idéal et pourra être remplacé par un autre nom au besoin.

Le backend doit dont être la partie à décider si il faut charger les fichiers précédent ou en créer de nouveaux afin de ne pas faire tester l'existence de fichiers précédent au frontend.

# `GET /exercise/{id}/script` --Hidden, script should be used by server-comm to evaluate the exercise

Je propose de renommer cette route en `GET /exercise/{id}/edit` pour mettre l'accent sur l'action désiré par cette route. L'objet renvoyé par cette route est le même que pour `GET /exercise/{id}` avec pour seule différence l'objet `code`.

L'objet `code` est une liste composé au moins de:

* `check.sh`: le script de correction;
* Les fichiers qui permettent de composer un *programme modèle*.

		{
			"id:" 1,
			"course": {
				"id": 1,
				"name": "Getting started with C",
				"language": {
					"id": "1",
					"name": "C"
				}
			},
			"account": {
				...
			},
			"title": "Write a HelloWorld app",
			"instructions": "You are tasked to write a HelloWorld app that will print HelloWorld followed by a new line.",
			"code": [
				{"name": "check.sh", "content": "#!/bin/sh\n\ngcc helloworld.c -o model\ngcc main.c -o a.out\ndiff <(./model) <(./a.out)\nexit $?"},
				{"name": "helloworld.c", "content": "#include <stdio.h>\n\nint main() {\n\tprintf("HelloWorld\n");\nreturn (0);\n}"}
			],
			"mod": {
				"published": false,
				"message": "This exercise was not moderated yet"
			},
			"date": {
				"edited": 1234567890,
				"created": 1234567890
			},
			"grade": 1
		}


# `GET /exercise/{id}/moderation` --Untouched

Cette route devient obsolète avec l'inclusion des informations de modérations sur les exercices eux même.

# `POST /exercise` --Untouched

Afin de faciliter la création d'exercices il serait intéressant de permettre l'initialisation de la création de l'exercice en fournissant l'objet suivant:

	{
		"course_id": 1,
		"title": "New exercise",
		"instruction": "Sample instruction.",
		"code": [
			{"name": "check.sh", "content": "#!/bin/sh\n\nexit $?"}
		]
		"grade": 10
	}

Dans ce cas la nous initialisons le script de correction avec l'exercice en une seule requête HTTP. Cette inclusion rend obsolète la route `GET /exercise/script`.

La variable `grade` n'est peut être pas très importante car nous pouvons aussi nous contenter de vérifier si l'exercice est résolu ou bien si l'utilisateur à échouer afin de constituer des conditions de réussite indépendante d'une note numérique. --il s'agit ici de la note maximale obtensible

Le `course_id` est bien sûr toujours nécessaire pour préciser à quel cours cet exercice est rattaché. Il n'est pas nécessaire cependant d'y rattacher un compte utilisateur à l'aide de la variable `account_id` ([voir documentation](https://gitlab.com/CodeandLearn/Doc/blob/b2f1d205cda7479d1c8ea75c66e6e02ef211c71f/API_REST/Exercices.md#exercise)).

# `POST /exercise/moderation` --Hidden

Cette route devient obsolète avec la création d'une entrée dans la table de modération lors de la création d'un exercice.

# `PUT /exercise/{id}` --DONE

La variable `course_id` n'est plus nécessaire car l'exercice est déjà associé à un cours.

	{
		"title": "New exercise",
		"instruction": "Sample instruction.",
		"code": [
			{"name": "check.sh", "content": "#!/bin/sh\n\nexit $?"}
		]
		"grade": 10
	}

La liste `code` peut ainsi être étendu et rétrécit au besoin pour le *programme model*. En cas d'ajoute ou de suppression il sera nécessaire d'effectuer les opérations nécessaire du coté du backend pour supprimer les fichiers non utilisé ou en ajouter d'autres.  
Cette dernière peut être facilité à l'aide d'un système de versionning permettant de créer une nouvelle entrée et de cacher l'entrée précédente lorsqu'une plus récente est publié et approuvé.

# `DELETE /exercise/{id}`

Cette route devrait se charger de supprimer le script de correction et le code du *programme model* en plus de supprimer l'entrée dans la base de données pour l'exercice. Cette entrée doit donc avoir un effet de cascade sur:

* Les scripts;
* Les corrections;
* La modération.


# `/exercise/correction` --La route sers si l'utilisateur est justement incapable de resoudre l'exercice

Cette route ne devrait pas être accessible depuis le frontend afin de ne pas permettre à un utilisateur de gruger dans les résultats de ses exercices.

# `/exercise/comment` 

Il n'est pas encore prévue pour le frontend de permettre à un utilisateur de poster des commentaires sur les exercices. Il serait préférable de faire ça depuis le forum et d'ignorer ces routes pour une plus grande simplicité.

Dans le cas où cette route doit être utilisé, elle nécessite un ajout d'un objet `account` pour décrire l'utilisateur.

# `GET /user_exercices`

Cette route devrait retourner une liste d'exercices complète avec les champs exercices cité dans la section `GET /exercise/{id}`.

# `POST /user_exercise/{id}`

Pour permettre à l'utilisateur de soumettre son code pour résoudre un exercice, il serait plus facile et interessant de soumettre tout le code sous la forme de l'objet suivant:

	{
		"code": [
			{"name": "putchar.c", "content": "void putchar(char c) {\n\nwrite(1, &c, 1);\n}"},
			{"name": "putchar.h", "#pragma once\n\nvoid putchar(char c);"}
		]
	}

La list `code` prendra une liste de taille variable.

Les variable `account_id` et `exercice_id` doivent être définie respectivement à l'aide du header d'authorisation et de la route employée contrairement à ce qui [est documenté](https://gitlab.com/CodeandLearn/Doc/blob/b2f1d205cda7479d1c8ea75c66e6e02ef211c71f/API_REST/User_Exercice.md#succ%C3%A8s-type).

# `PUT /user_exercise/{id}`

Cette route est inutile à partir du moment où l'on souhaite garder un historique des compilations de l'utilisateur. Cet historique peut permettra à l'utilisateur de contrôler l'évolution de son code.

# `GET /account/{id}`

Il est impératif de cacher l'adresse email lorsqu'un utilisateur lance une requête pour récupérer l'adresse email d'un autre utilisateur. Ce changement vise tout les objets JSON qui serait susceptible de fournir les adresses email des membres à n'importe qui pouvant regarder les requêtes.  
Ceci fait partie de la protections des données personnels des utilisateurs.

# `PUT /account`

Afin d'éditer le profil il est nécessaire d'envisager l'utilisation de cette route dans plusieurs cas.

Cas N°1: l'utilisateur souhaite modifier:

* Son nom d'utilisateur;
* Son adresse email;
* Son avatar;
* Mais pas son mot de passe.

Il est nécessaire de pouvoir envoyer un objet JSON dont le champ mot de passe est vide, l'API prendra en compte le champ vide et ne changera pas le mot de passe.

Cas N°2: l'utilisateur souhaite modifier son mot de passe, dans ce cas l'utilisateur remplis le formulaire pour fournir un nouveau mot de passe et l'API se chargera de le prendre en compte.

L'objet JSON idéal concernant ces informations se représenterais de la façon suivante:

	{
		"username": "hirsch_b",
		"password": "",
		"email": "hirsch_b@epitech.eu",
		"avatar": "//www.gravatar.com/avatar/HASH"
	}

Cette requête ne changera donc pas le mot de passe utilisateur.

Le champ `group_id` est facultatif et ne sera prit en compte que si la requête émanne d'un `Administrateur`.

Pour l'utilisation d'un Gravatar il est nécessaire que le backend calcule la somme MD5 sur l'adresse email de l'utilisateur pour former le lien. Il est préférable d'utiliser une URL commençant par `//` au lieu de `http://` au cas où on servirait en `HTTPS`.

# Cours

Ce document ne couvre pas les cours car il n'existe pas de documentation sur le sujet. Si les remarques ci-dessus sont prisent en compte tout se passera pour le mieux.

# Forum

Pour le forum il sera nécessaire d'étudier les améliorations proposé ici pour ne pas le surcharger en éléments inutile et factoriser au maximum les opérations.