# 🔗 Endpoints
Esta aplicación consume datos desde una API de código abierto y utiliza una licencia BSD.

!!! tip "API utilizada"
    Esta app utiliza la **[Rick and Morty API](https://rickandmortyapi.com/documentation)**, un servicio gratuito y abierto que permite acceder a información sobre personajes, episodios y ubicaciones de la serie.

Puedes consultar la documentación oficial en el siguiente enlace:

👉 **[https://rickandmortyapi.com/documentation](https://rickandmortyapi.com/documentation)**

---
A continuación se describen los endpoints consumidos desde el servicio web y su estructura.

## 👥 `/character`

Obtiene uno o varios personajes.

```http
GET /api/character/
```
#### Ejemplo de llamada al Endpoint
=== "Swift"
    ```swift
    let url = URL(string: "https://rickandmortyapi.com/api/character")!
    ```
=== "JavaScript"
    ```js
    fetch("https://rickandmortyapi.com/api/character")
        .then(res => res.json())
        .then(data => console.log(data));
    ```

#### Ejemplo de retorno del Endpoint
```JSON
{
    "info": {
        "count": 826,
        "pages": 42,
        "next": "https://rickandmortyapi.com/api/character?page=2",
        "prev": null
    },
    "results": [
        {
            "id": 1,
            "name": "Rick Sanchez",
            "status": "Alive",
            "species": "Human",
            "type": "",
            "gender": "Male",
            "origin": {
                "name": "Earth (C-137)",
                "url": "https://rickandmortyapi.com/api/location/1"
            },
            "location": {
                "name": "Citadel of Ricks",
                "url": "https://rickandmortyapi.com/api/location/3"
            },
            "image": "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
            "episode": [
                "https://rickandmortyapi.com/api/episode/1",
                "https://rickandmortyapi.com/api/episode/2",
                "https://rickandmortyapi.com/api/episode/3"
            ],
            "url": "https://rickandmortyapi.com/api/character/1",
            "created": "2017-11-04T18:48:46.250Z"
        }
    ]
}
```
!!! tip
    Puedes acceder a un personaje por ID usando `/character/{id}`.

---

## 📍 `/location`

Proporciona información sobre una ubicación.

```http
GET /api/location
```
#### Ejemplo de llamada al Endpoint
=== "Swift"
    ```swift
    let url = URL(string: "https://rickandmortyapi.com/api/location")!
    ```
=== "JavaScript"
    ```js
    fetch("https://rickandmortyapi.com/api/location")
        .then(res => res.json())
        .then(data => console.log(data));
    ```

#### Ejemplo de retorno del Endpoint
```JSON
{
    "info": {
        "count": 126,
        "pages": 7,
        "next": "https://rickandmortyapi.com/api/location?page=2",
        "prev": null
    },
    "results": [
        {
            "id": 1,
            "name": "Earth (C-137)",
            "type": "Planet",
            "dimension": "Dimension C-137",
            "residents": [
                "https://rickandmortyapi.com/api/character/38",
                "https://rickandmortyapi.com/api/character/45"
            ],
            "url": "https://rickandmortyapi.com/api/location/1",
            "created": "2017-11-10T12:42:04.162Z"
        }
    ]
}
```

!!! note
    Puedes usar este endpoint para mostrar de dónde provienen los personajes.