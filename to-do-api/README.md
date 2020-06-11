# ToDo Api

### List to dos

`GET /to-dos`

##### Responses

`Status: 204 NoContent`

`Status: 200 OK`

```json
[
  {
    "id": 1,
    "title": "Buy milk",
    "dueDate": "2020/06/06",
    "status": "Expired"
  },
  {
    "id": 2,
    "title": "Gym",
    "dueDate": "2021/06/06",
    "status": "ToDo"
  }
]
```

### Get to do

`GET /to-dos/:id`

##### Responses

`Status: 204 NoContent`

`Status: 200 OK`

```json
{
  "id": 1,
  "title": "Buy milk",
  "dueDate": "2020/06/06",
  "status": "Expired"
}
```

### Create to do

`POST /to-dos`

##### Body

```json
{
  "title": "Buy milk",
  "dueDate": "2020/06/06"
}
```

##### Responses

`Status: 201 Created`

`Status: 400 BadRequest`

### Update to do

`PUT /to-dos/:id`

##### Body

```json
{
  "title": "Buy cheese",
  "dueDate": "2020/06/07"
}
```

##### Responses

`Status: 204 NoContent`

`Status: 400 BadRequest`

`Status: 404 NotFound`

### Delete to do

`DELETE /to-dos/:id`

##### Responses

`Status: 204 NoContent`

`Status: 404 NotFound`

#### Requirements:

- To create and update a to do item the dueDate needs to be a future date.
- The to do have a status wich can be ToDo, Expired and Done and sub-items.
- Create an api with at least 3 layers (api, business, data).
- Use MySql as database and the repository pattern to access it (https://medium.com/thecodemonks/cautions-applying-repository-and-unit-of-work-patterns-with-dependency-injection-in-domain-driven-52fbe05bf9a5).
- Use dependency injection.
- Use swagger documentation.
- Create at least unit tests for the business layer.
