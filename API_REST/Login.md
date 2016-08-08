# Login
## Récupération d'un token
### Requête `/oauth` méthode `POST`
Pour créer l'authorisation il suffit d'encoder `username:password` en base64.

Ex : `test:secret` encodé en base64 donne `dGVzdDpzZWNyZXQ=`

Header d'envoi :
```
  Content-Type : application/json
  Authorization : Basic dGVzdDpzZWNyZXQ=
```
Réception JSON :
```
{
  "code": 200,
  "method": "POST",
  "token_type": "bearer",
  "error": "OK",
  "access_token": "bal0o08s5rsulmdu3qsrg1lgej",
  "path": "/oauth",
  "scope": "read/write",
  "expires_in": 1470673283336,
  "group": 50,
  "timestamp": 1470666083288
}
```

### Requête `/revoke` méthode `DELETE`
Permet de supprimer le token actuel

Header d'envoi :
```
  Content-Type : application/json
  Authorization : Basic dGVzdDpzZWNyZXQ=
```
Réception JSON :
```
{
  "path": "/revoke",
  "code": 200,
  "method": "DELETE",
  "scope": "read/write",
  "token_type": "bearer",
  "error": "OK",
  "timestamp": 1470666025415
}
```

### Ex de requête `/blog` méthode `GET`
Header :
```
  Content-Type : application/json
  Authorization : Bearer 193590b7-80b3-43b1-932b-c2df7b891d73
```
Réception JSON :
```
{
  "timestamp": 1460657635548,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog",
  "data": [
    {
      "article": {
        "id": 5,
        "account_id": 1,
        "locales_id": 1,
        "blog_category_id": 1,
        "title": "test d'insertion 3",
        "content": "ceci est un troisième 'test' d'insertion depuis l'api",
        "create_timestamp": 1460107216526,
        "modify_timestamp": 1460107216526,
        "account": {
          "id": 1,
          "username": "test",
          "group": {
            "id": 1,
            "name": "membre",
            "parent_id": 1
          },
          "avatar": {
            "id": 1,
            "path": "http://www.canopsis.com/wp-content/uploads/2013/11/brick-default.png"
          }
        },
        "locale": {
          "id": 1,
          "name": "fr"
        },
        "category": {
          "id": 1,
          "name": "test"
        }
      }
    },
    {
      "article": {
        "id": 4,
        "account_id": 1,
        "locales_id": 1,
        "blog_category_id": 1,
        "title": "test d'insertion bis",
        "content": "ceci est un deuxième 'test' d'insertion depuis l'api",
        "create_timestamp": 1460107201099,
        "modify_timestamp": 1460107201099,
        "account": {
          "id": 1,
          "username": "test",
          "group": {
            "id": 1,
            "name": "membre",
            "parent_id": 1
          },
          "avatar": {
            "id": 1,
            "path": "http://www.canopsis.com/wp-content/uploads/2013/11/brick-default.png"
          }
        },
        "locale": {
          "id": 1,
          "name": "fr"
        },
        "category": {
          "id": 1,
          "name": "test"
        }
      }
    },
    {
      "article": {
        "id": 3,
        "account_id": 1,
        "locales_id": 1,
        "blog_category_id": 1,
        "title": "test",
        "content": "test de content",
        "create_timestamp": 1455450486873,
        "modify_timestamp": 1455450486873,
        "account": {
          "id": 1,
          "username": "test",
          "group": {
            "id": 1,
            "name": "membre",
            "parent_id": 1
          },
          "avatar": {
            "id": 1,
            "path": "http://www.canopsis.com/wp-content/uploads/2013/11/brick-default.png"
          }
        },
        "locale": {
          "id": 1,
          "name": "fr"
        },
        "category": {
          "id": 1,
          "name": "test"
        }
      }
    },
    {
      "article": {
        "id": 2,
        "account_id": 1,
        "locales_id": 1,
        "blog_category_id": 2,
        "title": "gfsdgdsfg",
        "content": "sgfdshhfdhsdfh",
        "create_timestamp": 1455450486873,
        "modify_timestamp": 1455450486873,
        "account": {
          "id": 1,
          "username": "test",
          "group": {
            "id": 1,
            "name": "membre",
            "parent_id": 1
          },
          "avatar": {
            "id": 1,
            "path": "http://www.canopsis.com/wp-content/uploads/2013/11/brick-default.png"
          }
        },
        "locale": {
          "id": 1,
          "name": "fr"
        },
        "category": {
          "id": 2,
          "name": "test 3"
        }
      }
    },
    {
      "article": {
        "id": 1,
        "account_id": 1,
        "locales_id": 1,
        "blog_category_id": 1,
        "title": "test d'insertion (modifié)",
        "content": "ceci est un test d'insertion depuis l'api",
        "create_timestamp": 1455450486873,
        "modify_timestamp": 1460201153567,
        "account": {
          "id": 1,
          "username": "test",
          "group": {
            "id": 1,
            "name": "membre",
            "parent_id": 1
          },
          "avatar": {
            "id": 1,
            "path": "http://www.canopsis.com/wp-content/uploads/2013/11/brick-default.png"
          }
        },
        "locale": {
          "id": 1,
          "name": "fr"
        },
        "category": {
          "id": 1,
          "name": "test"
        }
      },
      "comments": [
        {
          "id": 1,
          "content": "test",
          "create_timestamp": 1455451097541,
          "modify_timestamp": 1455451097541,
          "user": {
            "id": 1,
            "username": "test",
            "group": {
              "id": 1,
              "name": "membre",
              "parent_id": 1
            },
            "avatar": {
              "id": 1,
              "path": "http://www.canopsis.com/wp-content/uploads/2013/11/brick-default.png"
            }
          }
        }
      ]
    }
  ]
}
```