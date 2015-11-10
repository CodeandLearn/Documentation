**DOC API CODE&LEARN**

*HTTP Status : 200 si Ok, 404 ou 500 si erreur*


# REFERENCES GET:


## GET: /login

Si l’utilisateur est connecté, renvoie un token et le ttl de la session.

    {
		"login_token": "0123456789ABCDEF",
		"login_ttl": 3600
	}

* `login_token` : renvoie le token de la session en cours;
* `login_ttl` : renvoie le temps restant de la session en cours.

Si l’utilisateur n’est pas connecté, renvoie un Status HTTP de 429 si l’utilisateur a dépassé le nombre de tentative d’authentification sinon renvoie :

    {
		"login_attempts": 1,
		"login_max_attemps": 3,
		"login_cooldown": 3600
	}

* `login_attempts` : le nombre de tentatives de connexion;
* `login_mac_attempts` : le nombre maximum de tentatives;
* `login_cooldown` : le temps avant que le nombre de tentaitves se remette à 0.

## GET: /user/&lt;string:username&gt;

Renvoie les informations sur l’utilisateur “username”.

Si le Status HTTP est 200:

	{
		"user_id": 0,
		"username": "John",
		"user_email": "john@legend.ie",
		"user_group_id": 1
	}

`user_id` : l’id de l’utilisateur dans la base de données.
`username` : le nom de l’utilisateur.
`user_email` : son email.
`user_group_id` : le groupe auquel il appartient (permet de connaître ses permissions)

Si l’utilisateur n’a pas été trouvé (404):

	{
		"error": "No user found with this name."
	}

En cas de permissions insuffisantes (401):

	{
		"error": "You’re not allowed to see this."
	}


## GET: /user/id/&lt;int:id&gt;

Renvoie les informations sur l’utilisateur par son id.

Si le Status HTTP est 200:

	{
		"user_id": 0,
		"username": "John",
		"user_email": "john@legend.ie",
		"user_group_id": 1
	}

`user_id` : l’id de l’utilisateur dans la base de données.
`username` : le nom de l’utilisateur.
`user_email` : son email.
`user_group_id` : le groupe auquel il appartient (permet de connaître ses permissions)

Si l’utilisateur n’a pas été trouvé (404):

	{
		"error": "No user found with this id."
	}

En cas de permissions insuffisantes (401):

	{
		"error": "You’re not allowed to see this."
	}

## GET: /permissions/&lt;int:id&gt;

Prend un id en paramètre. Renvoie les permissions liées à cet id si le Status HTTP est 200.

	{
		"permission_id": 0,
		"permission_name": “Admin”,
		"permission_code": 0,
		"group_id": 0
	}

`permission_id` : l’id de ces permissions.
`permission_name` : leur nom.
`permission_code` : permet de savoir ce qu’elles permettent.
`group_id` : le groupe possédant ces permissions.

Si l’id n’a pas été trouvé (404):

	{
		"error": "No permissions found with this id."
	}

En cas de permissions insuffisantes (401):

	{
		"error": "You’re not allowed to see this."
	}

## GET: /permissions/groupid/&lt;int:groupid&gt;

Prend l’id d’un groupe en paramètre. Renvoie les permissions liées à un groupe si le Status HTTP est 200.

	{
		"permission_id": 0,
		"permission_name": "Admin",
		"permission_code": 0,
		"group_id": 0
	}

`permission_id` : l’id de ces permissions.
`permission_name` : leur nom.
`permission_code` : permet de savoir ce qu’elles permettent.
`group_id` : le groupe possédant ces permissions.

Si le group_id n’a pas été trouvé (404):

	{
		"error": "No permissions found with this group id."
	}

En cas de permissions insuffisantes (401):

	{
	    "error": "You’re not allowed to see this."
	}