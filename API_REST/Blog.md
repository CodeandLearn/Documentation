# Blog
```
	Content-Type : application/json
	Authorization : Bearer <token d'autorisation voir login>
```
## GET - Récupération
### Requête `/blog` méthode `GET`
Réception JSON :
```
{
  "timestamp": 1460622340168,
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
### Requête `/blog/limit/{limit}` méthode `GET`
Réception JSON pour une limite de `1` :
```
{
  "timestamp": 1460622518095,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/limit/1",
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
    }
  ]
}
```
### Requête `/blog/author/{author_name}` méthode `GET`
Réception JSON pour l'auteur `test`:
```
{
  "timestamp": 1460622618056,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/author/test",
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
### Requête `/blog/author/id/{author_id}` méthode `GET`
Réception JSON pour l'auteur d'id `1` :
```
{
  "timestamp": 1460622673033,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/author/id/1",
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
### Requête `/blog/category/{category_name}` méthode `GET`
Réception JSON pour la categorie `test 3` :
```
{
  "timestamp": 1460622751584,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/category/test 3",
  "data": [
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
    }
  ]
}
```
### Requête `/blog/category/id/{category_id}` méthode `GET`
Réception JSON pour la categorie d'id `2` :
```
{
  "timestamp": 1460622792497,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/category/id/2",
  "data": [
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
    }
  ]
}
```
### Requête `/blog/{post_id}` méthode `GET`
Réception JSON pour le post d'id `1` :
```
{
  "timestamp": 1460622830489,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/1",
  "data": [
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
### Requête `/blog/categories` méthode `GET`
Réception JSON :
```
{
  "timestamp": 1460622873024,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/categories",
  "data": [
    {
      "id": 3,
      "name": "test bis"
    },
    {
      "id": 2,
      "name": "test 3"
    },
    {
      "id": 1,
      "name": "test"
    }
  ]
}
```
### Requête `/blog/comments` méthode `GET`
Réception JSON :
```
{
  "timestamp": 1460622885483,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/comments",
  "data": [
    {
      "id": 1,
      "account_id": 1,
      "blog_post_id": 1,
      "content": "test",
      "create_timestamp": 1455451097541,
      "modify_timestamp": 1455451097541,
      "user": {
        "id": 1,
        "username": "test",
        "group_id": 1,
        "avatar_id": 1,
        "create_timestamp": 1455450486873,
        "last_connect_timestamp": 1455450486873,
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
```
### Requête `/blog/comments/limit/{limit}` méthode `GET`
Réception JSON pour une limite de `1`:
```
{
  "timestamp": 1460622900380,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/comments/limit/1",
  "data": [
    {
      "id": 1,
      "account_id": 1,
      "blog_post_id": 1,
      "content": "test",
      "create_timestamp": 1455451097541,
      "modify_timestamp": 1455451097541,
      "user": {
        "id": 1,
        "username": "test",
        "group_id": 1,
        "avatar_id": 1,
        "create_timestamp": 1455450486873,
        "last_connect_timestamp": 1455450486873,
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
```
### Requête `/blog/comment/{id}` méthode `GET`
Réception JSON d'id `1` :
```
{
  "timestamp": 1460622925900,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/comment/1",
  "data": [
    {
      "id": 1,
      "account_id": 1,
      "blog_post_id": 1,
      "content": "test",
      "create_timestamp": 1455451097541,
      "modify_timestamp": 1455451097541,
      "user": {
        "id": 1,
        "username": "test",
        "group_id": 1,
        "avatar_id": 1,
        "create_timestamp": 1455450486873,
        "last_connect_timestamp": 1455450486873,
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
```
### Requête `/blog/comment/post/{post_id}` méthode `GET`
Réception JSON du post d'id `1`:
```
{
  "timestamp": 1460622971243,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/comment/post/1",
  "data": [
    {
      "id": 1,
      "account_id": 1,
      "blog_post_id": 1,
      "content": "test",
      "create_timestamp": 1455451097541,
      "modify_timestamp": 1455451097541,
      "user": {
        "id": 1,
        "username": "test",
        "group_id": 1,
        "avatar_id": 1,
        "create_timestamp": 1455450486873,
        "last_connect_timestamp": 1455450486873,
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
```
### Requête `/blog/comment/author/{author_name}` méthode `GET`
Réception JSON de l'auteur `test` :
```
{
  "timestamp": 1460623010802,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/comment/author/test",
  "data": [
    {
      "id": 1,
      "account_id": 1,
      "blog_post_id": 1,
      "content": "test",
      "create_timestamp": 1455451097541,
      "modify_timestamp": 1455451097541,
      "user": {
        "id": 1,
        "username": "test",
        "group_id": 1,
        "avatar_id": 1,
        "create_timestamp": 1455450486873,
        "last_connect_timestamp": 1455450486873,
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
```
### Requête `/blog/comment/author/id/{author_id}` méthode `GET`
Réception JSON de l'id d'auteur `1` :
```
{
  "timestamp": 1460623039686,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/blog/comment/author/id/1",
  "data": [
    {
      "id": 1,
      "account_id": 1,
      "blog_post_id": 1,
      "content": "test",
      "create_timestamp": 1455451097541,
      "modify_timestamp": 1455451097541,
      "user": {
        "id": 1,
        "username": "test",
        "group_id": 1,
        "avatar_id": 1,
        "create_timestamp": 1455450486873,
        "last_connect_timestamp": 1455450486873,
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
```

## POST - Création
### Requête `/blog` méthode `POST`
JSON à envoyer :
```
{
    "locales_id": 1,
    "blog_category_id": 1,
    "title": "test d'insertion",
    "content": "ceci est un test d'insertion depuis l'api"
}
```
### Requête `/blog/category` méthode `POST`
JSON à envoyer :
```
{
	"name": "titre d'une catégorie"
}
```
### Requête `/blog/comment` méthode `POST`
JSON à envoyer :
```
{
    "blog_post_id": 1,
    "content": "contenue d'un commentaire"
}
```

## PUT - Modification
### Requête `/blog/{id}` méthode `PUT`
JSON à envoyer :
```
{
    "locales_id": 1,
    "blog_category_id": 1,
    "title": "test d'insertion",
    "content": "ceci est un test de modification depuis l'api"
}
```
### Requête `/blog/category/{id}` méthode `PUT`
JSON à envoyer :
```
{
	"name": "titre d'une catégorie modifié"
}
```
### Requête `/blog/comment/{id}` méthode `PUT`
JSON à envoyer :
```
{
    "blog_post_id": 1,
    "content": "contenue d'un commentaire modifié"
}
```

## DELETE - Suppression
### Requête `/blog/{id}` méthode `DELETE`
### Requête `/blog/category/{id}` méthode `DELETE`
### Requête `/blog/comment/{id}` méthode `DELETE`