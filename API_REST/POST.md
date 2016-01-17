Références POST
===============

En cas de succès, un code 201 sera retourné. En cas d’erreur de permission, le code 401 sera retourné

<<<<<<< HEAD
**POST /login/**
=======
## POST: /login

>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Prend le pseudo et le mot de passe en paramètre.

Paramètres:

	{
		 "username": "kevin13",
		 "Password": "123456789"
	}

Réponse en cas de succes:

	{
		"token": "123456789ABCDEF"
	}

En cas de pseudo non reconnu: 

	{
		"error": "No such user name in the website"
	}

En cas de mauvais mot de passe:

	{
		"error": "Bad Password"
	}

## POST: /account/register

<<<<<<< HEAD
**POST /account/register**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Créer un compte.

Paramètres:

	{
		"username": "kevin13",
		"Password": "123456789",
		"email": "example@mail.com",
		"group": "regular"
	}

Réponse en cas de succès 

	{
		"code": 201
	}

Réponse en cas d’email déjà utilisé:

	{
		"error": "this email is already in use"
	}

Réponse en cas de mot de passe pas assez securisé:

	{
		"error": "the password is not good"
	}

## POST: /exercice

<<<<<<< HEAD
**POST /exercice**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Créer un exercice
paramètres:

	{
		"title": "Do a Hello World",
		"instruction": "print a Hello World ….",
		"author": "kevin13",
		"user_token": "123456789ABCDEF",
		"max_grade": 20,
		"token": "123456789ABCDEF"
	}

## POST: /exercice/comment

<<<<<<< HEAD
**POST /exercice/comment**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Commenter un exercice

paramètres:

	{
		"content": "contenu du commentaire",
		"author": "kevin13",
		"author_id": 42,
		"user_token": "123456789ABCDEF",
		"exercice_id": 2113,
		"timestamp": 12569537329
	}

<<<<<<< HEAD
**POST /exercice/script**
=======
## POST: /exercice/script
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Créer un script de verification pour un exercice.

paramètres:

	{
		"exercice_id": 2113,
		"content": "Contenu du script",
		"token": "123456789ABCDEF",
	}

<<<<<<< HEAD
**POST /exercice/correction**
=======
## POST: /exercice/correction
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
écrire une correction

paramètres:

	{
		"exercice_id":2113,
		"correction": "Helloworld!\n",
		"token": "123456789ABCDEF"
	}

## POST: /exercice/save_code

<<<<<<< HEAD
**POST /exercice/save_code**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Sauvegarde le code l’utilisateur sur un exercice.

Paramètres:

	{
		"account_id": 42,
		"user_exercice_id": 69,
		"user_token": "123456789ABCDEF",
		"content": "code code code",
		"exercice_id": 2113,
	}

<<<<<<< HEAD
**POST /course**
=======
## POST: /course
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Créer un cours. 

paramètres:

	{
		"title": "Le C en 29 minutes",
		"content": "Bla bla bla",
		"creator_id": "kevin13",
		"token": "123456789ABCDEF",
		"language": "C"
	}

en réponse en cas de duplication :

	{
		"error": "A lesson has already this title."
	}

en cas d’erreur de token:

	{
		"error": "bad token"
	}

En cas de permission pas suffisantes le code erreur 403 et le message suivant:

	{
		"error": "you don’t have the permission to do that."
	}


<<<<<<< HEAD
**POST /course/comment**
=======
## POST: /course/comment

>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Commenter un cours. 

Paramètres:

	{
		"title": "à revoir",
		"content": "Bla bla bla",
		"creator_id": "kevin13",
		"lesson_id": 42,
		"token": "123456789ABCDEF",
		"timestamp": 125695373290
	}

en cas d’erreur de token:

	{
		"error": "bad token"
	}

dans le cas où l’utilisateur n’as pas de permission adequate:

	{
		"error": "you don’t have the permission to do that."
	}

<<<<<<< HEAD
**POST /blog/post**
=======
## POST:  /blog/post
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Créer un post sur le blog.

Paramètres:

<<<<<<< HEAD
    {
		"title" : "le C en 29 minutes ne dure parfois pas 29 minutes",
		"content" : "Bla bla bla",
		"creator_id" : "kevin13",
		"token" : "123456789ABCDEF",
		"blog_category_id" : 2
    }
=======
	{
		"title": "le C en 29 minutes ne dure parfois pas 29 minutes",
		"content": "Bla bla bla",
		"creator_id": "kevin13",
		"token": "123456789ABCDEF",
		"blog_category_id": 2
	}
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0

en cas d’erreur de token:

	{
		"error": "bad token"
	}

en cas d’erreur d’authorisation:

	{
		"error": "you don’t have the permission to do that.
	}

## POST: /blog/comment_post

<<<<<<< HEAD
**POST /blog/comment_post**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Poster un commentaire à un article.

 paramètres:

	{
		"title": "Tu m’as ouvert les yeux",
		"content": "Bla bla bla",
		"creator_id": "kevin13",
		"token": "123456789ABCDEF"
	}

en cas d'erreur de token:

	{
		"error": "bad token"
	}

## POST: /forum/forum

<<<<<<< HEAD
**POST /forum/forum**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Créer une un forum.

Paramètres:

	{
		"nom": "forum d’aide au language C",
		"groups": "all",
		"token": "123456789ABCDEF"
	}


## POST: /forum/subject

<<<<<<< HEAD
**POST /forum/subject**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
créer un sujet sur le forum.

paramètres: 

	{
		"author_id": 42,
		"timestamp": 12569537329,
		"name": "Problème printf",
		"content": "",
		"token": "123456789ABCDEF",
	}

## POST: /forum/post

<<<<<<< HEAD
**POST  /forum/post**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Ecrire un message sur le forum.

Paramètres: 

	{
		"author": "kevin13",
		"author_id": 42,
		"name": "aide en C",
		"description": "ici toute vos question en rapport au langage C",
		"token": "123456789ABCDEF"
	}
