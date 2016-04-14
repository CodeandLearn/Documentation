# Account
```
	Content-Type : application/json
	Authorization : Bearer <token d'autorisation voir login>
```
## GET - R�cup�ration
### Requ�te `/accounts` m�thode `GET`
R�ception JSON :
```
{
  "timestamp": 1460658809716,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/accounts",
  "data": [
    {
      "id": 1,
      "username": "test",
      "email": "test@hotmail.fr",
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
  ]
}
```
### Requ�te `/accounts/limit/{limit}` m�thode `GET`
R�ception JSON :
```
{
  "timestamp": 1460658823676,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/accounts/limit/1",
  "data": [
    {
      "id": 1,
      "username": "test",
      "email": "test@hotmail.fr",
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
  ]
}
```
### Requ�te `/account` m�thode `GET`
R�ception JSON :
```
{
  "timestamp": 1460658834294,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/account",
  "data": [
    {
      "id": 1,
      "username": "test",
      "email": "test@hotmail.fr",
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
  ]
}
```
### Requ�te `/account/{id}` m�thode `GET`
R�ception JSON :
```
{
  "timestamp": 1460658843455,
  "status": 200,
  "error": "OK",
  "message": "",
  "path": "/account/1",
  "data": [
    {
      "id": 1,
      "username": "test",
      "email": "test@hotmail.fr",
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
  ]
}
```

## POST - Cr�ation
### Requ�te `/register` m�thode `POST`
JSON � envoyer :
```
{
	"username": "USERNAME",
    "password": "PASSWORD",
    "email": "EMAIL@EMAIL.FR"
}
```

## PUT - Modification
### Requ�te `/account` m�thode `PUT`
JSON � envoyer :
```
{
	"username": "USERNAME",
    "password": "PASSWORD",
    "email": "EMAIL@EMAIL.FR",
    "group_id": 1,
    "avatar_id": 1
}
```
### Requ�te `/account/{id}` m�thode `PUT`
JSON � envoyer :
```
{
	"username": "USERNAME",
    "password": "PASSWORD",
    "email": "EMAIL@EMAIL.FR",
    "group_id": 1,
    "avatar_id": 1
}
```

## DELETE - Suppression
### Requ�te `/account` m�thode `DELETE`
### Requ�te `/account/{id}` m�thode `DELETE`