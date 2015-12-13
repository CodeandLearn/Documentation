Références PUT 
==============

En cas de succès, le code 200 sera renvoyé.

## PUT: /account

Update les informations du comptes.

Paramètres:

	{
		"username": "kevin13",
		"email": "new@gmail.com",
		"password": "newpassword1",
		"token": "123456789ABCDEF"
	}

## PUT: /course

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

Mettre à jour un script de vérification.

Paramètres:

	{
		"exercice_id": 2113,
		"content": "Contenu du script",
		"token": "123456789ABCDEF"
	}

## PUT: /blog/post

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

Mettre à jour le nom du forum.

Paramètres:

	{
		"id": 1,
		"name": "new_name",
		"token": "123456789ABCDEF"
	}

## PUT: /forum/category

Mettre à jour le nom de la categorie.

Paramètres:

	{
		"id": 1,
		"name": "new category",
		"token": "123456789ABCDEF"
	}


## PUT: /forum/post

Mettre à jour un message du forum.

Paramètres:

	{
		"id": 1,
		"token": "123456789ABCDEF"
	}
