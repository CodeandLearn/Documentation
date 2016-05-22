# Blog
```
	Content-Type : application/json
	Authorization : Bearer <token d'autorisation voir login>
```
## GET - R�cup�ration
### Requ�te `/blog` m�thode `GET`
R�ception JSON :
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
        "content": "ceci est un troisi�me 'test' d'insertion depuis l'api",
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
        "content": "ceci est un deuxi�me 'test' d'insertion depuis l'api",
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
        "title": "test d'insertion (modifi�)",
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
### Requ�te `/blog/limit/{limit}` m�thode `GET`
R�ception JSON pour une limite de `1` :
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
        "content": "ceci est un troisi�me 'test' d'insertion depuis l'api",
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
### Requ�te `/blog/author/{author_name}` m�thode `GET`
R�ception JSON pour l'auteur `test`:
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
        "content": "ceci est un troisi�me 'test' d'insertion depuis l'api",
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
        "content": "ceci est un deuxi�me 'test' d'insertion depuis l'api",
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
        "title": "test d'insertion (modifi�)",
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
### Requ�te `/blog/author/id/{author_id}` m�thode `GET`
R�ception JSON pour l'auteur d'id `1` :
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
        "content": "ceci est un troisi�me 'test' d'insertion depuis l'api",
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
        "content": "ceci est un deuxi�me 'test' d'insertion depuis l'api",
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
        "title": "test d'insertion (modifi�)",
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
### Requ�te `/blog/category/{category_name}` m�thode `GET`
R�ception JSON pour la categorie `test 3` :
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
### Requ�te `/blog/category/id/{category_id}` m�thode `GET`
R�ception JSON pour la categorie d'id `2` :
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
### Requ�te `/blog/{post_id}` m�thode `GET`
R�ception JSON pour le post d'id `1` :
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
        "title": "test d'insertion (modifi�)",
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
### Requ�te `/blog/categories` m�thode `GET`
R�ception JSON :
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
### Requ�te `/blog/comments` m�thode `GET`
R�ception JSON :
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
### Requ�te `/blog/comments/limit/{limit}` m�thode `GET`
R�ception JSON pour une limite de `1`:
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
### Requ�te `/blog/comment/{id}` m�thode `GET`
R�ception JSON d'id `1` :
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
### Requ�te `/blog/comment/post/{post_id}` m�thode `GET`
R�ception JSON du post d'id `1`:
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
### Requ�te `/blog/comment/author/{author_name}` m�thode `GET`
R�ception JSON de l'auteur `test` :
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
### Requ�te `/blog/comment/author/id/{author_id}` m�thode `GET`
R�ception JSON de l'id d'auteur `1` :
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

## POST - Cr�ation
### Requ�te `/blog` m�thode `POST`
JSON � envoyer :
```
{
    "locales_id": 1,
    "blog_category_id": 1,
    "title": "test d'insertion",
    "content": "ceci est un test d'insertion depuis l'api"
}
```
### Requ�te `/blog/category` m�thode `POST`
JSON � envoyer :
```
{
	"name": "titre d'une cat�gorie"
}
```
### Requ�te `/blog/comment` m�thode `POST`
JSON � envoyer :
```
{
    "blog_post_id": 1,
    "content": "contenue d'un commentaire"
}
```

## PUT - Modification
### Requ�te `/blog/{id}` m�thode `PUT`
JSON � envoyer :
```
{
    "locales_id": 1,
    "blog_category_id": 1,
    "title": "test d'insertion",
    "content": "ceci est un test de modification depuis l'api"
}
```
### Requ�te `/blog/category/{id}` m�thode `PUT`
JSON � envoyer :
```
{
	"name": "titre d'une cat�gorie modifi�"
}
```
### Requ�te `/blog/comment/{id}` m�thode `PUT`
JSON � envoyer :
```
{
    "blog_post_id": 1,
    "content": "contenue d'un commentaire modifi�"
}
```

## DELETE - Suppression
### Requ�te `/blog/{id}` m�thode `DELETE`
### Requ�te `/blog/category/{id}` m�thode `DELETE`
### Requ�te `/blog/comment/{id}` m�thode `DELETE`