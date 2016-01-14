En cas de succès, un code 200 sera retourné.

Référence DELETE
----------------

## DELETE /account
supprimer un compte

paramètres :

    {
     "id" : 1
     "username" : "Serginho-kun"
     "email": "kikoolol64@gmail.com"
      "token" : "123456789ABCDEF"
    }

## DELETE /groups
supprimer un groupe

paramètres :

    {
     "id": 2
     "token" : "123456789ABCDEF"
    }

## DELETE /course
supprimer un cours

paramètres :

    {
     "id" : 2
      "token" : "123456789ABCDEF"
    }

## DELETE /course/comment
supprimer un commentaire d’un cours

paramètres :

    {
     "id" : 2
      "token" : "123456789ABCDEF"
    }

## DELETE /exercice
supprimer un exercice

paramètres :

    {
    "id": 12
    "script_id": 12
     "token" : "123456789ABCDEF"
    }

## DELETE /exercice/comment
Supprimer le commentaire d’un exercice

paramètres :

    {
    "id": 1
    "exercice_id": 12
    }

## DELETE /blog/post
Supprimer un post sur le blog

paramètres :

    {
     "id": 54
      "token" : "123456789ABCDEF"
    }

    DELETE /blog/category

Supprimer une categorie du blog

paramètres :

    {
     "id": 1
      "token" : "123456789ABCDEF"
    }

## DELETE /blog/comment
Supprimer un commentaire d’un post sur le blog

paramètres:

    {
     "id" : 1
     "blog_post_id" : 54
    }

## DELETE /forum/post
Supprimer un message sur le forum

paramètres :

    {
     "id" : 21
      "token" : "123456789ABCDEF"
    }

## DELETE /forum/category
Supprimer une catégorie du forum

paramètres :

    {
     "id" : 1
     "token" : "123456789ABCDEF"
    }