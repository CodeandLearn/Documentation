# References PUT
## [Compte] PUT: /account/create/[string:username]/[string:password]/[string:email]
***
### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/account/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/account/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/account/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/account/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Compte] PUT: /account/group/create/[string:name]/[integer:parent_id]
***
### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 204,
		"error": "No Content",
		"message": "...",
		"path": "/account/group/create/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 204;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/account/group/create/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/account/group/create/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/account/group/create/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Account] PUT: /account/token/renew/[string:token]
### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
        "ttl": 3600,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/account/token/renew/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`ttl`]**: dur�e de validit� du token en secondes;
* **[integer:`status`]**: code 204;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/account/token/renew/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/account/token/renew/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Exercice] PUT [JSON RAW]: /exercise/create
***
### Envoi
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

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 204,
		"error": "No Content",
		"message": "...",
		"path": "/exercise/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 204;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Exercice] POST [JSON RAW]: /exercise/moderation/create
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
* **[string:`token`]**: token de la session en cours;
* **[integer:`exercice_id`]**: id de mod�ration de l'exercice � cr�er;
* **[integer:`moderation_validate_id`]**: id du statut de mod�ration;
* **[string:`commentary`]**: commentaire relatif � la mod�ration.

***

### R�ception
***
#### Requ�te trait�e avec succ�s mais pas d'information � renvoyer
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/moderation/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 204;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/moderation/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/moderation/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/moderation/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Exercice] PUT [JSON RAW]: /exercise/correction/create
***
### Envoi
```
    {
        "token": "0123456789ABCDEF",
        "content": "Texte de correction"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`content`]**: contient le texte de correction.

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/correction/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/correction/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/correction/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/correction/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Exercice] PUT [JSON RAW]: /exercise/script/create
***
### Envoi
```
    {
        "token": "0123456789ABCDEF",
        "content": "Contient le script de correction"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`content`]**: contient le script de correction.

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/script/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/script/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/script/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/script/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Exercice] PUT [JSON RAW]: /exercise/script/log/create
***
### Envoi
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

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/script/log/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/script/log/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/script/log/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/script/log/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Exercice] PUT [JSON RAW]: /exercise/grade/create
***
### Envoi
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

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/grade/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/grade/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/grade/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/grade/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Exercice] PUT [JSON RAW]: /exercise/user/create
***
### Envoi
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

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/user/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/user/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/user/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/user/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Exercice] PUT [JSON RAW]: /exercise/user/code/create
***
### Envoi
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

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/user/code/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/user/code/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/user/code/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/user/code/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Exercice] PUT [JSON RAW]: /exercise/comment/create
***
### Envoi
```
    {
        "token": "0123456789ABCDEF",
        "exercice_id": 1,
        "content": "commentaire"
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`exercice_id`]**: l'id de l'exercice;
* **[string:`content`]**: contenu du commentaire.

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/exercise/comment/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/exercise/comment/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/exercise/comment/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/comment/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Cour] PUT [JSON RAW]: /course/create
***
### Envoi
```
    {
        "token": "0123456789ABCDEF",
        "local_id": 1,
        "language_id": 1,
        "title": "titre",
        "content": "contenu"
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`local_id`]**: l'id de la langue;
* **[integer:`language_id`]**: l'id de la langue de programmation;
* **[string:`title`]**: intitul� du cour;
* **[string:`content`]**: contenu du cour.

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/course/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/course/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/course/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/course/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Cour] POST [JSON RAW]: /course/moderation/create
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
* **[string:`token`]**: token de la session en cours;
* **[integer:`course_id`]**: id du cour;
* **[integer:`moderation_validate_id`]**: id du statut du cour � mod�rer;
* **[string:`commentary`]**: commentaire relatif au cour.

***

### R�ception
***
#### Requ�te trait�e avec succ�s mais pas d'information � renvoyer
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/course/moderation/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 204;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/course/moderation/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/course/moderation/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/course/moderation/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Cour] PUT [JSON RAW]: /course/language/create
***
### Envoi
```
    {
        "token": "0123456789ABCDEF",
        "name": "C++"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`name`]**: contient le language de programmation.

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/course/language/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/course/language/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/course/language/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/course/language/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Cour] PUT [JSON RAW]: /course/commente/create
***
### Envoi
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

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/course/commente/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/course/commente/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/course/commente/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/course/commente/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Blog] PUT [JSON RAW]: /blog/post/create
***
### Envoi
```
    {
        "token": "0123456789ABCDEF",
        "local_id": 1,
        "blog_category_id": 1,
        "title": "string contenu",
        "content": "contenu"
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`local_id`]**: l'id de la langue;
* **[integer:`blog_category_id`]**: l'id de la categorie du blog;
* **[string:`title`]**: titre du post;
* **[string:`content`]**: contenu du post.

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/blog/post/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/blog/post/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/blog/post/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/blog/post/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Blog] PUT [JSON RAW]: /blog/post/category/create
***
### Envoi
```
    {
        "token": "0123456789ABCDEF",
        "name": "categorie"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`name`]**: nom de la cat�gorie.

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/blog/post/category/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/blog/post/category/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/blog/post/category/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/blog/post/category/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Blog] PUT [JSON RAW]: /blog/post/comment/create
***
### Envoi
```
    {
        "token": "0123456789ABCDEF",
        "blog_post_id": 1,
        "content": "contenu"
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`blog_post_id`]**: l'id du post;
* **[string:`content`]**: contenu du commentaire.

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/blog/post/comment/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/blog/post/comment/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/blog/post/comment/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/blog/post/comment/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Forum] PUT [JSON RAW]: /forum/create
***
### Envoi
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

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/forum/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/forum/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/forum/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/forum/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Forum] PUT [JSON RAW]: /forum/categorie/create
***
### Envoi
```
    {
        "token": "0123456789ABCDEF",
        "name": ""
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`name`]**: nom de la categorie.

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/forum/categorie/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/forum/categorie/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/forum/categorie/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/forum/categorie/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Forum] PUT [JSON RAW]: /forum/post/create
***
### Envoi
```
    {
        "token": "0123456789ABCDEF",
        "forum_subject_id": 1,
        "content": ""
    }
```
* **[string:`token`]**: token de connexion;
* **[integer:`forum_subject_id`]**: l'id du sujet du forum;
* **[string:`content`]**: contenu du post.

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/forum/post/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/forum/post/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/forum/post/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/forum/post/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Forum] PUT [JSON RAW]: /forum/subject/create
***
### Envoi
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

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/forum/subject/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/forum/subject/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/forum/subject/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/forum/subject/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Autre] PUT [JSON RAW]: /other/locale/create
***
### Envoi
```
    {
        "token": "0123456789ABCDEF",
        "name": "FR"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`name`]**: nom de la langue.

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/other/locale/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/other/locale/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/other/locale/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/other/locale/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Autre] PUT [JSON RAW]: /other/avatar/create
***
### Envoi
```
    {
        "token": "0123456789ABCDEF",
        "path": "./../../"
    }
```
* **[string:`token`]**: token de connexion;
* **[string:`path`]**: chemin de l'avatar.

***

### R�ception
***
#### Requ�te trait�e avec succ�s
```
	{
		"timestamp": 1453903559817,
		"id": 1,
		"status": 200,
		"error": "OK",
		"message": "...",
		"path": "/other/avatar/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 200;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/other/avatar/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/other/avatar/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/other/avatar/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***

## [Autre] POST [JSON RAW]: /other/moderation/statut/create
***
### Envoi
```
	{
		"token": "0123456789ABCDEF",
		"name": "FR"
	}
```
* **[string:`token`]**: token de la session en cours;
* **[string:`name`]**: nom du statut.

***

### R�ception
***
#### Requ�te trait�e avec succ�s mais pas d'information � renvoyer
```
	{
		"timestamp": 1453903559817,
		"status": 204,
		"error": "No Content",
		"message": "...",
		"path": "/other/moderation/statut/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 204;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Le serveur a compris la requ�te, mais refuse de l'ex�cuter, permission non accord�e
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/other/moderation/statut/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### La syntaxe de la requ�te est erron�e
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/other/moderation/statut/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

#### Donn�e d�j� pr�sente dans la base de donn�e
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/other/moderation/statut/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'ex�cution de la requ�te;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur g�n�ralis�;
* **[string:`message`]**: message d'erreur plus d�taill�;
* **[string:`path`]**: chemin de la requ�te.

***