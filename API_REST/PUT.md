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