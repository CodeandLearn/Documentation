# References PUT
## [Compte] PUT: /account/create/[string:username]/[string:password]/[string:email]
### Cr�ation d'un compte r�ussit
```
	{
		"status": 204
	}
```
* **[integer:`status`]**: code 204.

### Informations d�j� utilis� ou informations erron�es
```
    {
        "error_validate": false,
        "error_indice": 1,
        "status": 403
    }
```
* **[boolean:`error_validate`]**: indique si l'erreur concerne la validation des donn�es ou une donn�e d�j� pr�sente dans la base de donn�e:
    * `true`: l'erreur concerne la validation des donn�es;
    * `false`: certaines donn�es sont d�j� pr�sentes dans la base de donn�e.
* **[integer:`error_indice`]**: indique quel champs contient des donn�es invalides ou d�j� dans la base de donn�e :
    * **1**: username;
    * **2**: password (s'applique uniquement si `error_validate` == `true`;
    * **3**: email.
* **[integer:`status`]**: code 600 si `error_validate` == `false` & code 601 si `error_validate` == `true`.

## [Compte] PUT: /account/group/create/[string:name]/[integer:parent_id]
### Cr�ation 'un groupe r�ussit
```
    {
        "status": 204
    }
```
* **[integer:`status`]**: code 204.

### Groupe d�j� existant
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

### La requ�te contient des donn�es mal format�
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

## [Account] PUT: /account/token/renew/[string:token]
### Renouvellement du token r�ussit
```
    {
        "token": "0123456789ABCDEF",
        "ttl": 3600,
        "status": 200
    }
```
* **[string:`token`]**: contient le token � renvoyer � chaques demande d'information;
* **[integer:`ttl`]**: dur�e de validit� du token en secondes;
* **[integer:`status`]**: code 200.

### Token soumis non valide
```
    {
        "status": 602
    }
```
* **[integer:`status`]**: code 602.

## [Exercice] PUT [JSON RAW]: /exercise/create
### Param�tres � envoyer
```
    {
        "token": "0123456789ABCDEF",
        "course_id": 1,
        "title": "titre",
        "instruction": "instructions pour r�aliser l'exercice",
        "grade_max": 10,
        "script_id": 1,
        "correction_id": 1
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`course_id`]**: l'id du cour;
* **[string:`title`]**: le titre de l'exercice;
* **[string:`instruction`]**: les instruction � suivre pour r�aliser l'exercice;
* **[integer:`grade_max`]**: le grade max qu'on peux avoir en r�alisant l'exercice;
* **[integer:`script_id`]**: l'id du script de correction;
* **[integer:`correction_id`]**: l'exercice corrig�.

### Cr�ation d'exercice r�ussit
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Exercice d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT [JSON RAW]: /exercise/correction/create
### Param�tres � envoyer
```
    {
        "token": "0123456789ABCDEF",
        "content": "Texte de correction"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`content`]**: contient le texte de correction.

### Cr�ation d'une correction r�ussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: contient l'id de la correction r�ssament enregistr�e dans la base de donn�e;
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Correction d�j� pr�sente dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT [JSON RAW]: /exercise/script/create
### Param�tres � envoyer
```
    {
        "token": "0123456789ABCDEF",
        "content": "Contient le script de correction"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`content`]**: contient le script de correction.

### Cr�ation d'un script de correction r�ussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: contient l'id d'u script r�ssament enregistr�e dans la base de donn�e;
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Script d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT [JSON RAW]: /exercise/script/log/create
### Param�tres � envoyer
```
    {
        "token": "0123456789ABCDEF",
        "content": "Traces d'�x�cution",
        "script_id": 1
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`content`]**: contient les informations d'�x�cution de la correction";
* **[integer:`script_id`]**: contient l'id d'un script.

### Cr�ation d'un rapport rattach� � un script r�ussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: contient l'id du rapport cr��.
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Rapport d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT  [JSON RAW]: /exercise/grade/create
### Param�tres � envoyer
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

### Cr�ation d'un grade r�ussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: contient l'id du grade ajout�;
* **[integer:`status`]**: code 200.

### La valeur du grade a d�pass�e la valeur max
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Grade d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT [JSON RAW]: /exercise/user/create
### Param�tres � envoyer
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

### Cr�ation d'exercice r�alis� par l'utilisateur r�ussit
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Exercice r�alis� par l'utilisateur d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT [JSON RAW]: /exercise/user/code/create
### Param�tres � envoyer
```
    {
        "token": "0123456789ABCDEF",
        "user_exercice_id": 1,
        "content": "code r�dig�..."
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`user_exercice_id`]**: l'id de l'exercice r�alis� par l'utilisateur,
* **[string:`content`]**: code r�dig� par l'utilisateur.

### Cr�ation de code r�ussit
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Code d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Exercice] PUT  [JSON RAW]: /exercise/comment/create
### Param�tres � envoyer
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

### Cr�ation de commentaire sur exercice r�ussit
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Commentaire sur exercice d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Cour] PUT [JSON RAW]: /course/create
### Param�tres � envoyer
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
* **[string:`title`]**: intitul� du cour;
* **[string:`content`]**: contenue du cour.

### Cr�ation d'un cour r�ussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: l'id du cour r�dig�;
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Cour d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Cour] PUT  [JSON RAW]: /course/language/create
### Param�tres � envoyer
```
    {
        "token": "0123456789ABCDEF",
        "name": "C++"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`name`]**: contient le language de programmation.

### Cr�ation d'un langage pour un cour r�ussit
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Langage d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Cour] PUT [JSON RAW]: /course/commente/create
### Param�tres � envoyer
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

### Cr�ation d'un commentaire pour un cour r�ussit
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Commentaire de cour d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Blog] PUT [JSON RAW]: /blog/post/create
### Param�tres � envoyer
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

### Cr�ation d'un post r�ussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: l'id du post cr��;
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Post d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Blog] PUT [JSON RAW]: /blog/post/category/create
### Param�tres � envoyer
```
    {
        "token": "0123456789ABCDEF",
        "name": "categorie"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`name`]**: nom de la cat�gorie.

### Cr�ation d'une cat�gorie r�ussit
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Cat�gorie d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Blog] PUT [JSON RAW]: /blog/post/comment/create
### Param�tres � envoyer
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

### Cr�ation d'un commentaire en r�ponse � un post r�ussit
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Commentaire d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Forum] PUT [JSON RAW]: /forum/create
### Param�tres � envoyer
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

### Cr�ation d'un forum de discussion r�ussit
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Forum de discussion d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Forum] PUT [JSON RAW]: /forum/categorie/create
### Param�tres � envoyer
```
    {
        "token": "0123456789ABCDEF",
        "name": ""
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`name`]**: nom de la categorie.

### Cr�ation d'une categorie de forum r�ussit
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Cat�gorie de forum d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Forum] PUT [JSON RAW]: /forum/post/create
### Param�tres � envoyer
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

### Cr�ation d'un post de forum r�ussit
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Post de forum d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Forum] PUT [JSON RAW]: /forum/subject/create
### Param�tres � envoyer
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

### Cr�ation d'un sujet de discussion r�ussit
```
    {
        "id": 1,
        "status": 200
    }
```
* **[integer:`id`]**: l'id du sujet cr��;
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Sujet de discussion d�j� pr�sent dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.

## [Autre] PUT [JSON RAW]: /other/locale/create
### Param�tres � envoyer
```
    {
        "token": "0123456789ABCDEF",
        "name": "FR"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`name`]**: nom de la langue.

### Cr�ation de langue r�ussit
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

### Informations mal format�s
```
    {
        "status": 601
    }
```
* **[integer:`status`]**: code 601.

### Langue d�j� pr�sente dans la base de donn�e
```
    {
        "status": 600
    }
```
* **[integer:`status`]**: code 600.