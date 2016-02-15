# References POST
## [Connexion] POST: /login/[string:username]/[string:password]
***
### Réception
***
#### Connexion réussit
```
	{
		"timestamp": 1453903559817,
		"token": "0123456789ABCDEF",
		"ttl": 3600,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/login"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[string:`token`]**: renvoie token de la session en cours;
* **[integer:`ttl`]**: renvoie le temps restant de la session en cours, temps en secondes;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Ressource non trouvée
```
	{
		"timestamp": 1453903559817,
		"attempts": 1,
		"max_attemps": 3,
		"cooldown": 3600,
		"status": 404,
		"error": "Not Found",
		"message": "...",
		"path": "/login"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`attempts`]**: nombre de tentatives de connexion;
* **[integer:`max_attempts`]**: nombre maximum de tentatives;
* **[integer:`coldown`]**: temps avant que le nombre de tentatives se remette à 0, temps en secondes;
* **[integer:`status`]**: code 404;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le client a émis trop de requêtes dans un délai donné
```
    {
		"timestamp": 1453903559817,
        "attempts": 3,
		"max_attemps": 3,
        "ban_duration": 36000,
        "status": 429,
		"error": "Too Many Requests",
		"message": "...",
		"path": "/login"
    }
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`attempts`]**: nombre de tentatives réalisés, se référer à `max_attempts`;
* **[integer:`max_attempts`]**: nombre maximum de tentatives;
* **[integer:`ban_duration`]**: temps avant d'autoriser à nouveau à l'utilisateur de se connecter, temps en secondes;
* **[integer:`statuts`]**: code 429;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Utilisateur banni
```
    {
		"timestamp": 1453903559817,
        "login_ban_duration_end": 3600,
        "status": 700,
		"error": "...",
		"message": "...",
		"path": "/login"
    }
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`login_ban_duration_end`]**: temps restant que l'utilisateur est banni, temps en secondes;
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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du compte à modifier;
* **[string:`username`]**: nouveau nom de compte;
* **[string:`password`]**: nouveau mot de passe;
* **[string:`email`]**: nouveau mail utilisateur;
* **[integer:`group_id`]**: id du nouveau groupe pour l'utilisateur;
* **[integer:`avatar_id`]**: id du nouvel avatar.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/account/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/account/modify"
	}
```
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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du group à modifier;
* **[string:`name`]**: nouveau nom;
* **[string:`parent_id`]**: id du nouveau parent.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/account/group/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/account/group/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/account/group/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id de l'exercice à modifier;
* **[integer:`account_id`]**: id du nouvel auteur;
* **[integer:`course_id`]**: id du nouveau cour de référence;
* **[string:`title`]**: nouveau titre;
* **[string:`instruction`]**: nouvelles instructions;
* **[integer:`script_id`]**: id du nouveau script de correction;
* **[integer:`grade_max`]**: nouveau grade maximum;
* **[integer:`correction_id`]**: id de la nouvelle correction.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Exercice] POST [JSON RAW]: /exercise/moderation/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"exercice_id": 1,
		"moderation_validate_id": 1,
		"commentary": ""
	}
```
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`exercice_id`]**: id de modération de l'exercice à modifier;
* **[integer:`moderation_validate_id`]**: id du statut de modération;
* **[string:`commentary`]**: commentaire relatif à la modération.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/moderation/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/moderation/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/moderation/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id de la correction;
* @NOT NULL **[string:`content`]**: contenue de la correction.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/correction/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/correction/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/correction/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du script;
* @NOT NULL **[string:`content`]**: contenu du script.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/script/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/script/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/script/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du rapport du script;
* **[string:`content`]**: contenue du rapport d'exécution;
* **[integer:`script_id`]**: id du script de correction.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/script/log/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/script/log/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/script/log/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Exercice] POST [JSON RAW]: /exercise/grade/modify
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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du grade;
* **[integer:`account_id`]**: id de l'utilisateur;
* **[integer:`exercice_id`]**: id de l'exercice;
* **[integer:`value`]**: valeur du grade;
* **[integer:`log_id`]**: id du rapport d'exécution.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/grade/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/grade/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/grade/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id de l'exercice rédigé par l'utilisateur;
* **[integer:`account_id`]**: id de l'utilisateur;
* **[integer:`exercice_id`]**: id de l'exercice;
* **[integer:`grade_id`]**: id du grade reçu.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/user/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/user/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/user/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du code rédigé par l'utilisateur;
* **[integer:`user_exercice_id`]**: id de l'exercice rédigé par l'utilisateur;
* **[string:`content`]**: contenu du code.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/user/code/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/user/code/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/user/code/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Exercice] POST [JSON RAW]: /exercise/comment/modify
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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du commentaire de l'exercice;
* **[integer:`exercice_id`]**: id de l'exercice;
* **[integer:`account_id`]**: id de l'auteur du commentaire;
* **[string:`content`]**: contenue du commentaire.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/comment/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/comment/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/comment/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du cour à modifier;
* **[integer:`account_id`]**: id de l'auteur du cour;
* **[integer:`locales_id`]**: id de la langue du cour;
* **[integer:`language_id`]**: id du langage de programmation du cour;
* **[string:`title`]**: titre du cour;
* **[string:`content`]**: contenue du cour.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/course/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/course/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/course/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Cour] POST [JSON RAW]: /course/moderation/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"course_id": 1,
		"moderation_validate_id": 1,
		"commentary": ""
	}
```
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`course_id`]**: id du cour;
* **[integer:`moderation_validate_id`]**: id du statut du cour à modérer;
* **[string:`commentary`]**: commentaire relatif au cour.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/course/moderation/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/course/moderation/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/course/moderation/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Cour] POST [JSON RAW]: /course/language/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"name": "C++"
	}
```
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du langage de programmation;
* **[string:`name`]**: nom du langage de programmation.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/course/language/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/course/language/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/course/language/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du commentaire du cour;
* **[integer:`course_id`]**: id du cour;
* **[integer:`account_id`]**: id de l'auteur;
* **[string:`content`]**: contenu du commentaire.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/course/commente/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/course/commente/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/course/commente/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du post;
* **[integer:`account_id`]**: id de l'auteur;
* **[integer:`locales_id`]**: id de la langue;
* **[integer:`blog_category_id`]**: id de la categorie;
* **[string:`title`]**: titre du post;
* **[string:`content`]**: contenue du post.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/blog/post/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/blog/post/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/blog/post/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id de la categorie;
* **[string:`name`]**: nom de la categorie.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/blog/post/category/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/blog/post/category/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/blog/post/category/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du commentaire de post;
* **[integer:`account_id`]**: id de l'auteur;
* **[integer:`blog_post_id`]**: id du post;
* **[string:`content`]**: contenu du commentaire.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/blog/post/comment/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/blog/post/comment/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/blog/post/comment/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du forum;
* **[integer:`forum_category_id`]**: id de la categorie du forum;
* **[string:`name`]**: nom du forum;
* **[string:`description`]**: description du forum.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/forum/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/forum/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/forum/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id de la categorie;
* **[string:`name`]**: nom de la categorie.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/forum/categorie/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/forum/categorie/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/forum/categorie/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du post;
* **[integer:`forum_subject_id`]**: id du sujet de forum;
* **[integer:`account_id`]**: id de l'auteur;
* **[string:`content`]**: contenu du post;
* **[integer:`likes`]**: nombre de j'aime du post.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/forum/post/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/forum/post/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/forum/post/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Forum] POST: /forum/post/like/[string:token]
### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/forum/post/like"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/forum/post/like"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/forum/post/like"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Forum] POST: /forum/post/likes/[string:token]/[integer:likes]
### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/forum/post/likes"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/forum/post/likes"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/forum/post/likes"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du sujet;
* **[integer:`forums_forum_id`]**: id du forum;
* **[integer:`locales_id`]**: id de la langue;
* **[integer:`account_id`]**: id de l'auteur.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/forum/subject/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/forum/subject/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/forum/subject/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Autre] POST [JSON RAW]: /other/locale/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"name": "FR"
	}
```
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id de la langue;
* **[string:`name`]**: nom de la langue.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/other/locale/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/other/locale/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/other/locale/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id de l'avatar;
* **[string:`path`]**: chemin de l'avatar.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/other/avatar/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/other/avatar/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/other/avatar/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Autre] POST [JSON RAW]: /other/moderation/statut/modify
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"id": 1,
		"name": "FR"
	}
```
* @NOT NULL **[string:`token`]**: token de la session en cours;
* @NOT NULL **[integer:`id`]**: id du statut;
* **[string:`name`]**: nom du statut.

***

### Réception
***
#### Requête traitée avec succès
```
	{
		"timestamp": 1453903559817,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/other/moderation/statut/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/other/moderation/statut/modify"
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
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/other/moderation/statut/modify"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***