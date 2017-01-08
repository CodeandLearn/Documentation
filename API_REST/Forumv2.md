# Forum
## GET - Récupération
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

## POST - Création

## PUT - Modification

## DELETE - Suppression