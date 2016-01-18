Référence DELETE
================

En cas de succès, un code 200 sera retourné.

## DELETE: /account

Supprimer un compte.

Paramètres :

	{
		"id": 1,
		"username": "kevin13",
		"email": "example@email.com",
		"token": "123456789ABCDEF"
	}

## DELETE: /groups

Supprimer un groupe.

Paramètres :

	{
		"id": 2,
		"token": "123456789ABCDEF"
	}

## DELETE/course

Supprimer un cours.

Paramètres :

	{
		"id": 2,
		"token": "123456789ABCDEF"
	}

## DELETE: /course/comment

Supprimer un commentaire d’un cours.

Paramètres :

	{
		"id": 2,
		"token": "123456789ABCDEF"
	}

## DELETE: /exercice

Supprimer un exercice.

Paramètres :

	{
		"id": 12,
		"script_id": 12,
		"token": "123456789ABCDEF"
	}

## DELETE: /exercice/comment

Supprimer le commentaire d’un exercice.

Paramètres :

	{
		"id": 1,
		"exercice_id": 12
	}

## DELETE: /blog/post

Supprimer un post sur le blog.

Paramètres :

	{
		"id": 54,
		"token": "123456789ABCDEF"
	}

## DELETE: /blog/category


Supprimer une categorie du blog.

Paramètres :

	{
		"id": 1,
		"token": "123456789ABCDEF"
	}

## DELETE: /blog/comment

Supprimer un commentaire d’un post sur le blog.

Paramètres:

	{
		"id": 1,
		"blog_post_id": 54,
		"token": "123456789ABCDEF"
	}

## DELETE: /forum/post
Supprimer un message sur le forum.

Paramètres :

	{
		"id": 21,
		"token": "123456789ABCDEF"
	}

## DELETE: /forum/category

Supprimer une catégorie du forum.

Paramètres :

	{
		"id": 1,
		"token": "123456789ABCDEF"
	}
