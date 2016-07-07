#### Objects

### UserExercise
```
{
  "account_id": 12,
  "exercice_id": 2,
  "id": 2
}
```

### Code
```
{
  "create_timestamp": 1465981217540,
  "user_exercice_id": 2,
  "modify_timestamp": 1465981217540,
  "id": 2,
  "content": "#include <stdio.h>\n \nint main()\n{\n  printf(\"Hello world\\n\");\n  return 0;\n}",
  "name": "file.txt"
}

```

### Grade
```
{
  "user_exercice_id": 1,
  "id": 2,
  "value": 10,
  "timestamp": 1465981188313
}
```

### Log
```
{
  "user_exercice_id": 1,
  "id": 2,
  "content": "test",
  "timestamp": 1465981262675
}
```

#### Get Methods

### /user_exercises

Returns the list of user_exercise objects linked to the authenticated user
```
{
  "path": "/user_exercises",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "account_id": 12,
      "exercice_id": 2,
      "id": 2
    },
    {
      "account_id": 12,
      "exercice_id": 3,
      "id": 3
    },
    {
      "account_id": 12,
      "exercice_id": 1,
      "id": 4
    }
  ],
  "error": "OK",
  "timestamp": 1466865844298
}
```
### user_exercise/{exercise_id}
Returns the user_exercise object linked to the connected user pointing to the exercise parametre
```
{
  "path": "/user_exercise/{id}",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "account_id": 12,
      "exercice_id": 1,
      "id": 4
    }
  ],
  "error": "OK",
  "timestamp": 1466865926781
}
```


#### Post Methods

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
### user_exercise/

Ajoute une entree

```
{
  "account_id": 12,
  "exercice_id": 1
}
```


#### Put Methods

### user_exercise/{id}
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
Modifie une entree

```
{
  "account_id": 12,
  "exercice_id": 1,
  "id" = 1
}
```

#### Delete Routes

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
### /user_exercise/{id}

### /user_exercise/code/{id}

### /user_exercise/log/{id}

### /user_exercise/grade/{id}
