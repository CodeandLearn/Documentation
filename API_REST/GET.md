# Réferences GET
##### GET: /user/<string:token>/<string:username>
Renvoie les informations sur l’utilisateur “username”.

Si le Status HTTP est 200:
```
	{
		"user_id": 0,
		"username": "John",
		"user_email": "john@legend.ie",
		"user_group_id": 1,
		"status": 200
	}
```
* `user_id` : l’id de l’utilisateur dans la base de données;
* `username` : le nom de l’utilisateur;
* `user_email` : son email;
* `user_group_id` : le groupe auquel il appartient (permet de connaître ses permissions);
* `error_code`: code 200, voir [Codes d'erreur]("./ERROR.md").

Si l’utilisateur n’a pas été trouvé (404):
```
	{
		"error": "No user found with this name."
	}
```
En cas de permissions insuffisantes (401):
```
	{
		"error": "You’re not allowed to see this."
	}
```

##### GET: /user/id/<string:token>/<int:id>
Renvoie les informations sur l’utilisateur par son id.

Si le Status HTTP est 200:
```
	{
		"user_id": 0,
		"username": "John",
		"user_email": "john@legend.ie",
		"user_group_id": 1,
		"status": 200
	}
```
* `user_id` : l’id de l’utilisateur dans la base de données;
* `username` : le nom de l’utilisateur;
* `user_email` : son email;
* `user_group_id` : le groupe auquel il appartient (permet de connaître ses permissions);
* `error_code`: code 200, voir [Codes d'erreur]("./ERROR.md").

Si l’utilisateur n’a pas été trouvé (404):
```
	{
		"error": "No user found with this id."
	}
```
En cas de permissions insuffisantes (401):
```
	{
		"error": "You’re not allowed to see this."
	}
```