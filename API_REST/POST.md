# References POST
##### POST: /login/<string:username>/<string:password>
###### Connexion réussit
```
	{
		"token": "0123456789ABCDEF",
		"token_ttl": 3600,
		"status": 200
	}
```
* `token`<string>: renvoie le token de la session en cours;
* `token_ttl`<integer>: renvoie le temps restant de la session en cours;
* `status`<integer: code 200, voir [Codes d'erreur]("./API_REST/ERROR.md").
###### Username ou password erroné
```
	{
		"login_attempts": 1,
		"login_max_attemps": 3,
		"login_cooldown": 3600,
		"status": 404
	}
```
* `login_attempts`<integer>: le nombre de tentatives de connexion;
* `login_max_attempts`<integer>: le nombre maximum de tentatives;
* `login_coldown`<integer>: le temps avant que le nombre de tentatives se remette à 0, temps en secondes;
* `status`<integer>: code 404, voir [Codes d'erreur]("./API_REST/ERROR.md").
###### Trop de tentatives infructueuses
```
    {
        "login_attempts": 3,
        "login_ban_duration": 36000,
        "status": 429
    }
```
* `login_attempts`<integer>: le nombre de tentatives réalisés, se référer à `login_max_attempts`;
* `login_ban_duration`<integer>: le temps avant d'autoriser à nouveau à l'utilisateur de se connecter, temps en secondes;
* `statuts`<integer>: code 429, voir [Codes d'erreur]("./API_REST/ERROR.md").
###### Utilisateur banni
```
    {
        "login_ban_duration_end": xx,
        "status": 500
    }
```
* `login_ban_duration_end`<integer>: le temps restant que l'utilisateur est banni, temps en secondes;
* `status`<integer>: code 500, voir [Codes d'erreur]("./API_REST/ERROR.md").