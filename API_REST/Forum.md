# Forum
```
	Content-Type : application/json
	Authorization : Bearer <token d'autorisation voir login>
```
## GET - Récupération
### Requête `/forum_categories` méthode `GET`
Récéption JSON :
```
{
  "path": "/forum_categories",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "name": "Test",
      "id": 1
    },
    {
      "name": "Category",
      "id": 2
    }
  ],
  "error": "OK",
  "timestamp": 1474554338524
}
```
### Requête `/forum_subcategories/{category_id}` méthode `GET`
Récéption JSON:
```
{
  "path": "/forum_subcategories/{category_id}`",
  "code": 200,
  "method": "GET",
  "data": [
	{
		"id": 1,
		"forum_category_id": 1,
		"title": "Test",
		"description": "Ceci est une description"
	}
  ],
  "error": "OK",
  "timestamp": 1474554338524
}
```
### Requête `/forum_subjects/{forum_id}` méthode `GET`
Récéption JSON:
```
{
  "path": "/forum_subjects/{forum_id}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "id": 1,
      "title": "Super sujet",
	  "account_id": 1,
	  "created_at": 1474554338524,
	  "last_updated": 1474554338524,
	  "last_account_id": 2,
	  "forum_subcategory_id": 1,
	  "likes": 42
    }
  ],
  "error": "OK",
  "timestamp": 1474554338524
}
```
### Requête `/forum_posts/{subject_id}` méthode `GET`
Récéption JSON:
```
{
  "path": "/forum_posts/{subject_id}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "id": 1,
	  "account_id": 1,
	  "forum_subject_id": 1,
	  "content": "Super post."
	  "created_at": 1474554338524,
	  "last_updated": 1474554338524,
	  "likes": 42
    }
  ],
  "error": "OK",
  "timestamp": 1474554338524
}
```

## POST - Création
### Requête `/forum_category` méthode `POST`
JSON à envoyer :
```
{
    "title": "Prog",
	"description": "La prog c'est cool."
}
```
### Requête `/forum_subcategory` méthode `POST`
JSON à envoyer :
```
{
    "forum_category_id": 1,
	"title": "C",
	"description": "Le C c'est cool."
}
```
### Requête `/forum_subject` méthode `POST`
JSON à envoyer :
```
{
	"title": "C",
	"account_id": 1,
	"forum_subcategory_id": 1
}
```
### Requête `/forum_post` méthode `POST`
JSON à envoyer :
```
{
    "account_id": 1,
	"forum_subject_id": 1,
	"content": "Blabla."
}
```

## PUT - Modification
### Requête `/forum_category` méthode `POST`
JSON à envoyer :
```
{
    "title": "Prog",
	"description": "La prog c'est cool."
}
```
### Requête `/forum_subcategory` méthode `POST`
JSON à envoyer :
```
{
    "forum_category_id": 1,
	"title": "C",
	"description": "Le C c'est cool."
}
```
### Requête `/forum_subject` méthode `POST`
JSON à envoyer :
```
{
	"title": "C",
	"account_id": 1,
	"forum_subcategory_id": 1
}
```
### Requête `/forum_post` méthode `POST`
JSON à envoyer :
```
{
    "account_id": 1,
	"forum_subject_id": 1,
	"content": "Blabla."
}
```

## DELETE - Suppression
### Requête `/forum_category/{id}` méthode `DELETE`
### Requête `/forum_subcategory/{id}` méthode `DELETE`
### Requête `/forum_subject/{id}` méthode `DELETE`
### Requête `/forum_post/{id}` méthode `DELETE`