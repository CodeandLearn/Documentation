# Codes
## Informations
* **100**: Attent de la suite de la requête.

## Succès
* **200**: Requête traitée avec succès;
* **204**: Requête traitée avec succès mais pas d'information à renvoyer.

## Erreurs client / serveur
* **400**: La syntaxe de la requête est erronée;
* **401**: Une authentification est nécessaire pour accéder à la ressource;
* **403**: Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée;
* **404**: Ressource non trouvée;
* **405**: Méthode de requête non autorisée;
* **411**: La longueur de la requête n'a pas été précisée;
* **418**: I"m a teapot !!!;
* **429**: Le client a émis trop de requêtes dans un délai donné;
* **500**: Erreur interne du serveur;

## Suppression en cour...
* **601**: Une donnée est mal formatée;
* **602**: Donnée invalide;
* **603**: Donnée manquante;
* **604**: Une valeur dépasse la valeur max;

## Codes additionnel
* **600**: Donnée déjà présente dans la base de donnée;
* **700**: L'utilisateur est banni.

***

# Examples
## [400] La syntaxe de la requête est erronée
***
```
	{
		"timestamp": 1453903559817,
		"status": 400,
		"error": "Bad Request",
		"message": "Validation failed for...",
		"path": "/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 400;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

## [401] Une authentification est nécessaire pour accéder à la ressource
***

## [403] Le serveur a compris la requête, mais refuse de l'exécuter, permission non accordée
***
```
	{
		"timestamp": 1453903559817,
		"status": 403,
		"error": "Forbidden",
		"message": "...",
		"path": "/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 403;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

## [404] Ressource non trouvée
***
```
	{
		"timestamp": 1453903559817,
		"status": 404,
		"error": "Not Found",
		"message": "...",
		"path": "/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 404;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

## [405] Méthode de requête non autorisée
***
```
	{
		"timestamp": 1453903559817,
		"status": 405,
		"error": "Method Not Allowed",
		"message": "...",
		"path": "/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 405;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

## [411] La longueur de la requête n'a pas été précisée
***
```
	{
		"timestamp": 1453903559817,
		"status": 411,
		"error": "Length Required",
		"message": "...",
		"path": "/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 411;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

## [418] I"m a teapot !!!
***

## [429] Le client a émis trop de requêtes dans un délai donné
***
```
	{
		"timestamp": 1453903559817,
		"status": 429,
		"error": "Too Many Requests",
		"message": "...",
		"path": "/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 429;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.

## [500] Erreur interne du serveur
***
```
	{
		"timestamp": 1453903559817,
		"status": 500,
		"error": "Internal Server Error",
		"message": "...",
		"path": "/"
	}
```
* **[integer:`timestamp`]**: timestamp au moment de l'exécution de la requête;
* **[integer:`status`]**: code 500;
* **[string:`error`]**: message d'erreur généralisé;
* **[string:`message`]**: message d'erreur plus détaillé;
* **[string:`path`]**: chemin de la requête.