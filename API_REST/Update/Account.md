# Account
```
	Content-Type : application/json
	Authorization : Bearer <token d'autorisation voir login>
```
## GET - Récupération
### Requête `/accounts` méthode `GET`
Réception JSON :
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
### Requête `/accounts/limit/{limit}` méthode `GET`
Réception JSON :
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
### Requête `/account` méthode `GET`
Réception JSON :
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
### Requête `/account/{id}` méthode `GET`
Réception JSON :
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

## POST - Création
### Requête `/register` méthode `POST`
JSON à envoyer :
```
{
	"username": "USERNAME",
    "password": "PASSWORD",
    "email": "EMAIL@EMAIL.FR"
}
```

## PUT - Modification
### Requête `/account` méthode `PUT`
JSON à envoyer :
```
{
	"username": "USERNAME",
    "password": "PASSWORD",
    "email": "EMAIL@EMAIL.FR",
    "group_id": 1,
    "avatar_id": 1
}
```
### Requête `/account/{id}` méthode `PUT`
JSON à envoyer :
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
### Requête `/account` méthode `DELETE`
### Requête `/account/{id}` méthode `DELETE`