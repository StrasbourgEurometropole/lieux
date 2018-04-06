## Liste des types de lieux

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-types
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {
    "name": {
      "fr_FR": "Petite Enfance"
    },
    "id": "Cat_01"
  },
  {
    "name": {
      "fr_FR": "Social"
    },
    "id": "Cat_04"
  },
  {
    "level": 1,
    "name": {
      "fr_FR": "Accueil de jour"
    },
    "id": "Cat_04_01",
    "parentId": "Cat_04"
  },
  {
    "level": 1,
    "name": {
      "fr_FR": "Accueils de loisirs maternels"
    },
    "id": "Cat_01_06",
    "parentId": "Cat_01"
  }
]
```

Ce endpoint renvoie la liste des types de lieux.

<aside class="notice">Un type de lieu peut avoir un type parent. La profondeur de la catégorie dans l'arbre global est indiqué par la propriété "level" et l'identifiant de la catégorie parente par "parentId".</aside>

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-types`