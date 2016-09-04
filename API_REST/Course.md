# Cours
```
	Content-Type : application/json
	Authorization : Bearer <token d'autorisation voir login>
```
## GET - Récupération
### Requête `/course` méthode `GET`
Récéption JSON :
```
{
  "path": "/course",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "comments": [
        {
          "course_id": 1,
          "account_id": 1,
          "create_timestamp": 1465982882754,
          "modify_timestamp": 1465982882754,
          "id": 1,
          "user": {
            "avatar_id": 0,
            "create_timestamp": 0,
            "group_id": 0,
            "last_connect_timestamp": 0,
            "nb_exercises_done": 0,
            "id": 1,
            "avatar": {
              "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
              "id": 1
            },
            "nb_courses_done": 0,
            "username": "Admin",
            "group": {
              "parent_id": 50,
              "name": "administrator",
              "id": 3
            }
          },
          "content": "test de com sur un cour"
        }
      ],
      "course": {
        "account_id": 1,
        "create_timestamp": 1465982816640,
        "locales_id": 1,
        "modify_timestamp": 1465982816640,
        "id": 1,
        "language_id": 1,
        "title": "test de cour",
        "content": "content du cour héhé",
        "account": {
          "avatar_id": 0,
          "create_timestamp": 0,
          "group_id": 0,
          "last_connect_timestamp": 0,
          "nb_exercises_done": 0,
          "id": 1,
          "avatar": {
            "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
            "id": 1
          },
          "nb_courses_done": 0,
          "username": "Admin",
          "group": {
            "parent_id": 50,
            "name": "administrator",
            "id": 3
          }
        }
      }
    }
  ],
  "error": "OK",
  "timestamp": 1473004602857
}
```
### Requête `/course/{limit}` méthode `GET`
Récéption JSON pour une limite de `1`:
```
{
  "path": "/course/limit/{limit}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "comments": [
        {
          "course_id": 1,
          "account_id": 1,
          "create_timestamp": 1465982882754,
          "modify_timestamp": 1465982882754,
          "id": 1,
          "user": {
            "avatar_id": 0,
            "create_timestamp": 0,
            "group_id": 0,
            "last_connect_timestamp": 0,
            "nb_exercises_done": 0,
            "id": 1,
            "avatar": {
              "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
              "id": 1
            },
            "nb_courses_done": 0,
            "username": "Admin",
            "group": {
              "parent_id": 50,
              "name": "administrator",
              "id": 3
            }
          },
          "content": "test de com sur un cour"
        }
      ],
      "course": {
        "account_id": 1,
        "create_timestamp": 1465982816640,
        "locales_id": 1,
        "modify_timestamp": 1465982816640,
        "id": 1,
        "language_id": 1,
        "title": "test de cour",
        "content": "content du cour héhé",
        "account": {
          "avatar_id": 0,
          "create_timestamp": 0,
          "group_id": 0,
          "last_connect_timestamp": 0,
          "nb_exercises_done": 0,
          "id": 1,
          "avatar": {
            "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
            "id": 1
          },
          "nb_courses_done": 0,
          "username": "Admin",
          "group": {
            "parent_id": 50,
            "name": "administrator",
            "id": 3
          }
        }
      }
    }
  ],
  "error": "OK",
  "timestamp": 1473005056955
}
```
### Requête `/course/id/{id}` méthode `GET`
Récéption JSON pour une id de `1`:
{
  "path": "/course/id/{id}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "comments": [
        {
          "course_id": 1,
          "account_id": 1,
          "create_timestamp": 1465982882754,
          "modify_timestamp": 1465982882754,
          "id": 1,
          "user": {
            "avatar_id": 0,
            "create_timestamp": 0,
            "group_id": 0,
            "last_connect_timestamp": 0,
            "nb_exercises_done": 0,
            "id": 1,
            "avatar": {
              "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
              "id": 1
            },
            "nb_courses_done": 0,
            "username": "Admin",
            "group": {
              "parent_id": 50,
              "name": "administrator",
              "id": 3
            }
          },
          "content": "test de com sur un cour"
        }
      ],
      "course": {
        "account_id": 1,
        "create_timestamp": 1465982816640,
        "locales_id": 1,
        "modify_timestamp": 1465982816640,
        "id": 1,
        "language_id": 1,
        "title": "test de cour",
        "content": "content du cour héhé",
        "account": {
          "avatar_id": 0,
          "create_timestamp": 0,
          "group_id": 0,
          "last_connect_timestamp": 0,
          "nb_exercises_done": 0,
          "id": 1,
          "avatar": {
            "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
            "id": 1
          },
          "nb_courses_done": 0,
          "username": "Admin",
          "group": {
            "parent_id": 50,
            "name": "administrator",
            "id": 3
          }
        }
      }
    }
  ],
  "error": "OK",
  "timestamp": 1473005197065
}
```
### Requête `/course/author/id/{id}` méthode `GET`
Récéption JSON pour une author_id de `1`:
{
  "path": "/course/author/id/{author_id}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "comments": [
        {
          "course_id": 1,
          "account_id": 1,
          "create_timestamp": 1465982882754,
          "modify_timestamp": 1465982882754,
          "id": 1,
          "user": {
            "avatar_id": 0,
            "create_timestamp": 0,
            "group_id": 0,
            "last_connect_timestamp": 0,
            "nb_exercises_done": 0,
            "id": 1,
            "avatar": {
              "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
              "id": 1
            },
            "nb_courses_done": 0,
            "username": "Admin",
            "group": {
              "parent_id": 50,
              "name": "administrator",
              "id": 3
            }
          },
          "content": "test de com sur un cour"
        }
      ],
      "course": {
        "account_id": 1,
        "create_timestamp": 1465982816640,
        "locales_id": 1,
        "modify_timestamp": 1465982816640,
        "id": 1,
        "language_id": 1,
        "title": "test de cour",
        "content": "content du cour héhé",
        "account": {
          "avatar_id": 0,
          "create_timestamp": 0,
          "group_id": 0,
          "last_connect_timestamp": 0,
          "nb_exercises_done": 0,
          "id": 1,
          "avatar": {
            "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
            "id": 1
          },
          "nb_courses_done": 0,
          "username": "Admin",
          "group": {
            "parent_id": 50,
            "name": "administrator",
            "id": 3
          }
        }
      }
    }
  ],
  "error": "OK",
  "timestamp": 1473005416744
}
```
### Requête `/course/language/id/{language_id}` méthode `GET`
Récéption JSON pour un language_id de `1`:
{
  "path": "/course/language/id/{language_id}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "comments": [
        {
          "course_id": 1,
          "account_id": 1,
          "create_timestamp": 1465982882754,
          "modify_timestamp": 1465982882754,
          "id": 1,
          "user": {
            "avatar_id": 0,
            "create_timestamp": 0,
            "group_id": 0,
            "last_connect_timestamp": 0,
            "nb_exercises_done": 0,
            "id": 1,
            "avatar": {
              "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
              "id": 1
            },
            "nb_courses_done": 0,
            "username": "Admin",
            "group": {
              "parent_id": 50,
              "name": "administrator",
              "id": 3
            }
          },
          "content": "test de com sur un cour"
        }
      ],
      "course": {
        "account_id": 1,
        "create_timestamp": 1465982816640,
        "locales_id": 1,
        "modify_timestamp": 1465982816640,
        "id": 1,
        "language_id": 1,
        "title": "test de cour",
        "content": "content du cour héhé",
        "account": {
          "avatar_id": 0,
          "create_timestamp": 0,
          "group_id": 0,
          "last_connect_timestamp": 0,
          "nb_exercises_done": 0,
          "id": 1,
          "avatar": {
            "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
            "id": 1
          },
          "nb_courses_done": 0,
          "username": "Admin",
          "group": {
            "parent_id": 50,
            "name": "administrator",
            "id": 3
          }
        }
      }
    }
  ],
  "error": "OK",
  "timestamp": 1473005495996
}
```
### Requête `/course/locales/id/{locales_id}` méthode `GET`
Récéption JSON pour un locales_id de `1`:
{
  "path": "/course/locales/id/{locales_id}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "comments": [
        {
          "course_id": 1,
          "account_id": 1,
          "create_timestamp": 1465982882754,
          "modify_timestamp": 1465982882754,
          "id": 1,
          "user": {
            "avatar_id": 0,
            "create_timestamp": 0,
            "group_id": 0,
            "last_connect_timestamp": 0,
            "nb_exercises_done": 0,
            "id": 1,
            "avatar": {
              "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
              "id": 1
            },
            "nb_courses_done": 0,
            "username": "Admin",
            "group": {
              "parent_id": 50,
              "name": "administrator",
              "id": 3
            }
          },
          "content": "test de com sur un cour"
        }
      ],
      "course": {
        "account_id": 1,
        "create_timestamp": 1465982816640,
        "locales_id": 1,
        "modify_timestamp": 1465982816640,
        "id": 1,
        "language_id": 1,
        "title": "test de cour",
        "content": "content du cour héhé",
        "account": {
          "avatar_id": 0,
          "create_timestamp": 0,
          "group_id": 0,
          "last_connect_timestamp": 0,
          "nb_exercises_done": 0,
          "id": 1,
          "avatar": {
            "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
            "id": 1
          },
          "nb_courses_done": 0,
          "username": "Admin",
          "group": {
            "parent_id": 50,
            "name": "administrator",
            "id": 3
          }
        }
      }
    }
  ],
  "error": "OK",
  "timestamp": 1473005566739
}
```
### Requête `/course/title/{title}` méthode `GET`
Récéption JSON avec comme titre `test de cour`:
{
  "path": "/course/title/{title}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "comments": [
        {
          "course_id": 1,
          "account_id": 1,
          "create_timestamp": 1465982882754,
          "modify_timestamp": 1465982882754,
          "id": 1,
          "user": {
            "avatar_id": 0,
            "create_timestamp": 0,
            "group_id": 0,
            "last_connect_timestamp": 0,
            "nb_exercises_done": 0,
            "id": 1,
            "avatar": {
              "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
              "id": 1
            },
            "nb_courses_done": 0,
            "username": "Admin",
            "group": {
              "parent_id": 50,
              "name": "administrator",
              "id": 3
            }
          },
          "content": "test de com sur un cour"
        }
      ],
      "course": {
        "account_id": 1,
        "create_timestamp": 1465982816640,
        "locales_id": 1,
        "modify_timestamp": 1465982816640,
        "id": 1,
        "language_id": 1,
        "title": "test de cour",
        "content": "content du cour héhé",
        "account": {
          "avatar_id": 0,
          "create_timestamp": 0,
          "group_id": 0,
          "last_connect_timestamp": 0,
          "nb_exercises_done": 0,
          "id": 1,
          "avatar": {
            "path": "http://www.freakingnews.com/pictures/97500/Korean-Elephant-Rocket--97543.jpg",
            "id": 1
          },
          "nb_courses_done": 0,
          "username": "Admin",
          "group": {
            "parent_id": 50,
            "name": "administrator",
            "id": 3
          }
        }
      }
    }
  ],
  "error": "OK",
  "timestamp": 1473005669238
}
```
### Requête `/course/comment/{id_course}` méthode `GET`
Récéption JSON des commentaires du cours d'id id_course :
{
  "path": "/course/comment/{id_course}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "course_id": 1,
      "account_id": 1,
      "create_timestamp": 1465982882754,
      "modify_timestamp": 1465982882754,
      "id": 1,
      "user": {
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
      },
      "content": "test de com sur un cour"
    }
  ],
  "error": "OK",
  "timestamp": 1473005830703
}
```

## POST - Création
### Requête `/course` méthode `POST`
JSON à envoyer :
```
{
    "locales_id": 1,
    "language_id": 1,
    "title": "Cours de C",
    "content": "Le C est super !"
}
```
### Requête `/course/comment` méthode `POST`
JSON à envoyer :
```
{
	"content": "Super cours merci !"
}
```
### Requête `/course/comment` méthode `POST`
JSON à envoyer :
```

## PUT - Modification
### Requête `/course` méthode `PUT`
JSON à envoyer :
```
{
    "locales_id": 1,
    "language_id": 1,
    "title": "Cours de C",
    "content": "Le C est super !"
}
```
### Requête `/course/comment/id/{id}` méthode `PUT`
JSON à envoyer :
```
{
	"content": "J'adore !"
}
```

## DELETE - Suppression
### Requête `/course/{id}` méthode `DELETE`
### Requête `/course/comment/{id}` méthode `DELETE`