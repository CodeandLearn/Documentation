### Objects

## Exercice

Entite contenant les informations de bases de l'exercice

```
{
  "course_id": 1,                 ==> Cours lie a l'exercice
  "account_id": 12,               ==> Auteur
  "instruction": "Hello World!",  ==> Instructions
  "grade_max": 0,                 ==> note maximale
  "id": 1,                        ==> id
  "title": "COUCOU"               ==> Titre
}
```

## Script

Script permettant d'executer et de verifier le code utilisateur
```
{
  "create_timestamp": 1465768973254,    ==> date de creation
  "exercice_id": 1,                     ==> Exercice lie au script
  "modify_timestamp": 1465768973254,    ==> date de derniere modification
  "id": 1,
  "content": "Nothing"                  ==> Contenu du script
}
```

## Correction

Sers de conteneur pour le code contenant la solution de l'exercice
```
{
  "exercice_id": 1,
  "id": 1,
  "content": "Nothing",
  "timestamp": 0
}
```

## Comment

Commentaires
```
{
  {
    "account_id": 12,
    "create_timestamp": 1465769713322,
    "exercice_id": 1,
    "modify_timestamp": 1465769713322,
    "id": 1,
    "content": "Cool Stuff"
  }
}
```

## GET Methods

### /exercises

Cette methode permet de recuperer la liste d'exercices

```
{
  "path": "/exercises",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "course_id": 1,
      "account_id": 12,
      "instruction": "Hello World!",
      "grade_max": 0,
      "id": 1,
      "title": "COUCOU"
    },
    {
      "course_id": 1,
      "account_id": 12,
      "instruction": "Hello Dave",
      "grade_max": 0,
      "id": 3,
      "title": "jeej"
    },
    {
      "course_id": 1,
      "account_id": 12,
      "instruction": "Utiliser la commande 'echo' pour afficher 'Hello World1'",
      "grade_max": 20,
      "id": 4,
      "title": "Test POST exercie"
    }
  ],
  "error": "OK",
  "timestamp": 1465817342774
}
```

### /exercise/course/{course_id}

Cette methode permet de recuperer la liste d'exercices liée au cours passé en paramétre

JSON type sur succès

```
{
  "path": "/exercise/course/{course_id}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "course_id": 1,
      "account_id": 12,
      "instruction": "Hello World!",
      "grade_max": 0,
      "id": 1,
      "title": "COUCOU"
    },
    {
      "course_id": 1,
      "account_id": 12,
      "instruction": "Hello Dave!",
      "grade_max": 0,
      "id": 3,
      "title": "jeej"
    }
  ],
  "error": "OK",
  "timestamp": 1465815932513
}
```

### /exercise/{id}

Cette methode permet de recuperer un exercice par son ID

JSON type sur succès

```
{
  "path": "/exercise/{id}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "course_id": 1,
      "account_id": 12,
      "instruction": "Hello World!",
      "grade_max": 0,
      "id": 1,
      "title": "COUCOU"
    }
  ],
  "error": "OK",
  "timestamp": 1465816065661
}
```

### /exercise/{exercice_id}/script

Cette methode permet de recuperer le script de correction lié à l'exercice parametre

JSON type sur succès

```
{
  "path": "/exercise/{exercice_id}/script",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "create_timestamp": 1465768973254,
      "exercice_id": 1,
      "modify_timestamp": 1465768973254,
      "id": 1,
      "content": "Nothing"
    }
  ],
  "error": "OK",
  "timestamp": 1465815847185
}
```

### /exercise/{exercice_id}/correction

Cette methode permet de recuperer la correction lié à l'exercice parametre

JSON type sur succès

```
{
  "path": "/exercise/{exercice_id}/correction",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "exercice_id": 1,
      "id": 1,
      "content": "Nothing",
      "timestamp": 0
    }
  ],
  "error": "OK",
  "timestamp": 1465816493962
}
```

### /exercise/{exercice_id}/comments

Cette methode permet de recuperer les commentaires lié à l'exercice parametre

JSON type sur succès

```
{
  "path": "/exercise/{exercice_id}/comments",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "account_id": 12,
      "create_timestamp": 1465769713322,
      "exercice_id": 1,
      "modify_timestamp": 1465769713322,
      "id": 1,
      "content": "Cool Stuff"
    }
  ],
  "error": "OK",
  "timestamp": 1465816467612
}
```

### /exercise/{exercice_id}/moderation

Cette methode permet de recuperer l'etat de moderation lié à l'exercice parametre

JSON type sur succès

```
{
  "path": "/exercise/{exercice_id}/moderation",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "exercice_id": 1,
      "moderation_validate_id": 1,
      "commentary": "Nothing"
    }
  ],
  "error": "OK",
  "timestamp": 1465816481464
}
```

## POST Methods

### Succès type

```
{
  "path": "{Path}",
  "code": 200,
  "method": "POST",
  "id": 1,                    ==> Identite de l'objet insere
  "error": "OK",
  "timestamp": 1465916194498
}
```

### /exercise

Insert un exercice dans la base de données

JSON Body

```
{
    "course_id": 1,
    "account_id": 12,
    "instruction": "Utiliser la commande 'echo' pour afficher 'Hello World1'",
    "grade_max": 20,
    "title": "Test POST exercie"
}
```

### /exercise/script

Insert un script dans la base de données

JSON Body

```
{
    "exercice_id": 1,
    "content": "Verifie l'exercice"
}
```

### /exercise/comment

Insert un exercice_comment dans la base de données

JSON Body

```
{
  "account_id": 12,
  "exercice_id": 1,
  "content": "Cool Stuff"
}
```

### /exercise/correction

Insert une correction dans la base de données

JSON Body

```
{
  "exercice_id": 1,
  "content": "Correction for the Exercise goes there"
}
```

### /exercise/moderation

Insert une entree de moderation dans la base de données

JSON Body

```
{
  "exercice_id": 1,
  "moderation_validate_id": 1,
  "commentary": "commentary goes there"
}
```

## PUT Methods

### Succès type

```
{
  "path": "{Path}",
  "code": 200,
  "method": "PUT",
  "error": "OK",
  "timestamp": 1465916194498
}
```

### /exercise/{exercice_id}

Modifie un exercice dans la base de données

JSON Body

```
{
    "id": 1,
    "course_id": 1,
    "account_id": 12,
    "instruction": "Utiliser la commande 'echo' pour afficher 'Hello World1'",
    "grade_max": 20,
    "title": "Test POST exercie"
}
```

### /exercise/script/{script_id}

Modifie un script dans la base de données

JSON Body

```
{
    "id": 1,
    "exercice_id": 1,
    "content": "Correction for the Exercise goes there"
}
```

### /exercise/comment/{comment_id}

Modifie un exercice_comment dans la base de données

JSON Body

```
{
  "id": 1,
  "account_id": 12,
  "exercice_id": 1,
  "content": "Cool Stuff"
}
```

### /exercise/correction/{correction_id}

Modifie une correction dans la base de données

JSON Body

```
{
  "id": 1,
  "exercice_id": 1,
  "content": "Correction for the Exercise goes there"
}
```

### /exercise/moderation/{exercice_id}

Modifie une entree de moderation dans la base de données

JSON Body

```
{
  "exercice_id": 1,
  "moderation_validate_id": 1,
  "commentary": "commentary goes there"
}
```

## DELETE Methods

### Succès type

```
{
  "path": "{Path}",
  "code": 200,
  "method": "DELETE",
  "error": "OK",
  "timestamp": 1465916194498
}
```

### /exercise/{id}

### /exercise/script/{script_id}

### /exercise/correction/{correction_id}

### /exercise/comments/{comment_id}

### /exercise/moderation/{exercice_id}
