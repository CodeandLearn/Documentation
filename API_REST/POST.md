# References POST
##### POST: /login
Si l’utilisateur est connecté, renvoie un token et le ttl de la session.
```
	{
		"token": "0123456789ABCDEF",
		"token_ttl": 3600,
		"status": 200
	}
```
* `token`: renvoie le token de la session en cours;
* `token_ttl`: renvoie le temps restant de la session en cours;
* `error_code`: code 200, voir [Codes d'erreur]("./ERROR.md").

Si l’utilisateur n’est pas connecté, renvoie un Status HTTP de 429 si l’utilisateur a dépassé le nombre de tentative d’authentification sinon renvoie :
```
	{
		"login_attempts": 1,
		"login_max_attemps": 3,
		"login_cooldown": 3600,
		"status": 404
	}
```
* `login_attempts`: le nombre de tentatives de connexion;
* `login_max_attempts`: le nombre maximum de tentatives;
* `login_coldown`: le temps avant que le nombre de tentatives se remette à 0, temps en secondes;
* `error_code`: code 404, voir [Codes d'erreur]("./ERROR.md").
```
    {
        "login_attempts": 3,
        "login_ban_duration": 36000,
        "status": 429
    }
```
* `login_attempts`: le nombre de tentatives réalisés, se référer à `login_max_attempts`;
* `login_ban_duration`: le temps avant d'autoriser à nouveau à l'utilisateur de se connecter, temps en secondes;
* `error_code`: code 429, voir [Codes d'erreur]("./ERROR.md").