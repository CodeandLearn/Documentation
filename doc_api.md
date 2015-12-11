
Références POST
---------------

En cas de succès, un code 201 sera retourné. En cas d’erreur de permission, le code 401 sera retourné

## POST: /login/
Prend le pseudo et le mot de passe en paramètre.

Paramètres :

    {
     "username" : "Serginho-kun"
     "Password" : "123456789"
    }

reponse en cas de succes :

    {
    "token" : "123456789ABCDEF"
    }

en cas de pseudo non reconnu: 

    {
    "error": "No such pseudo in the website"
    }

en cas de mauvais mot de passe

    {
    "error" : "Bad Password"
    }

**POST /account/register**
Créer un compte.

    {
     "username" : "Serginho-kun"
     "Password": "123456789"
     "email" : "kikoolol64@gmail.com"
     "group" : "regular"
    }

réponse en cas de succès 

    {
     "code": 201
    }

réponse en cas d’email déjà utilisé le code HTTP 409 et :

    {
    "error": "this email is already in use"
    }

réponse en cas de mot de passe pas assez securisé :

    {
    "error": "the password is not good"
    }

## POST /exercice
créer un exercice
paramètres :

    {
    "title": "Do a Hello World"
    "instruction" : "print a Hello World …."
    "author" : "Serginho_kun"
    "user_token" : "123456789ABCDEF"
    "max_grade": 20
     "token" : "123456789ABCDEF"
    }

## POST /exercice/comment
Commenter un exercice

paramètres :

    {
    "content": "contenu du commentaire"
    "author": "Serginho_kun"
    "author_id": 42
    "user_token" : "123456789ABCDEF"
    "exercice_id" : 2113
    "timestamp": 12569537329
    }

## POST /exercice/script
Créer un script de verification pour un exercice

paramètres :

    {
    "exercice_id": 2113
    "content": "Contenu du script"
    "token" : "123456789ABCDEF"
    }

## POST /exercice/correction
écrire une correction

paramètres :

    {
      "exercice_id":2113
      "correction": "Helloworld!\n"
      "token" : "123456789ABCDEF"
     }

## POST /exercice/save_code
Sauvegarde le code l’utilisateur sur un exercice

paramètres :

    {
     "account_id": 42
     "user_exercice_id": 69
     "user_token" : "123456789ABCDEF"
     "content" : "code code code"
     "exercice_id" : 2113
    }

## POST /course
Créer un cours. 

paramètres :

    {
     "title" : "Le C en 29 minutes"
     "content" : "Bla bla bla"
     "creator_id" : "Serginho-kun"
     "token" : "123456789ABCDEF"
     "language" : "C"
     }

en réponse en cas de duplication  :

    {
     "error": "a lesson has already this title"
    }

en cas d’erreur de token :

    {
    "error": "bad token"
    }

En cas de permission pas suffisantes :

    {
    "error": "you don’t have the permission to do that."
    }


## POST /course/comment
Commenter un cours. 

paramètres :

    {
     "title" : "à revoir"
     "content" : "Bla bla bla"
     "creator_id" : "Serginho-kun"
     "lesson_id" : 42
     "token" : "123456789ABCDEF"
     "timestamp": 125695373290
    }

en cas d’erreur de token :

    {
    "error": "bad token"
    }

dans le cas où l’utilisateur n’as pas de permission adequate:

    {
    "error": "you don’t have the permission to do that."
    }

## POST /blog/post
Créer un post sur le blog.

Paramètres:

    {
     "title" : "Pourquoi j’aime les chinoises"
     "content" : "Bla bla bla"
     "creator_id" : "Serginho-kun"
     "token" : "123456789ABCDEF"
     blog_category_id : 2
    }

en cas d’erreur de token :

    {
    "error": "bad token"
    }

en cas d’erreur d’authorisation :

    {
    "error": "you don’t have the permission to do that.
    }

**POST /blog/comment_post**
poster un commentaire à un article

 paramètres :

    {
     "title" : "Tu m’as ouvert les yeux"
     "content" : "Bla bla bla"
     "creator_id" : "Serginho-kun"
     "token" : "123456789ABCDEF"
    }

en cas d'erreur de token

    {
    "error": "bad token"
    }

## POST /forum/forum
Créer une un forum

paramètres :

    {
     "nom" : "forum d’aide au language C"
     "groups" : "all"
     "token": "123456789ABCDEF"
    }


## POST /forum/subject
créer un sujet sur le forum

paramètres : 

    {
     "author_id" : 42
     "timestamp": 12569537329
     "name": "Problème printf"
     "content": ""
      "token" : "123456789ABCDEF"
    }

## POST  /forum/post
écrire un message sur le forum

paramètres : 

    {
     "author": "Serginho-kun"
     "author_id" : 42
     "name": "aide en C"
     "description": "ici toute vos question en rapport au langage C"
      "token" : "123456789ABCDEF"
    }




Références PUT
--------------

En cas de succès, le code 200 sera renvoyé.

## PUT /account
Update les informations du comptes

paramètres :

    {
     "username": Serginho-kun
     "email": "new@gmail.com"
     "password": "newpassword1"
     "token" : "123456789ABCDEF"
    }

## PUT /course
mettre à un jour un cours

Paramètres :

    {
     "title" : "Le C en 29 minutes"
     "content" : "Bla bla bla"
     "creator_id" : "Serginho-kun"
     "user token" : "123456789ABCDEF"
     "language" : "C"
    }

## PUT /exercice
mettre à jour un exercice

paramètres :

    {
    "content": "contenu du commentaire"
    "author": "Serginho_kun"
    "author_id": 42
    "user_token" : "123456789ABCDEF"
    "exercice_id" : 2113
    "timestamp": 12569537329
    }

## PUT /exercice/script
mettre à jour un script de vérification

paramètres :

    {
    "exercice_id": 2113
    "content": "Contenu du script"
     "token" : "123456789ABCDEF"
    }

## PUT /blog/post
mettre à jour un post du blog

paramètres :

    {
     "id" : 0
     "title" : "Pourquoi j’aime les chinoises"
     "content" : "Bla bla bla"
     "creator_id" : "Serginho-kun"
     "user_token" : "123456789ABCDEF"
     "blog_category_id" : 2
     "token" : "123456789ABCDEF"
    }

## PUT /forum
mettre à jour le nom du forum

paramètres :

    {
     "id": 1
     "name" : "new_name"
     "token" : "123456789ABCDEF"
    }

## PUT /forum/category
mettre à jour le nom de la categorie

paramètres :

    {
     "id": 1
     "name": "new category"
     "token" : "123456789ABCDEF"
    }


## PUT /forum/post
mettre à jour un message du forum

paramètres :

    {
     "id": 1
      "token" : "123456789ABCDEF"
    }
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