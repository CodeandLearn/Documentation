# Forum
## GET - R�cup�ration

Les 3 premi�re routes permettent d'avoir toute les informations n�cessaires � l'affichage du forum. `/forum`, `/forum/{id_forum}`, `/forum/subject/{id_subject}`.

### Requ�te `/forum` m�thode `GET`
R�c�ption JSON :
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
### Requ�te `/forum/{id_forum}` m�thode `GET`
R�c�ption JSON:
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
### Requ�te `/forum/subject/{id_subject}` m�thode `GET`
R�c�ption JSON:
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
### Requ�te `/forum/categories` m�thode `GET`
R�c�ption JSON:
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
### Requ�te `/forum/categories/order/position` m�thode `GET`
R�c�ption JSON:
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
### Requ�te `/forum/category/{id_category}` m�thode `GET`
R�c�ption JSON:
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
### Requ�te `/forum/icons` m�thode `GET`
R�c�ption JSON:
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
### Requ�te `/forum/icon/{id_icon}` m�thode `GET`
R�c�ption JSON:
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

## POST - Cr�ation
### Requ�te `/forum/category` m�thode `POST`
JSON � envoyer :
```
{
	"forum_icon_id":1,
	"title": "test api",
	"position": 5
}
```
### Requ�te `/forum/forum` m�thode `POST`
JSON � envoyer :
```
{
	"forum_category_id": 1,
	"forum_icon_id":1,
	"title": "test api",
	"description": "test de l'api",
	"position": 30
}
```
### Requ�te `/forum/subject` m�thode `POST`
JSON � envoyer :
```
{
	"forum_forum_id": 1,
	"title": "test de sujet",
	"post": {
		"content": "contenue du premier post"
	}
}
```
### Requ�te `/forum/subject/post` m�thode `POST`
JSON � envoyer :
```
{
	"forum_subject_id": 1,
	"content": "suite du contenue d'un sujet"
}
```
### Requ�te `/forum/icon` m�thode `POST`
JSON � envoyer :
```
{
	"path": "url_de_l'image"
}
```

## PUT - Modification
### Requ�te `/forum/category/{id_category}` m�thode `PUT`
JSON � envoyer :
```
{
	"forum_icon_id": 1,
	"title": "modifi�",
	"position": 42
}
```
### Requ�te `/forum/forum/{id_forum}` m�thode `PUT`
JSON � envoyer :
```
{
	"forum_category_id": 1,
	"forum_icon_id": 1,
	"title": "forum modifi�",
	"description": "description modifi�e",
	"position": 42
}
```
### Requ�te `/forum/icon/{id_icon}` m�thode `PUT`
JSON � envoyer :
```
{
	"path": "path_de_l'image"
}
```
### Requ�te `/forum/post/{id_post}` m�thode `PUT`
JSON � envoyer :
```
{
	"content": "content modifi�"
}
```
### Requ�te `/forum/admin/post/{id_post}` m�thode `PUT`
JSON � envoyer :
```
{
	"content": "content modifi�"
}
```
### Requ�te `/forum/post/{id_post}/like` m�thode `PUT`
### Requ�te `/forum/post/{id_post}/dislike` m�thode `PUT`
### Requ�te `/forum/subject/{id_subject}` m�thode `PUT`
JSON � envoyer :
```
{
	"title": "title modifi�"
}
```
### Requ�te `/forum/admin/subject/{id_subject}` m�thode `PUT`
JSON � envoyer :
```
{
	"title": "title modifi�"
}
```
### Requ�te `/forum/admin/subject/{id_subject}/pin` m�thode `PUT`
### Requ�te `/forum/admin/subject/{id_subject}/unpin` m�thode `PUT`

## DELETE - Suppression
### Requ�te `/forum/category/{id_category}` m�thode `DELETE`
### Requ�te `/forum/forum/{id_forum}` m�thode `DELETE`
### Requ�te `/forum/icon/{id_icon}` m�thode `DELETE`
### Requ�te `/forum/post/{id_post}` m�thode `DELETE`
### Requ�te `/forum/admin/post/{id_post}` m�thode `DELETE`
### Requ�te `/forum/subject/{id_subject}` m�thode `DELETE`
### Requ�te `/forum/admin/subject/{id_subject}` m�thode `DELETE`