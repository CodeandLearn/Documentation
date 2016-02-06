# References PUT
## [Compte] PUT: /account/create/[string:username]/[string:password]/[string:email]
***
### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/account/create"
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
		"path": "/account/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/account/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Compte] PUT: /account/group/create/[string:name]/[integer:parent_id]
***
### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 204;
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
		"path": "/account/group/create/"
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
		"path": "/account/group/create/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/account/group/create/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Account] PUT: /account/token/renew/[string:token]
### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`ttl`]**: durée de validité du token en secondes;
* **[integer:`status`]**: code 204;
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
		"path": "/account/token/renew/"
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
		"path": "/account/token/renew/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Exercice] PUT [JSON RAW]: /exercise/create
***
### Envoi
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

***

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 204;
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
		"path": "/exercise/create"
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
		"path": "/exercise/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* **[integer:`exercice_id`]**: id de modération de l'exercice à créer;
* **[integer:`moderation_validate_id`]**: id du statut de modération;
* **[string:`commentary`]**: commentaire relatif à la modération.

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 204;
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
		"path": "/exercise/moderation/create"
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
		"path": "/exercise/moderation/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/moderation/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/exercise/correction/create"
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
		"path": "/exercise/correction/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/correction/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/exercise/script/create"
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
		"path": "/exercise/script/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/script/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Exercice] PUT [JSON RAW]: /exercise/script/log/create
***
### Envoi
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

***

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/exercise/script/log/create"
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
		"path": "/exercise/script/log/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/script/log/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/exercise/grade/create"
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
		"path": "/exercise/grade/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/grade/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/exercise/user/create"
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
		"path": "/exercise/user/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/user/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***

## [Exercice] PUT [JSON RAW]: /exercise/user/code/create
***
### Envoi
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

***

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/exercise/user/code/create"
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
		"path": "/exercise/user/code/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/user/code/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/exercise/comment/create"
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
		"path": "/exercise/comment/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/exercise/comment/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* **[string:`title`]**: intitulé du cour;
* **[string:`content`]**: contenu du cour.

***

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/course/create"
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
		"path": "/course/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/course/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* **[integer:`moderation_validate_id`]**: id du statut du cour à modérer;
* **[string:`commentary`]**: commentaire relatif au cour.

***

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
* **[integer:`status`]**: code 204;
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
		"path": "/course/moderation/create"
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
		"path": "/course/moderation/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/course/moderation/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/course/language/create"
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
		"path": "/course/language/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/course/language/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/course/commente/create"
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
		"path": "/course/commente/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/course/commente/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/blog/post/create"
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
		"path": "/blog/post/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/blog/post/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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
* **[string:`name`]**: nom de la catégorie.

***

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/blog/post/category/create"
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
		"path": "/blog/post/category/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/blog/post/category/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/blog/post/comment/create"
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
		"path": "/blog/post/comment/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/blog/post/comment/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/forum/create"
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
		"path": "/forum/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/forum/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/forum/categorie/create"
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
		"path": "/forum/categorie/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/forum/categorie/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/forum/post/create"
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
		"path": "/forum/post/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/forum/post/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/forum/subject/create"
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
		"path": "/forum/subject/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/forum/subject/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/other/locale/create"
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
		"path": "/other/locale/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/other/locale/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès
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
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`id`]**: id de l'enregistrement;
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
		"path": "/other/avatar/create"
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
		"path": "/other/avatar/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/other/avatar/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

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

### Réception
***
#### Requête traitée avec succès mais pas d'information à renvoyer
```
	{
		"timestamp": 1453903559817,
		"status": 204,
		"error": "No Content",
		"message": "...",
		"path": "/other/moderation/statut/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 204;
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
		"path": "/other/moderation/statut/create"
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
		"path": "/other/moderation/statut/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

#### Donnée déjà présente dans la base de donnée
```
	{
		"timestamp": 1453903559817,
		"status": 600,
		"error": "...",
		"message": "...",
		"path": "/other/moderation/statut/create"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 600;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

***