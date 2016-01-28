# References POST
## [Connexion] POST: /login/[string:username]/[string:password]
***
### Réception
***
### Connexion réussit
```
	{
		"token": "0123456789ABCDEF",
		"ttl": 3600,
		"status": 200,
		"error": "...",
		"message": "...",
		"path": "/login"
	}
```
* **[string:`token`]**: renvoie le token de la session en cours;
* **[integer:`ttl`]**: renvoie le temps restant de la session en cours, temps en secondes;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

### Ressource non trouvée
```
	{
		"attempts": 1,
		"max_attemps": 3,
		"cooldown": 3600,
		"status": 404,
		"error": "Not Found",
		"message": "...",
		"path": "/login"
	}
```
* **[integer:`attempts`]**: le nombre de tentatives de connexion;
* **[integer:`max_attempts`]**: le nombre maximum de tentatives;
* **[integer:`coldown`]**: le temps avant que le nombre de tentatives se remette à 0, temps en secondes;
* **[integer:`status`]**: code 404;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

### Le client a émis trop de requêtes dans un délai donné
```
    {
        "attempts": 3,
		"max_attemps": 3,
        "ban_duration": 36000,
        "status": 429,
		"error": "Too Many Requests",
		"message": "...",
		"path": "/login"
    }
```
* **[integer:`attempts`]**: le nombre de tentatives réalisés, se référer à `max_attempts`;
* **[integer:`max_attempts`]**: le nombre maximum de tentatives;
* **[integer:`ban_duration`]**: le temps avant d'autoriser à nouveau à l'utilisateur de se connecter, temps en secondes;
* **[integer:`statuts`]**: code 429;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

### Utilisateur banni
```
    {
        "login_ban_duration_end": 3600,
        "status": 700,
		"error": "...",
		"message": "...",
		"path": "/login"
    }
```
* **[integer:`login_ban_duration_end`]**: le temps restant que l'utilisateur est banni, temps en secondes;
* **[integer:`status`]**: code 700;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Compte] POST [JSON RAW]: /account/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"username": "",
		"password": "",
		"email": "",
		"group_id": 1,
		"avatar_id": 1
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: .

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
```
	{
		"timestamp": 1453903559817,
		"status": 204,
		"path": "/account/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 204;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/account/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### La syntaxe de la requête est erronée
```
	{
		"token": "0123456789ABCDEF",
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/account/modify"
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Compte] POST [JSON RAW]: /account/group/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"name": "",
		"parent_id": 1
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Exercice] POST [JSON RAW]: /exercise/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"account_id": 1,
		"course_id": 1,
		"title": "",
		"instruction": "",
		"script_id": 1,
		"grade_max": 10,
		"correction_id": 1
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Exercice] POST: /exercise/moderation/validate/[boolean:value]
***
### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Exercice] POST [JSON RAW]: /exercise/correction/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"content": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Exercice] POST [JSON RAW]: /exercise/script/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"content": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Exercice] POST [JSON RAW]: /exercise/script/log/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"content": "",
		"script_id": 1
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Exercice] POST  [JSON RAW]: /exercise/grade/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"account_id": 1,
		"exercice_id": 1,
		"value": 10,
		"log_id": 1
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Exercice] POST [JSON RAW]: /exercise/user/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"account_id": 1,
		"exercice_id": 1,
		"grade_id": 1
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Exercice] POST [JSON RAW]: /exercise/user/code/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"user_exercice_id": 1,
		"content": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Exercice] POST  [JSON RAW]: /exercise/comment/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"exercice_id": 1,
		"account_id": 1,
		"content": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Cour] POST [JSON RAW]: /course/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"account_id": 1,
		"locales_id": 1,
		"language_id": 1,
		"title": "",
		"content": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Cour] POST: /course/moderation/validate/[string:token]/[boolean:value]
***
### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Cour] POST  [JSON RAW]: /course/language/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"name": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Cour] POST [JSON RAW]: /course/commente/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"couse_id": 1,
		"account_id": 1,
		"content": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: .

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Blog] POST [JSON RAW]: /blog/post/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"account_id": 1,
		"locales_id": 1,
		"blog_category_id": 1,
		"title": "",
		"content": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: .

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Blog] POST [JSON RAW]: /blog/post/category/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"name": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: .

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Blog] POST [JSON RAW]: /blog/post/comment/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"account_id": 1,
		"blog_post_id": 1,
		"content": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: .

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Forum] POST [JSON RAW]: /forum/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"forum_category_id": 1,
		"name": "",
		"description": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: .

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Forum] POST [JSON RAW]: /forum/categorie/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"name": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: .

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Forum] POST [JSON RAW]: /forum/post/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"forum_subject_id": 1,
		"account_id": 1,
		"content": "",
		"likes": 1
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: .

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Forum] POST [JSON RAW]: /forum/post/like/[string:token]
### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Forum] POST [JSON RAW]: /forum/post/likes/[string:token]/[integer:likes]
### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Forum] POST [JSON RAW]: /forum/subject/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"forums_forum_id": 1,
		"locales_id": 1,
		"account_id": 1
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: ;
* **[:``]**: .

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Autre] POST [JSON RAW]: /other/locale/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"name": ""
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: .

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***

## [Autre] POST [JSON RAW]: /other/avatar/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"path": "./../../"
	}
```
* **[string:`token`]**: le token de la session en cours;
* **[:``]**: ;
* **[:``]**: .

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
#### La syntaxe de la requête est erronée
***