Références PUT 
==============

En cas de succès, le code 200 sera renvoyé.

<<<<<<< HEAD
**PUT /account**
=======
## PUT: /account

>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Update les informations du comptes.

Paramètres:

	{
		"username": "kevin13",
		"email": "new@gmail.com",
		"password": "newpassword1",
<<<<<<< HEAD
		"token" : "123456789ABCDEF"
    }
**PUT /course**
=======
		"token": "123456789ABCDEF"
	}

## PUT: /course

>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Mettre à un jour un cours.

Paramètres:

	{
		"title": "Le C en 29 minutes",
		"content": "Bla bla bla",
		"creator_id": "kevin13",
		"user token": "123456789ABCDEF",
		"language": "C"
	}

## PUT: /exercice

<<<<<<< HEAD
**PUT /exercice**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Mettre à jour un exercice.

Paramètres:

	{
		"content": "contenu du commentaire",
		"author": "kevin13",
		"author_id": 42,
		"user_token": "123456789ABCDEF",
		"exercice_id": 2113,
		"timestamp": 12569537329
	}

## PUT: /exercice/script

<<<<<<< HEAD
**PUT /exercice/script**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Mettre à jour un script de vérification.

Paramètres:

	{
		"exercice_id": 2113,
		"content": "Contenu du script",
<<<<<<< HEAD
		"token" : "123456789ABCDEF"
    }
**PUT /blog/post**
=======
		"token": "123456789ABCDEF"
	}

## PUT: /blog/post

>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Mettre à jour un post du blog.

Paramètres:

	{
		"id": 0,
		"title": "Pourquoi j’aime les chinoises",
		"content": "Bla bla bla",
		"creator_id": "kevin13",
		"user_token": "123456789ABCDEF",
		"blog_category_id": 2,
		"token": "123456789ABCDEF"
	}

## PUT: /forum

<<<<<<< HEAD
**PUT /forum**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Mettre à jour le nom du forum.

Paramètres:

	{
		"id": 1,
		"name": "new_name",
		"token": "123456789ABCDEF"
	}

## PUT: /forum/category

<<<<<<< HEAD
**PUT /forum/category**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Mettre à jour le nom de la categorie.

Paramètres:

	{
		"id": 1,
		"name": "new category",
		"token": "123456789ABCDEF"
	}


## PUT: /forum/post

<<<<<<< HEAD
**PUT /forum/post**
=======
>>>>>>> 7d8db6c0e6a36be05c57ec91f95323f172de51c0
Mettre à jour un message du forum.

Paramètres:

	{
		"id": 1,
		"token": "123456789ABCDEF"
	}
