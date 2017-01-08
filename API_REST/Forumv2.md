# Forum
## GET - Récupération

Les 3 première routes permettent d'avoir toute les informations nécessaires à l'affichage du forum. `/forum`, `/forum/{id_forum}`, `/forum/subject/{id_subject}`.

### Requête `/forum` méthode `GET`
Récéption JSON :
```
{
  "code": 200,
  "data": [
    {
      "forums": [
        {
          "forum_category_id": 1,
          "icon": {
            "path": "path",
            "id": 1
          },
          "description": "forumdesc",
          "id": 1,
          "position": 1,
          "title": "forum",
          "icon_id": 1,
          "category": {
            "icon": {
              "id": 0
            },
            "id": 0,
            "position": 0,
            "icon_id": 0
          }
        },
        {
          "forum_category_id": 1,
          "icon": {
            "path": "path",
            "id": 1
          },
          "description": "forumdesc",
          "id": 2,
          "position": 2,
          "title": "all",
          "icon_id": 1,
          "category": {
            "icon": {
              "id": 0
            },
            "id": 0,
            "position": 0,
            "icon_id": 0
          }
        },
        {
          "forum_category_id": 1,
          "icon": {
            "path": "path",
            "id": 1
          },
          "description": "forumdesc",
          "id": 3,
          "position": 3,
          "title": "test",
          "icon_id": 1,
          "category": {
            "icon": {
              "id": 0
            },
            "id": 0,
            "position": 0,
            "icon_id": 0
          }
        }
      ],
      "id": 1,
      "title": "cat"
    },
    {
      "forums": [
        {
          "forum_category_id": 2,
          "icon": {
            "path": "path",
            "id": 1
          },
          "description": "forumdesc",
          "id": 4,
          "position": 4,
          "title": "othertest",
          "icon_id": 1,
          "category": {
            "icon": {
              "id": 0
            },
            "id": 0,
            "position": 0,
            "icon_id": 0
          }
        }
      ],
      "id": 2,
      "title": "cat2"
    }
  ],
  "length": 2,
  "error": "OK",
  "timestamp": 1483866728769
}
```
### Requête `/forum/{id_forum}` méthode `GET`
Récéption JSON:
```
{
  "code": 200,
  "data": [
    {
      "forum": {
        "forum_category_id": 0,
        "icon": {
          "id": 0
        },
        "id": 0,
        "position": 0,
        "title": "forum",
        "icon_id": 0,
        "category": {
          "icon": {
            "id": 0
          },
          "id": 0,
          "position": 0,
          "icon_id": 0
        }
      },
      "account_id": 1,
      "pin": false,
      "forum_forum_id": 1,
      "id": 1,
      "title": "TitreSubject",
      "account": {
        "avatar_id": 0,
        "create_timestamp": 0,
        "group_id": 0,
        "last_connect_timestamp": 0,
        "nb_exercises_done": 0,
        "id": 0,
        "avatar": {
          "path": "male.png",
          "id": 0
        },
        "nb_courses_done": 0,
        "username": "admin",
        "group": {
          "parent_id": 0,
          "id": 0
        }
      }
    },
    {
      "forum": {
        "forum_category_id": 0,
        "icon": {
          "id": 0
        },
        "id": 0,
        "position": 0,
        "title": "forum",
        "icon_id": 0,
        "category": {
          "icon": {
            "id": 0
          },
          "id": 0,
          "position": 0,
          "icon_id": 0
        }
      },
      "account_id": 1,
      "pin": false,
      "forum_forum_id": 1,
      "id": 2,
      "title": "TitreSubject",
      "account": {
        "avatar_id": 0,
        "create_timestamp": 0,
        "group_id": 0,
        "last_connect_timestamp": 0,
        "nb_exercises_done": 0,
        "id": 0,
        "avatar": {
          "path": "male.png",
          "id": 0
        },
        "nb_courses_done": 0,
        "username": "admin",
        "group": {
          "parent_id": 0,
          "id": 0
        }
      }
    },
    {
      "forum": {
        "forum_category_id": 0,
        "icon": {
          "id": 0
        },
        "id": 0,
        "position": 0,
        "title": "forum",
        "icon_id": 0,
        "category": {
          "icon": {
            "id": 0
          },
          "id": 0,
          "position": 0,
          "icon_id": 0
        }
      },
      "account_id": 1,
      "pin": false,
      "forum_forum_id": 1,
      "id": 3,
      "title": "TitreSubject",
      "account": {
        "avatar_id": 0,
        "create_timestamp": 0,
        "group_id": 0,
        "last_connect_timestamp": 0,
        "nb_exercises_done": 0,
        "id": 0,
        "avatar": {
          "path": "male.png",
          "id": 0
        },
        "nb_courses_done": 0,
        "username": "admin",
        "group": {
          "parent_id": 0,
          "id": 0
        }
      }
    }
  ],
  "length": 3,
  "error": "OK",
  "timestamp": 1483867022974
}
```
### Requête `/forum/subject/{id_subject}` méthode `GET`
Récéption JSON:
```
{
  "code": 200,
  "data": [
    {
      "account_id": 1,
      "create_timestamp": 1464262190085,
      "subject": {
        "forum": {
          "forum_category_id": 0,
          "icon": {
            "id": 0
          },
          "id": 0,
          "position": 0,
          "icon_id": 0,
          "category": {
            "icon": {
              "id": 0
            },
            "id": 0,
            "position": 0,
            "icon_id": 0
          }
        },
        "account_id": 0,
        "pin": false,
        "forum_forum_id": 0,
        "id": 1,
        "title": "TitreSubject",
        "account": {
          "avatar_id": 0,
          "create_timestamp": 0,
          "group_id": 0,
          "last_connect_timestamp": 0,
          "nb_exercises_done": 0,
          "id": 0,
          "avatar": {
            "id": 0
          },
          "nb_courses_done": 0,
          "group": {
            "parent_id": 0,
            "id": 0
          }
        }
      },
      "modify_timestamp": 1464262190085,
      "id": 1,
      "forum_subject_id": 1,
      "content": "content",
      "account": {
        "avatar_id": 0,
        "create_timestamp": 0,
        "group_id": 0,
        "last_connect_timestamp": 0,
        "nb_exercises_done": 0,
        "id": 1,
        "avatar": {
          "path": "male.png",
          "id": 0
        },
        "nb_courses_done": 0,
        "username": "admin",
        "group": {
          "parent_id": 0,
          "id": 0
        }
      },
      "likes": 2
    },
    {
      "account_id": 1,
      "create_timestamp": 1464262190085,
      "subject": {
        "forum": {
          "forum_category_id": 0,
          "icon": {
            "id": 0
          },
          "id": 0,
          "position": 0,
          "icon_id": 0,
          "category": {
            "icon": {
              "id": 0
            },
            "id": 0,
            "position": 0,
            "icon_id": 0
          }
        },
        "account_id": 0,
        "pin": false,
        "forum_forum_id": 0,
        "id": 1,
        "title": "TitreSubject",
        "account": {
          "avatar_id": 0,
          "create_timestamp": 0,
          "group_id": 0,
          "last_connect_timestamp": 0,
          "nb_exercises_done": 0,
          "id": 0,
          "avatar": {
            "id": 0
          },
          "nb_courses_done": 0,
          "group": {
            "parent_id": 0,
            "id": 0
          }
        }
      },
      "modify_timestamp": 1464262190085,
      "id": 2,
      "forum_subject_id": 1,
      "content": "content2",
      "account": {
        "avatar_id": 0,
        "create_timestamp": 0,
        "group_id": 0,
        "last_connect_timestamp": 0,
        "nb_exercises_done": 0,
        "id": 1,
        "avatar": {
          "path": "male.png",
          "id": 0
        },
        "nb_courses_done": 0,
        "username": "admin",
        "group": {
          "parent_id": 0,
          "id": 0
        }
      },
      "likes": 5
    }
  ],
  "length": 2,
  "error": "OK",
  "timestamp": 1483867051696
}
```
### Requête `/forum/categories` méthode `GET`
Récéption JSON:
```
{
  "path": "/forum/categories",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "icon": {
        "path": "path",
        "id": 1
      },
      "id": 1,
      "position": 1,
      "title": "cat",
      "icon_id": 1
    },
    {
      "icon": {
        "path": "path",
        "id": 1
      },
      "id": 2,
      "position": 2,
      "title": "cat2",
      "icon_id": 1
    }
  ],
  "length": 2,
  "error": "OK",
  "timestamp": 1483868292763
}
```
### Requête `/forum/categories/order/position` méthode `GET`
Récéption JSON:
```
{
  "path": "/forum/categories/order/position",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "icon": {
        "path": "path",
        "id": 1
      },
      "id": 1,
      "position": 1,
      "title": "cat",
      "icon_id": 1
    },
    {
      "icon": {
        "path": "path",
        "id": 1
      },
      "id": 2,
      "position": 2,
      "title": "cat2",
      "icon_id": 1
    }
  ],
  "length": 2,
  "error": "OK",
  "timestamp": 1483868546774
}
```
### Requête `/forum/category/{id_category}` méthode `GET`
Récéption JSON:
```
{
  "path": "/forum/category/{id_category}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "icon": {
        "path": "path",
        "id": 1
      },
      "id": 2,
      "position": 2,
      "title": "cat2",
      "icon_id": 1
    }
  ],
  "length": 1,
  "error": "OK",
  "timestamp": 1483868670128
}
```
### Requête `/forum/icons` méthode `GET`
Récéption JSON:
```
{
  "path": "/forum/icons",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "path": "path",
      "id": 1
    },
    {
      "path": "http://image.flaticon.com/icons/svg/297/297568.svg",
      "id": 2
    }
  ],
  "length": 2,
  "error": "OK",
  "timestamp": 1483875482152
}
```
### Requête `/forum/icon/{id_icon}` méthode `GET`
Récéption JSON:
```
{
  "path": "/forum/icon/{id_icon}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "path": "http://image.flaticon.com/icons/svg/297/297568.svg",
      "id": 2
    }
  ],
  "length": 1,
  "error": "OK",
  "timestamp": 1483875580766
}
```

## POST - Création
### Requête `/forum/category` méthode `POST`
JSON à envoyer :
```
{
	"forum_icon_id":1,
	"title": "test api",
	"position": 5
}
```
### Requête `/forum/forum` méthode `POST`
JSON à envoyer :
```
{
	"forum_category_id": 1,
	"forum_icon_id":1,
	"title": "test api",
	"description": "test de l'api",
	"position": 30
}
```
### Requête `/forum/subject` méthode `POST`
JSON à envoyer :
```
{
	"forum_forum_id": 1,
	"title": "test de sujet",
	"post": {
		"content": "contenue du premier post"
	}
}
```
### Requête `/forum/subject/post` méthode `POST`
JSON à envoyer :
```
{
	"forum_subject_id": 1,
	"content": "suite du contenue d'un sujet"
}
```
### Requête `/forum/icon` méthode `POST`
JSON à envoyer :
```
{
	"path": "url_de_l'image"
}
```

## PUT - Modification
### Requête `/forum/category/{id_category}` méthode `PUT`
JSON à envoyer :
```
{
	"forum_icon_id": 1,
	"title": "modifié",
	"position": 42
}
```
### Requête `/forum/forum/{id_forum}` méthode `PUT`
JSON à envoyer :
```
{
	"forum_category_id": 1,
	"forum_icon_id": 1,
	"title": "forum modifié",
	"description": "description modifiée",
	"position": 42
}
```
### Requête `/forum/icon/{id_icon}` méthode `PUT`
JSON à envoyer :
```
{
	"path": "path_de_l'image"
}
```
### Requête `/forum/post/{id_post}` méthode `PUT`
JSON à envoyer :
```
{
	"content": "content modifié"
}
```
### Requête `/forum/admin/post/{id_post}` méthode `PUT`
JSON à envoyer :
```
{
	"content": "content modifié"
}
```
### Requête `/forum/post/{id_post}/like` méthode `PUT`
### Requête `/forum/post/{id_post}/dislike` méthode `PUT`
### Requête `/forum/subject/{id_subject}` méthode `PUT`
JSON à envoyer :
```
{
	"title": "title modifié"
}
```
### Requête `/forum/admin/subject/{id_subject}` méthode `PUT`
JSON à envoyer :
```
{
	"title": "title modifié"
}
```
### Requête `/forum/admin/subject/{id_subject}/pin` méthode `PUT`
### Requête `/forum/admin/subject/{id_subject}/unpin` méthode `PUT`

## DELETE - Suppression
### Requête `/forum/category/{id_category}` méthode `DELETE`
### Requête `/forum/forum/{id_forum}` méthode `DELETE`
### Requête `/forum/icon/{id_icon}` méthode `DELETE`
### Requête `/forum/post/{id_post}` méthode `DELETE`
### Requête `/forum/admin/post/{id_post}` méthode `DELETE`
### Requête `/forum/subject/{id_subject}` méthode `DELETE`
### Requête `/forum/admin/subject/{id_subject}` méthode `DELETE`