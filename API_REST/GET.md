# Introduction

HTTP Status: 200 si Ok, 404 ou 500 si erreur


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

* `user_id` : l’id de l’utilisateur dans la base de données;
* `username` : le nom de l’utilisateur;
* `user_email` : son email;
* `user_group_id` : le groupe auquel il appartient (permet de connaître ses permissions).

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

* `user_id` : l’id de l’utilisateur dans la base de données;
* `username` : le nom de l’utilisateur;
* `user_email` : son email;
* `user_group_id` : le groupe auquel il appartient (permet de connaître ses permissions)

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
		"permission_name": "Admin",
		"permission_code": 0,
		"group_id": 0
	}

* `permission_id` : l’id de ces permissions;
* `permission_name` : leur nom;
* `permission_code` : permet de savoir ce qu’elles permettent;
* `group_id` : le groupe possédant ces permissions.

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

* `permission_id` : l’id de ces permissions;
* `permission_name` : leur nom;
* `permission_code` : permet de savoir ce qu’elles permettent;
* `group_id` : le groupe possédant ces permissions.

Si le group_id n’a pas été trouvé (404):

	{
		"error": "No permissions found with this group id."
	}

En cas de permissions insuffisantes (401):

	{
	    "error": "You’re not allowed to see this."
	}

## GET: /course/list
renvoi la liste des cours
paramètres:
	{
	}

réponse en cas de succes (200): 
	[
		{
			"author" : "Serginho-kun",
			"title" : "Le C en 29 minutes",
			"tags" : "C",
			"languages": "C"
		}	
	]		
	
## GET: /course
renvoie un cours
paramètres:
	{
		"id" : 12
	}

réponse en cas de succes (200): 
	{
		"author" : "Serginho-kun",
		"title" : "Le C en 29 minutes",
		"tags" : "C",
		"languages": "C"
		"content" : "le texte c'est içi"
	}		
	
	
Si l'id n'as pas été trouvé (404):

	{
		"error": "Course not found."
	}
	
## GET: /course/comment
renvoie les commentaires du cours.

	{
		"course_id" : 45
	}

réponse en cas de succes (200): 
	[
		{
			"author" : "kevindu13",
			"content" "C'est nul",			
		}	
	]		

	
Si l'id n'as pas été trouvé (404):

	{
		"error": "Course not found."
	}
	
## GET: /course/languages/list
renvoie la liste des languages des cours

paramètres :
	[
		{
			"id" : 1,
			"name" : "C"
		}	
	]	
	
## GET: /exercice
renvoie un exercice

paramètres :
	{
		"id" : 14
	}
	
réponse en cas de succes (200): 
	{
		id : "14",
		"title" : "Hello World en C",
		"author" : "Serginho-kun",
		"language" : "C",
		"instruction" : "Ecrire un Hello World en C"
	}	
Si l'id n'as pas été trouvé (404):

{
	"error": "Exercice not found."
}

	
## GET: /exercice/comment
renvoi les commentaires d'un exercice

paramètres :
	{
		"exercice_id" : 64
	}

réponse en cas de succes (200): 
	[
		{
			"content": "contenu du commentaire",
			"author": "kevin13",
		}	
	]			
	
Si l'id n'as pas été trouvé (404):

	{
		"error": "Course not found."
	}

## GET: /exercice/correction
renvoie la correction d'un cours.

paramètres :
	{
		"exercice_id" : 55,
		"token" : 1234567789ABCDEF
	}

réponse en cas de succes (200): 
	{
		"id" : 12
		"exercice_id": 2113,
		"content": "Contenu du script"		
	}		
	
En cas de permissions insuffisantes (401):

	{
	    "error": "You’re not allowed to see this."
	}
	
## GET: /exercice/user_code
renvoie le code d'un exercice par un utilisateur.

paramètres:
	{
		"exercice_id" : 12,
		"author_id" : 23,
		"token" : 1234567789ABCDEF
	}

réponse en cas de succes (200): 
	{
		"account_id": 42,
		"user_exercice_id": 69,
		"content" : "code code code",
	}		

## GET: /exercice
renvoie un exercice

paramètres :
	{
		"id" : 14
	}
	
réponse en cas de succes (200): 
	{
		"title": "Do a Hello World",
		"instruction" : "print a Hello World ….",
		"author" : "kevin13",
	}	
	
Si l'id n'as pas été trouvé (404):

	{
		"error": "Exercice not found."
	}
	
## GET: /blog_post/list
renvoie la liste des post du blog

paramètres :
	{
	}
	
réponse en cas de succes (200):
	[
		{
			"title" : "le C en 29 minutes ne dure parfois pas 29 minutes",
			"content" : "Bla bla bla",
			"creator_id" : "kevin13",
			"blog_category_id" : 2
		}	
	]	
	
## GET: /blog_post/categories
renvoie la listes des categories du blog

paramètres :
	{
	}
	
réponse en cas de succes (200):
	[
		{
			"blog_category_id" : 2,
			"name" : "programmation"
		}	
	]		

## GET: /blog_post/comment
renvoie la listes des commentaire d'un post

paramètres :
	{
		"id" : 74
	}

réponse en cas de succes (200): 
	[
		{
			"title" : "Tu m’as ouvert les yeux",
			"content" : "Bla bla bla",
			"creator_id" : "kevin13"
		}	
	]	
	
## GET: /forum/forum
renvoie la liste des forums
paramètres :
	{
	}
	
réponse en cas de succes (200):
	[
		{
			"id" : 2,
			"name" : "aide aux exercices",
			"description" : "ici, demandez de l'aide en rapport aux exercices de C&L",			
		}
	]
	
## GET: /forum/subject
renvoie les sujets du forum.

paramètres :
	{
		"id" : 12
	}
	
réponse:
	[
		{
			"name": "sujet",
			"date" : "1454215520",
			"replies" : 49,
			"views" : (?)
		}
	]
	
	
## GET: /forum/categories
renvoie la liste des categories d'un forum
paramètres :
	{
		"id_forum" : 4,		
	}
	
réponse en cas de succes (200):
	[
		{	
			"id" : 2,
			"name" : "C"
		}
	]
	
## GET: /forum/posts
renvoie la liste des post d'un sujet
paramètres :
	{
		"id_subject" : 4
		"token" : "1234567789ABCDEF"
	}

réponses en cas de succes (200) :
	[
		{		
			"author" : "Serginho-kun",
			"content" : "Je n'arrive pas à utiliser printf, ki pe m'aider ?",
			"date" : "1454215520",
			"likes" : 0
		}
	]

En cas de permissions insuffisantes (401):

	{
	    "error": "You’re not allowed to see this."
	}	
	