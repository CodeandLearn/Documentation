# Réferences GET
#### **GET: /user/[string:token]/[string:username]**
Renvoie les informations sur l’utilisateur “username”.

Si le Status HTTP est 200:
```
	{
		"user_id": 1,
		"username": "John",
		"user_email": "john@legend.ie",
		"user_group_id": 1,
		"status": 200
	}
```
* `user_id` : l’id de l’utilisateur dans la base de données;
* `username` : le nom de l’utilisateur;
* `user_email` : son email;
* `user_group_id` : le groupe auquel il appartient (permet de connaître ses permissions);
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET: /user/id/[string:token]/[int:id]**
Renvoie les informations sur l’utilisateur par son id.

Si le Status HTTP est 200:
```
	{
		"user_id": 1,
		"username": "John",
		"user_email": "john@legend.ie",
		"user_group_id": 1,
		"status": 200
	}
```
* `user_id` : l’id de l’utilisateur dans la base de données;
* `username` : le nom de l’utilisateur;
* `user_email` : son email;
* `user_group_id` : le groupe auquel il appartient (permet de connaître ses permissions);
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET: /user/email/[string:token]/[string:email]**
Renvoie les informations sur l’utilisateur par son email.

Si le Status HTTP est 200:
```
	{
		"user_id": 1,
		"username": "John",
		"user_email": "john@legend.ie",
		"user_group_id": 1,
		"status": 200
	}
```
* `user_id` : l’id de l’utilisateur dans la base de données;
* `username` : le nom de l’utilisateur;
* `user_email` : son email;
* `user_group_id` : le groupe auquel il appartient (permet de connaître ses permissions);
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/user/exercice/id/[string:token]/[int:id]**
Renvoi les informations d'un exercice fait par un utilisateur par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"account_id": 1,
		"exercice_id": 1,
		"grade_id": 1,
		"code_id": 1,
		"status": 200
	}
```
* `id` : l'id de l'exercice effectué;
* `account_id` : l'id de l'utilisateur qui l'a fait;
* `exercice_id` : l'id de l'énoncé de l'exercice;
* `grade_id` : l'id de la note attribuée;
* `code_id` : l'id du code fourni par l'utilisateur;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/user/exercice/account_id/[string:token]/[int:account_id]**
Renvoi les informations des exercice fait par un utilisateur par son account_id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 1,
		"exercice_id": 1,
		"grade_id": 1,
		"code_id": 1,
		"status": 200
	}
```
* `id` : l'id de l'exercice effectué;
* `account_id` : l'id de l'utilisateur qui l'a fait;
* `exercice_id` : l'id de l'énoncé de l'exercice;
* `grade_id` : l'id de la note attribuée;
* `code_id` : l'id du code fourni par l'utilisateur;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/user/exercice/exercice_id/[string:token]/[int:exercice_id]**
Renvoi les informations des exercice fait par un utilisateur à partir de l'id de l'énoncé.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 1,
		"exercice_id": 1,
		"grade_id": 1,
		"code_id": 1,
		"status": 200
	}
```
* `id` : l'id de l'exercice effectué;
* `account_id` : l'id de l'utilisateur qui l'a fait;
* `exercice_id` : l'id de l'énoncé de l'exercice;
* `grade_id` : l'id de la note attribuée;
* `code_id` : l'id du code fourni par l'utilisateur;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/user/exercice/grade_id/[string:token]/[int:grade_id]**
Renvoi les informations de l'exercice lié à la note par son grade_id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"account_id": 1,
		"exercice_id": 1,
		"grade_id": 1,
		"code_id": 1,
		"status": 200
	}
```
* `id` : l'id de l'exercice effectué;
* `account_id` : l'id de l'utilisateur qui l'a fait;
* `exercice_id` : l'id de l'énoncé de l'exercice;
* `grade_id` : l'id de la note attribuée;
* `code_id` : l'id du code fourni par l'utilisateur;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/user/exercice/code_id/[string:token]/[int:code_id]**
Renvoi les informations de l'exercice lié au code fourni par l'utilisateur par son code_id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"account_id": 1,
		"exercice_id": 1,
		"grade_id": 1,
		"code_id": 1,
		"status": 200
	}
```
* `id` : l'id de l'exercice effectué;
* `account_id` : l'id de l'utilisateur qui l'a fait;
* `exercice_id` : l'id de l'énoncé de l'exercice;
* `grade_id` : l'id de la note attribuée;
* `code_id` : l'id du code fourni par l'utilisateur;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/blog/category/id/[string:token]/[int:id]**
Renvoie une catégorie du blog par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"name": "C++",
		"status": 200
	}
```
* `id` : l'id de la catégorie;
* `name` : le nom de la catégorie;
* `status` : code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/blog/category/name/[string:token]/[string:name]**
Renvoie une catégorie du blog par son nom.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"name": "C++",
		"status": 200
	}
```
* `id` : l'id de la catégorie;
* `name` : le nom de la catégorie;
* `status` : code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/blog/comment/id/[string:token]/[int:id]**
Renvoie un commentaire d'un post du blog par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"account_id": 9,
		"blog_post_id": 47,
		"content": "Super news, merci le staff pour votre travail !",
		"date": "11/04/2016",
		"status": 200
	}
```
* `id`: l'id du commentaire;
* `account_id`: l'id du compte de l'auteur du commentaire;
* `blog_post_id` : l'id du post contenant ce commentaire;
* `content` : le contenu du commentaire;
* `date` : la date à laquelle le commentaire a été posté;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/blog/comment/account_id/[string:token]/[int:account_id]**
Renvoie les commentaires d'un utilisateur sur le blog par son account_id.

Si le Status HTTP est 200, cela renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 9,
		"blog_post_id": 47,
		"content": "Super news, merci le staff pour votre travail !",
		"date": "11/04/2016",
		"status": 200
	}
```
* `id`: l'id du commentaire;
* `account_id`: l'id du compte de l'auteur du commentaire;
* `blog_post_id` : l'id du post contenant ce commentaire;
* `content` : le contenu du commentaire;
* `date` : la date à laquelle le commentaire a été posté;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/blog/comment/blog_post_id/[string:token]/[int:blog_post_id]**
Renvoie les commentaires d'un post sur le blog par son id.

Si le Status HTTP est 200, cela renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 9,
		"blog_post_id": 47,
		"content": "Super news, merci le staff pour votre travail !",
		"date": "11/04/2016",
		"status": 200
	}
```
* `id`: l'id du commentaire;
* `account_id`: l'id du compte de l'auteur du commentaire;
* `blog_post_id` : l'id du post contenant ce commentaire;
* `content` : le contenu du commentaire;
* `date` : la date à laquelle le commentaire a été posté;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/blog/comment/date/[string:token]/[string:date]**
Renvoie les commentaires du blog postés à cette date.

Si le Status HTTP est 200, cela renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 9,
		"blog_post_id": 47,
		"content": "Super news, merci le staff pour votre travail !",
		"date": "11/04/2016",
		"status": 200
	}
```
* `id`: l'id du commentaire;
* `account_id`: l'id du compte de l'auteur du commentaire;
* `blog_post_id` : l'id du post contenant ce commentaire;
* `content` : le contenu du commentaire;
* `date` : la date à laquelle le commentaire a été posté;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/code/id/[string:token]/[int:id]**
Renvoie les informations sur le code d'un exercice par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"account_id": 3,
		"user_exercice_id": 2,
		"content": "<?php echo 'Ca marche !'; ?>",
		"status": 200
	}
```
* `id`: l'id du code;
* `account_id`: l'id du compte de l'auteur de ce code;
* `user_exercice_id` : l'id de l'exercice auquel il appartient;
* `content` : le contenu du code;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/code/account_id/[string:token]/[int:account_id]**
Renvoie les informations sur les codes d'un utilisateur par son account_id.

Si le Status HTTP est 200, cela renvoie une array d'objet JSON de ce format :
```
	{
		"id": 1,
		"account_id": 3,
		"user_exercice_id": 2,
		"content": "<?php echo 'Ca marche !'; ?>",
		"status": 200
	}
```
* `id`: l'id du code;
* `account_id`: l'id du compte de l'auteur de ce code;
* `user_exercice_id` : l'id de l'exercice auquel il appartient;
* `content` : le contenu du code;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).


#### **GET:/code/user_exercice_id/[string:token]/[int:user_exercice_id]**
Renvoie les informations sur les codes d'un exercice par son id.

Si le Status HTTP est 200, cela renvoie une array d'objet JSON de ce format :
```
	{
		"id": 1,
		"account_id": 3,
		"user_exercice_id": 2,
		"content": "<?php echo 'Ca marche !'; ?>",
		"status": 200
	}
```
* `id`: l'id du code;
* `account_id`: l'id du compte de l'auteur de ce code;
* `user_exercice_id` : l'id de l'exercice auquel il appartient;
* `content` : le contenu du code;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/course/id/[string:token]/[int:id]**
Renvoie les informations sur un cours par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"account_id": 3,
		"locales_id": 1,
		"language_id": 2,
		"title": "Le C++ pour les Nuls",
		"content": "Le C++ c'est ...",
		"status": 200
	}
```
* `id`: l'id du cours;
* `account_id`: l'id du compte de l'auteur de ce cours;
* `locales_id` : l'id du langage de rédaction du cours (ex: Français);
* `language_id` : l'id du langage concerné (ex: C++);
* `title` : le titre du cours;
* `content` : le contenu du code;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/course/account_id/[string:token]/[int:account_id]**
Renvoie les informations sur les cours crées par un utilisateur par son account_id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 3,
		"locales_id": 1,
		"language_id": 2,
		"title": "Le C++ pour les Nuls",
		"content": "Le C++ c'est ...",
		"status": 200
	}
```
* `id`: l'id du cours;
* `account_id`: l'id du compte de l'auteur de ce cours;
* `locales_id` : l'id du langage de rédaction du cours (ex: Français);
* `language_id` : l'id du langage concerné (ex: C++);
* `title` : le titre du cours;
* `content` : le contenu du code;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/course/locales_id/[string:token]/[int:locales_id]**
Renvoie les informations sur les cours rédigés dans un langage par son id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 3,
		"locales_id": 1,
		"language_id": 2,
		"title": "Le C++ pour les Nuls",
		"content": "Le C++ c'est ...",
		"status": 200
	}
```
* `id`: l'id du cours;
* `account_id`: l'id du compte de l'auteur de ce cours;
* `locales_id` : l'id du langage de rédaction du cours (ex: Français);
* `language_id` : l'id du langage concerné (ex: C++);
* `title` : le titre du cours;
* `content` : le contenu du code;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/course/language_id/[string:token]/[int:language_id]**
Renvoie les informations sur les cours concernant un langage de programmation par son id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 3,
		"locales_id": 1,
		"language_id": 2,
		"title": "Le C++ pour les Nuls",
		"content": "Le C++ c'est ...",
		"status": 200
	}
```
* `id`: l'id du cours;
* `account_id`: l'id du compte de l'auteur de ce cours;
* `locales_id` : l'id du langage de rédaction du cours (ex: Français);
* `language_id` : l'id du langage concerné (ex: C++);
* `title` : le titre du cours;
* `content` : le contenu du code;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/course/title/[string:token]/[string:title]**
Renvoie les informations sur les cours ayant comme titre (ou partie de titre) la string title.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 3,
		"locales_id": 1,
		"language_id": 2,
		"title": "Le C++ pour les Nuls",
		"content": "Le C++ c'est ...",
		"status": 200
	}
```
* `id`: l'id du cours;
* `account_id`: l'id du compte de l'auteur de ce cours;
* `locales_id` : l'id du langage de rédaction du cours (ex: Français);
* `language_id` : l'id du langage concerné (ex: C++);
* `title` : le titre du cours;
* `content` : le contenu du code;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/course/comment/id/[string:token]/[int:id]**
Renvoie un commentaire d'un cours par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"course_id": 3,
		"account_id": 45,
		"content": "Super cours merci !",
		"date": "11/01/2016",
		"status": 200
	}
```
* `id` : l'id du commentaire;
* `course_id` : l'id du cours lié à ce commentaire;
* `account_id` : l'id du compte de l'auteur de ce commentaire;
* `content` : le contenu du commentaire;
* `date` : la date à laquelle il a été posté;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/course/comment/account_id/[string:token]/[int:account_id]**
Renvoie les commentaires de cours d'un utilisateur par son account_id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"course_id": 3,
		"account_id": 45,
		"content": "Super cours merci !",
		"date": "11/01/2016",
		"status": 200
	}
```
* `id` : l'id du commentaire;
* `course_id` : l'id du cours lié à ce commentaire;
* `account_id` : l'id du compte de l'auteur de ce commentaire;
* `content` : le contenu du commentaire;
* `date` : la date à laquelle il a été posté;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/course/comment/course_id/[string:token]/[int:course_id]**
Renvoie les commentaires d'un cours par son id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"course_id": 3,
		"account_id": 45,
		"content": "Super cours merci !",
		"date": "11/01/2016",
		"status": 200
	}
```
* `id` : l'id du commentaire;
* `course_id` : l'id du cours lié à ce commentaire;
* `account_id` : l'id du compte de l'auteur de ce commentaire;
* `content` : le contenu du commentaire;
* `date` : la date à laquelle il a été posté;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/course/comment/date/[string:token]/[string:date]**
Renvoie les commentaires des cours postés à cette date.

Si le Status HTTP est 200, cela renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"course_id": 3,
		"account_id": 45,
		"content": "Super cours merci !",
		"date": "11/01/2016",
		"status": 200
	}
```
* `id` : l'id du commentaire;
* `course_id` : l'id du cours lié à ce commentaire;
* `account_id` : l'id du compte de l'auteur de ce commentaire;
* `content` : le contenu du commentaire;
* `date` : la date à laquelle il a été posté;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/exercice/id/[string:token]/[int:id]**
Renvoie un exercice par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"account_id": 3,
		"course_id": 1,
		"date": "19/10/2015",
		"title": "C++ Exercices",
		"instruction": "Create a class ...",
		"script_id": 2,
		"grade_max": 100,
		"correction_id": 1,
		"status": 200
	}
```
* `id` : l'id de l'exercice;
* `account_id` : l'id du compte de l'auteur de cet exercice;
* `course_id` : l'id du cours lié à cet exercice;
* `date` : la date à laquelle l'exercice a été posté;
* `title` : le titre de l'exercice;
* `instruction` : les instructions de l'exercice;
* `script_id` : l'id du script de compilation et de correction lié à cet exercice;
* `grade_max` : la note maximum possible;
* `correction_id` : l'id du code de correction de l'exercice;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/exercice/account_id/[string:token]/[int:account_id]**
Renvoie les exercices d'un créateur par son account_id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 3,
		"course_id": 1,
		"date": "19/10/2015",
		"title": "C++ Exercices",
		"instruction": "Create a class ...",
		"script_id": 2,
		"grade_max": 100,
		"correction_id": 1,
		"status": 200
	}
```
* `id` : l'id de l'exercice;
* `account_id` : l'id du compte de l'auteur de cet exercice;
* `course_id` : l'id du cours lié à cet exercice;
* `date` : la date à laquelle l'exercice a été posté;
* `title` : le titre de l'exercice;
* `instruction` : les instructions de l'exercice;
* `script_id` : l'id du script de compilation et de correction lié à cet exercice;
* `grade_max` : la note maximum possible;
* `correction_id` : l'id du code de correction de l'exercice;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/exercice/course_id/[string:token]/[int:course_id]**
Renvoie les exercices par l'id du cours qui y est lié.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 3,
		"course_id": 1,
		"date": "19/10/2015",
		"title": "C++ Exercices",
		"instruction": "Create a class ...",
		"script_id": 2,
		"grade_max": 100,
		"correction_id": 1,
		"status": 200
	}
```
* `id` : l'id de l'exercice;
* `account_id` : l'id du compte de l'auteur de cet exercice;
* `course_id` : l'id du cours lié à cet exercice;
* `date` : la date à laquelle l'exercice a été posté;
* `title` : le titre de l'exercice;
* `instruction` : les instructions de l'exercice;
* `script_id` : l'id du script de compilation et de correction lié à cet exercice;
* `grade_max` : la note maximum possible;
* `correction_id` : l'id du code de correction de l'exercice;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/exercice/title/[string:token]/[string:title]**
Renvoie les exercices dont le titre est/contient [string:title].

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 3,
		"course_id": 1,
		"date": "19/10/2015",
		"title": "C++ Exercices",
		"instruction": "Create a class ...",
		"script_id": 2,
		"grade_max": 100,
		"correction_id": 1,
		"status": 200
	}
```
* `id` : l'id de l'exercice;
* `account_id` : l'id du compte de l'auteur de cet exercice;
* `course_id` : l'id du cours lié à cet exercice;
* `date` : la date à laquelle l'exercice a été posté;
* `title` : le titre de l'exercice;
* `instruction` : les instructions de l'exercice;
* `script_id` : l'id du script de compilation et de correction lié à cet exercice;
* `grade_max` : la note maximum possible;
* `correction_id` : l'id du code de correction de l'exercice;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/exercice/comment/id/[string:token]/[int:id]**
Renvoie un commentaire d'un exercice par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"exercice_id": 3,
		"account_id": 45,
		"content": "Je ne comprends pas vraiment l'énoncé...",
		"date": "11/01/2016",
		"status": 200
	}
```
* `id` : l'id du commentaire;
* `exercice_id` : l'id de l'exercice lié à ce commentaire;
* `account_id` : l'id du compte de l'auteur de ce commentaire;
* `content` : le contenu du commentaire;
* `date` : la date à laquelle il a été posté;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/exercice/comment/account_id/[string:token]/[int:account_id]**
Renvoie les commentaires d'exercices d'un utilisateur par son account_id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"exercice_id": 3,
		"account_id": 45,
		"content": "Je ne comprends pas vraiment l'énoncé...",
		"date": "11/01/2016",
		"status": 200
	}
```
* `id` : l'id du commentaire;
* `exercice_id` : l'id de l'exercice lié à ce commentaire;
* `account_id` : l'id du compte de l'auteur de ce commentaire;
* `content` : le contenu du commentaire;
* `date` : la date à laquelle il a été posté;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/exercice/comment/exercice_id/[string:token]/[int:exercice_id]**
Renvoie les commentaires d'un exercice par son id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"exercice_id": 3,
		"account_id": 45,
		"content": "Je ne comprends pas vraiment l'énoncé...",
		"date": "11/01/2016",
		"status": 200
	}
```
* `id` : l'id du commentaire;
* `exercice_id` : l'id de l'exercice lié à ce commentaire;
* `account_id` : l'id du compte de l'auteur de ce commentaire;
* `content` : le contenu du commentaire;
* `date` : la date à laquelle il a été posté;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/exercice/comment/date/[string:token]/[string:date]**
Renvoie les commentaires d'exercices postés à cette date.

Si le Status HTTP est 200, cela renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"exercice_id": 3,
		"account_id": 45,
		"content": "Je ne comprends pas vraiment l'énoncé...",
		"date": "11/01/2016",
		"status": 200
	}
```
* `id` : l'id du commentaire;
* `exercice_id` : l'id de l'exercice lié à ce commentaire;
* `account_id` : l'id du compte de l'auteur de ce commentaire;
* `content` : le contenu du commentaire;
* `date` : la date à laquelle il a été posté;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/exercice/correction/id/[string:token]/[int:id]**
Renvoie la correction d'un exercice par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"content": "int main() { int i = 5; return(0); }",
		"status": 200
	}
```
* `id` : l'id de la correction;
* `content` : le contenu de la correction;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/category/id/[string:token]/[int:id]**
Renvoie une catégorie de forum par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"name": "Programmation",
		"status": 200
	}
```
* `id` : l'id de la catégorie;
* `name` : le nom de la catégorie;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/category/id/[string:token]/[string:name]**
Renvoie une catégorie de forum par son nom.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"name": "Programmation",
		"status": 200
	}
```
* `id` : l'id de la catégorie;
* `name` : le nom de la catégorie;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/forums/id/[string:token]/[int:id]**
Renvoie un forum par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"forum_category_id": 1,
		"name": "C++",
		"description" : "Ici on ne parle que de C++ !",
		"status": 200
	}
```
* `id` : l'id du forum;
* `forum_category_id` : la catégorie du forum;
* `name` : le nom du forum;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/forums/forum_category_id/[string:token]/[int:forum_category_id]**
Renvoie les forums d'une catégorie par son id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"forum_category_id": 1,
		"name": "C++",
		"description" : "Ici on ne parle que de C++ !",
		"status": 200
	}
```
* `id` : l'id du forum;
* `forum_category_id` : la catégorie du forum;
* `name` : le nom du forum;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/forums/name/[string:token]/[string:name]**
Renvoie les forums dont le nom est/contient [string:name].

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"forum_category_id": 1,
		"name": "C++",
		"description" : "Ici on ne parle que de C++ !",
		"status": 200
	}
```
* `id` : l'id du forum;
* `forum_category_id` : la catégorie du forum;
* `name` : le nom du forum;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/subject/id/[string:token]/[int:id]**
Renvoie un sujet du forum par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"forum_forums_id": 1,
		"locales_id": 1,
		"title": "Tuto POO",
		"account_id": 2,
		"date": "24/03/2015",
		"replies": 42,
		"views": 42000,
		"status": 200
	}
```
* `id` : l'id du sujet;
* `forum_forums_id` : l'id du forum qui contient ce sujet;
* `locales_id` : l'id du langage utilisé pour rédigé ce sujet;
* `title` : le titre du sujet;
* `account_id` : l'id du compte du créateur du sujet;
* `date` : la date de la création du sujet;
* `replies` : le nombre de réponses au sujet;
* `views` : le nombre de personnes ayant lues/vues le sujet;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/subject/forum_forums_id/[string:token]/[int:forum_forums_id]**
Renvoie les sujets contenus dans un forum par son id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"forum_forums_id": 1,
		"locales_id": 1,
		"title": "Tuto POO",
		"account_id": 2,
		"date": "24/03/2015",
		"replies": 42,
		"views": 42000,
		"status": 200
	}
```
* `id` : l'id du sujet;
* `forum_forums_id` : l'id du forum qui contient ce sujet;
* `locales_id` : l'id du langage utilisé pour rédigé ce sujet;
* `title` : le titre du sujet;
* `account_id` : l'id du compte du créateur du sujet;
* `date` : la date de la création du sujet;
* `replies` : le nombre de réponses au sujet;
* `views` : le nombre de personnes ayant lues/vues le sujet;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/subject/locales_id/[string:token]/[int:locales_id]**
Renvoie les sujets rédigés dans une langue par son id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"forum_forums_id": 1,
		"locales_id": 1,
		"title": "Tuto POO",
		"account_id": 2,
		"date": "24/03/2015",
		"replies": 42,
		"views": 42000,
		"status": 200
	}
```
* `id` : l'id du sujet;
* `forum_forums_id` : l'id du forum qui contient ce sujet;
* `locales_id` : l'id du langage utilisé pour rédigé ce sujet;
* `title` : le titre du sujet;
* `account_id` : l'id du compte du créateur du sujet;
* `date` : la date de la création du sujet;
* `replies` : le nombre de réponses au sujet;
* `views` : le nombre de personnes ayant lues/vues le sujet;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/subject/title/[string:token]/[string:title]**
Renvoie les sujets dont le titre est/contient [string:title].

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"forum_forums_id": 1,
		"locales_id": 1,
		"title": "Tuto POO",
		"account_id": 2,
		"date": "24/03/2015",
		"replies": 42,
		"views": 42000,
		"status": 200
	}
```
* `id` : l'id du sujet;
* `forum_forums_id` : l'id du forum qui contient ce sujet;
* `locales_id` : l'id du langage utilisé pour rédigé ce sujet;
* `title` : le titre du sujet;
* `account_id` : l'id du compte du créateur du sujet;
* `date` : la date de la création du sujet;
* `replies` : le nombre de réponses au sujet;
* `views` : le nombre de personnes ayant lues/vues le sujet;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/subject/account_id/[string:token]/[int:account_id]**
Renvoie les sujets d'un utilisateur par son account_id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"forum_forums_id": 1,
		"locales_id": 1,
		"title": "Tuto POO",
		"account_id": 2,
		"date": "24/03/2015",
		"replies": 42,
		"views": 42000,
		"status": 200
	}
```
* `id` : l'id du sujet;
* `forum_forums_id` : l'id du forum qui contient ce sujet;
* `locales_id` : l'id du langage utilisé pour rédigé ce sujet;
* `title` : le titre du sujet;
* `account_id` : l'id du compte du créateur du sujet;
* `date` : la date de la création du sujet;
* `replies` : le nombre de réponses au sujet;
* `views` : le nombre de personnes ayant lues/vues le sujet;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/subject/date/[string:token]/[string:date]**
Renvoie les sujets crées à la date donnée.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"forum_forums_id": 1,
		"locales_id": 1,
		"title": "Tuto POO",
		"account_id": 2,
		"date": "24/03/2015",
		"replies": 42,
		"views": 42000,
		"status": 200
	}
```
* `id` : l'id du sujet;
* `forum_forums_id` : l'id du forum qui contient ce sujet;
* `locales_id` : l'id du langage utilisé pour rédigé ce sujet;
* `title` : le titre du sujet;
* `account_id` : l'id du compte du créateur du sujet;
* `date` : la date de la création du sujet;
* `replies` : le nombre de réponses au sujet;
* `views` : le nombre de personnes ayant lues/vues le sujet;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/subject/post/id/[string:token]/[int:id]**
Renvoie un post d'un sujet du forum par son id.

Si le Status HTTP est 200:
```
	{
		"id": 1,
		"forum_subject_id": 1,
		"account_id": 2,
		"date": "24/03/2015",
		"content": "Merci Sithis !",
		"likes": 4,
		"status": 200
	}
```
* `id` : l'id du post;
* `forum_subject_id` : l'id du sujet qui contient ce post;
* `account_id` : l'id du compte du posteur;
* `date` : la date de la création du post;
* `content` : le contenu du post;
* `likes` : le nombre de "Like";
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/subject/post/forum_subject_id/[string:token]/[int:forum_subject_id]**
Renvoie les posts d'un sujet par son id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"forum_subject_id": 1,
		"account_id": 2,
		"date": "24/03/2015",
		"content": "Merci Sithis !",
		"likes": 4,
		"status": 200
	}
```
* `id` : l'id du post;
* `forum_subject_id` : l'id du sujet qui contient ce post;
* `account_id` : l'id du compte du posteur;
* `date` : la date de la création du post;
* `content` : le contenu du post;
* `likes` : le nombre de "Like";
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/subject/post/account_id/[string:token]/[int:account_id]**
Renvoie les posts d'un utilisateur par son account_id.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"forum_subject_id": 1,
		"account_id": 2,
		"date": "24/03/2015",
		"content": "Merci Sithis !",
		"likes": 4,
		"status": 200
	}
```
* `id` : l'id du post;
* `forum_subject_id` : l'id du sujet qui contient ce post;
* `account_id` : l'id du compte du posteur;
* `date` : la date de la création du post;
* `content` : le contenu du post;
* `likes` : le nombre de "Like";
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/forum/subject/post/date/[string:token]/[string:date]**
Renvoie les posts postés à une date précise.

Si le Status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"forum_subject_id": 1,
		"account_id": 2,
		"date": "24/03/2015",
		"content": "Merci Sithis !",
		"likes": 4,
		"status": 200
	}
```
* `id` : l'id du post;
* `forum_subject_id` : l'id du sujet qui contient ce post;
* `account_id` : l'id du compte du posteur;
* `date` : la date de la création du post;
* `content` : le contenu du post;
* `likes` : le nombre de "Like";
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/grade/id/[string:token]/[int:id]**
Renvoie une note par son id.

Si le status HTTP est 200:
```
	{
		"id": 1,
		"account_id": 2,
		"exercice_id": 32,
		"value": 15,
		"log_id": 4,
		"status": 200
	}
```
* `id` : l'id de la note;
* `account_id` : l'id de l'utilisateur qui a été noté;
* `exercice_id` : l'id de l'exercice qui a été noté;
* `value` : la note;
* `log_id` : l'id du log de correction;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/grade/account_id/[string:token]/[int:account_id]**
Renvoie les notes d'un utilisateur par son account_id.

Si le status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 2,
		"exercice_id": 32,
		"value": 15,
		"log_id": 4,
		"status": 200
	}
```
* `id` : l'id de la note;
* `account_id` : l'id de l'utilisateur qui a été noté;
* `exercice_id` : l'id de l'exercice qui a été noté;
* `value` : la note;
* `log_id` : l'id du log de correction;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/grade/exercice_id/[string:token]/[int:exercice_id]**
Renvoie les notes d'un exercice par son id.

Si le status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 2,
		"exercice_id": 32,
		"value": 15,
		"log_id": 4,
		"status": 200
	}
```
* `id` : l'id de la note;
* `account_id` : l'id de l'utilisateur qui a été noté;
* `exercice_id` : l'id de l'exercice qui a été noté;
* `value` : la note;
* `log_id` : l'id du log de correction;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/grade/value/[string:token]/[int:value]**
Renvoie les notes d'une valeur précise.

Si le status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"account_id": 2,
		"exercice_id": 32,
		"value": 15,
		"log_id": 4,
		"status": 200
	}
```
* `id` : l'id de la note;
* `account_id` : l'id de l'utilisateur qui a été noté;
* `exercice_id` : l'id de l'exercice qui a été noté;
* `value` : la note;
* `log_id` : l'id du log de correction;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/grade/log_id/[string:token]/[int:log_id]**
Renvoie la note lié à un log de correction par son id.

Si le status HTTP est 200:
```
	{
		"id": 1,
		"account_id": 2,
		"exercice_id": 32,
		"value": 15,
		"log_id": 4,
		"status": 200
	}
```
* `id` : l'id de la note;
* `account_id` : l'id de l'utilisateur qui a été noté;
* `exercice_id` : l'id de l'exercice qui a été noté;
* `value` : la note;
* `log_id` : l'id du log de correction;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/group/id/[string:token]/[int:id]**
Renvoie un groupe par son id.

Si le status HTTP est 200:
```
	{
		"id": 1,
		"name": "Administrateur",
		"parent_id": 0,
		"status": 200
	}
```
* `id` : l'id du groupe;
* `name` : le nom du groupe;
* `parent_id` : l'id du groupe parent;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/group/name/[string:token]/[string:name]**
Renvoie un groupe par son nom.

Si le status HTTP est 200:
```
	{
		"id": 1,
		"name": "Administrateur",
		"parent_id": 0,
		"status": 200
	}
```
* `id` : l'id du groupe;
* `name` : le nom du groupe;
* `parent_id` : l'id du groupe parent;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/group/parent_id/[string:token]/[int:parent_id]**
Renvoie un groupe par son groupe parent.

Si le status HTTP est 200:
```
	{
		"id": 1,
		"name": "Administrateur",
		"parent_id": 0,
		"status": 200
	}
```
* `id` : l'id du groupe;
* `name` : le nom du groupe;
* `parent_id` : l'id du groupe parent;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/language/id/[string:token]/[int:id]**
Renvoie un langage par son id.

Si le status HTTP est 200:
```
	{
		"id": 1,
		"name": "C",
		"status": 200
	}
```
* `id` : l'id du langage;
* `name` : le nom du langage;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/language/name/[string:token]/[string:name]**
Renvoie un langage par son nom.

Si le status HTTP est 200:
```
	{
		"id": 1,
		"name": "C",
		"status": 200
	}
```
* `id` : l'id du langage;
* `name` : le nom du langage;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/locale/id/[string:token]/[int:id]**
Renvoie une langue par son id.

Si le status HTTP est 200:
```
	{
		"id": 1,
		"name": "Français",
		"status": 200
	}
```
* `id` : l'id de la langue;
* `name` : le nom de la langue;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/locale/name/[string:token]/[string:name]**
Renvoie une langue par son nom.

Si le status HTTP est 200:
```
	{
		"id": 1,
		"name": "Français",
		"status": 200
	}
```
* `id` : l'id de la langue;
* `name` : le nom de la langue;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/log/id/[string:token]/[int:id]**
Renvoie un log par son id.

Si le status HTTP est 200:
```
	{
		"id": 1,
		"content": "Abort error at line 10.",
		"script_id": 1;
		"status": 200
	}
```
* `id` : l'id du log;
* `content` : le contenu du log;
* `script_id` : le script de correction qui a donné ce log;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/log/script_id/[string:token]/[int:script_id]**
Renvoie les logs crées par un script par son id.

Si le status HTTP est 200, la requête renvoie une array d'objet JSON de ce format:
```
	{
		"id": 1,
		"content": "Abort error at line 10.",
		"script_id": 1;
		"status": 200
	}
```
* `id` : l'id du log;
* `content` : le contenu du log;
* `script_id` : le script de correction qui a donné ce log;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).

#### **GET:/script/id/[string:token]/[int:id]**
Renvoie un script de correction par son id.

Si le status HTTP est 200:
```
	{
		"id": 1,
		"content": "./make all",
		"status": 200
	}
```
* `id` : l'id du script de correction;
* `content` : le contenu du script de correction;
* `status`: code 200, voir [Codes d'erreur](./API_REST/CODE.md).