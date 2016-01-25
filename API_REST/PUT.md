# References PUT
## [Compte] PUT: /account/create/[string:username]/[string:password]/[string:email]
### Création d'un compte réussit
```
	{
		"status": 204
	}
```
* **[integer:`status`]**: code 204.

### Informations déjà utilisé ou informations erronées
```
    {
        "error_validate": false,
        "error_indice": 1,
        "status": 403
    }
```
* **[boolean:`error_validate`]**: indique si l'erreur concerne la validation des données ou une donnée déjà présente dans la base de donnée:
    * `true`: l'erreur concerne la validation des données;
    * `false`: certaines données sont déjà présentes dans la base de donnée.
* **[integer:`error_indice`]**: indique quel champs contient des données invalides ou déjà dans la base de donnée :
    * **1**: username;
    * **2**: password (s'applique uniquement si `error_validate` == `true`;
    * **3**: email.
* **[integer:`status`]**: code 600 si `error_validate` == `false` & code 601 si `error_validate` == `true`.

## [Compte] PUT: /account/group/create/[string:name]/[integer:parent_id]
### Création 'un groupe réussit
```
    {
        "status": 204
    }
```
* **[integer:`status`]**: code 204.

### Groupe déjà existant
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

### La requête contient des données mal formaté
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

## [Account] PUT: /account/token/renew/[string:token]
### Renouvellement du token réussit
```
    {
        "token": "0123456789ABCDEF",
        "ttl": 3600,
        "status": 200
    }
```
* **[string:`token`]**: contient le token à renvoyer à chaques demande d'information;
* **[integer:`ttl`]**: durée de validité du token en secondes;
* **[integer:`status`]**: code 200.

### Token soumis non valide
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

## [Exercice] PUT [JSON RAW]: /exercise/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "course_id": 1,
        "title": "titre",
        "instruction": "instructions pour réaliser l'exercice",
        "grade_max": 10,
        "script_id": 1,
        "correction_id": 1
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`course_id`]**: l'id du cour;
* **[string:`title`]**: le titre de l'exercice;
* **[string:`instruction`]**: les instruction à suivre pour réaliser l'exercice;
* **[integer:`grade_max`]**: le grade max qu'on peux avoir en réalisant l'exercice;
* **[integer:`script_id`]**: l'id du script de correction;
* **[integer:`correction_id`]**: l'exercice corrigé.

### Création d'exercice réussit
```
    {
        "status": 204
    }
```
* **[integer:`status`]**: code 204.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Exercice déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT [JSON RAW]: /exercise/correction/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "content": "Texte de correction"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`content`]**: contient le texte de correction.

### Création d'une correction réussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: contient l'id de la correction réssament enregistrée dans la base de donnée;
* **[integer:`status`]**: code 200.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Correction déjà présente dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT [JSON RAW]: /exercise/script/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "content": "Contient le script de correction"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`content`]**: contient le script de correction.

### Création d'un script de correction réussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: contient l'id d'u script réssament enregistrée dans la base de donnée;
* **[integer:`status`]**: code 200.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Script déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT [JSON RAW]: /exercise/script/log/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "content": "Traces d'éxécution",
        "script_id": 1
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`content`]**: contient les informations d'éxécution de la correction";
* **[integer:`script_id`]**: contient l'id d'un script.

### Création d'un rapport rattaché à un script réussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: contient l'id du rapport créé.
* **[integer:`status`]**: code 200.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Rapport déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT  [JSON RAW]: /exercise/grade/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "exercice_id": 1,
        "value": 10,
        "log_id": 1
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`exercice_id`]**: contient l'id de l'exercice;
* **[integer:`value`]**: contient la valeur du grade;
* **[integer:`log_id`]**: contient l'id du rapport.

### Création d'un grade réussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: contient l'id du grade ajouté;
* **[integer:`status`]**: code 200.

### La valeur du grade a dépassée la valeur max
```
    {
        "status": 604
    }
```
* **[integer:`status`]**: code 604.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Grade déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT [JSON RAW]: /exercise/user/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "exercice_id": 1,
        "grade_id": 1
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`exercice_id`]**: l'id de l'exercice;
* **[integer:`grade_id`]**: l'id du grade;

### Création d'exercice réalisé par l'utilisateur réussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: l'id de l'exercice,
* **[integer:`status`]**: code 200.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Exercice réalisé par l'utilisateur déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT [JSON RAW]: /exercise/user/code/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "user_exercice_id": 1,
        "content": "code rédigé..."
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`user_exercice_id`]**: l'id de l'exercice réalisé par l'utilisateur,
* **[string:`content`]**: code rédigé par l'utilisateur.

### Création de code réussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: l'id de l'enregistrement;
* **[integer:`status`]**: code 200.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Code déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT  [JSON RAW]: /exercise/comment/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "exercice_id": 1,
        "content": "commentaire"
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`exercice_id`]**: l'id de l'exercice;
* **[string:`content`]**: contenue du commentaire.

### Création de commentaire sur exercice réussit
```
    {
        "status": 204
    }
```
* **[integer:`status`]**: code 204.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Commentaire sur exercice déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Cour] PUT [JSON RAW]: /course/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "local_id": 1,
        "language_id": 1,
        "title": "titre",
        "content": "contenue"
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`local_id`]**: l'id de la langue;
* **[integer:`language_id`]**: l'id de la langue de programmation;
* **[string:`title`]**: intitulé du cour;
* **[string:`content`]**: contenue du cour.

### Création d'un cour réussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: l'id du cour rédigé;
* **[integer:`status`]**: code 200.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Cour déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Cour] PUT  [JSON RAW]: /course/language/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "name": "C++"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`name`]**: contient le language de programmation.

### Création d'un langage pour un cour réussit
```
    {
        "status": 204
    }
```
* **[integer:`status`]**: code 204.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Langage déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Cour] PUT [JSON RAW]: /course/commente/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "course_id": 1,
        "content": "contenu"
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`course_id`]**: l'id du cour;
* **[string:`content`]**: contenu du commentaire.

### Création d'un commentaire pour un cour réussit
```
    {
        "status": 204
    }
```
* **[integer:`status`]**: code 204.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Commentaire de cour déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Blog] PUT [JSON RAW]: /blog/post/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "local_id": 1,
        "blog_category_id": 1,
        "title": "string contenue",
        "content": "contenue"
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`local_id`]**: l'id de la langue;
* **[integer:`blog_category_id`]**: l'id de la categorie du blog;
* **[string:`title`]**: titre du post;
* **[string:`content`]**: contenue du post.

### Création d'un post réussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: l'id du post créé;
* **[integer:`status`]**: code 204.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Post déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Blog] PUT [JSON RAW]: /blog/post/category/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "name": "categorie"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`name`]**: nom de la catégorie.

### Création d'une catégorie réussit
```
    {
        "status": 204
    }
```
* **[integer:`status`]**: code 204.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Catégorie déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Blog] PUT [JSON RAW]: /blog/post/comment/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "blog_post_id": 1,
        "content": "contenue"
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`blog_post_id`]**: l'id du post;
* **[string:`content`]**: contenue du commentaire.

### Création d'un commentaire en réponse à un post réussit
```
    {
        "status": 204
    }
```
* **[integer:`status`]**: code 204.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Commentaire déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Forum] PUT [JSON RAW]: /forum/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "forum_category_id": 1,
        "name": "",
        "description": ""
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`forum_category_id`]**: l'id de la category;
* **[string:`name`]**: nom de la categorie;
* **[string:`description`]**: description de la categorie.

### Création d'un forum de discussion réussit
```
    {
        "status": 204
    }
```
* **[integer:`status`]**: code 204.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Forum de discussion déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Forum] PUT [JSON RAW]: /forum/categorie/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "name": ""
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`name`]**: nom de la categorie.

### Création d'une categorie de forum réussit
```
    {
        "status": 204
    }
```
* **[integer:`status`]**: code 204.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Catégorie de forum déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Forum] PUT [JSON RAW]: /forum/post/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "forum_subject_id": 1,
        "content": ""
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`forum_subject_id`]**: l'id du sujet du forum;
* **[string:`content`]**: contenue du post.

### Création d'un post de forum réussit
```
    {
        "status": 204
    }
```
* **[integer:`status`]**: code 204.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Post de forum déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Forum] PUT [JSON RAW]: /forum/subject/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "forum_forum_id": 1,
        "locales_id": 1
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`forum_forum_id`]**: l'id du forum de discussion;
* **[integer:`locales_id`]**: l'id de la langue.

### Création d'un sujet de discussion réussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: l'id du sujet créé;
* **[integer:`status`]**: code 204.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Sujet de discussion déjà présent dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Autre] PUT [JSON RAW]: /other/locale/create
### Paramètres à envoyer
```
    {
        "token": "0123456789ABCDEF",
        "name": "FR"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`name`]**: nom de la langue.

### Création de langue réussit
```
    {
        "status": 204
    }
```
* **[integer:`status`]**: code 204.

### Informations manquantes
```
    {
        "status": 603
    }
```
* **[integer:`status`]**: code 603.

### Informations invalides
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

### Informations mal formatés
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Langue déjà présente dans la base de donnée
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.