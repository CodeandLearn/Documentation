# Badge (r�daction en cours...)
## GET - R�cup�ration
### Requ�te `/account/badges/list` m�thode `GET`
R�ception JSON :
```
{
  "path": "/account/badges/list",
  "code": 200,
  "method": "GET",
  "data": [
    {
      "badge": {
        "path_img": "http://127.0.0.1:3000/assets/images/badge/epitech_experience_2016.png",
        "name": "Epitech Experience 2016",
        "description": "description du badge",
        "id": 10,
        "type": 50
      },
      "account_id": 1,
      "badge_id": 10,
      "timestamp": 1480193041921
    }
  ],
  "length": 10,
  "error": "OK",
  "timestamp": 1480244875032
}
```