# Contact API Spec

## Create Contact

Endpoint: POST /api/contact

Request He  ader :

- X-API-TOKEN: Token {Mandatory}
  Response Body (Success):

Request Body:
```json
{
  "firstName": "Ahmad",
  "lastName": "Jaelani Sidiq",
  "email": "ahmad.zaelan@gmail.com",
  "phone": "085772670969"
}
```

Response Body (Success):
```json
{
  "data": {
    "id": "randomstring",
    "firstName": "Ahmad",
    "lastName": "Jaelani Sidiq",
    "email": "ahmad.zaelan@gmail.com",
    "phone": "085772670969"
  }
}
```

Response Body (Failed):
```json
{
  "errors": "error on store data" 
}
```

## Update Contact

Endpoint: PUT /api/contact/{id}

Request Header :

- X-API-TOKEN: Token {Mandatory}
  Response Body (Success):

Request Body:
```json
{
  "firstName": "Ahmad",
  "lastName": "Jaelani Sidiq",
  "email": "ahmad.zaelan@gmail.com",
  "phone": "085772670969"
}
```

Response Body (Success):
```json
{
  "data": {
    "id": "randomstring",
    "firstName": "Ahmad",
    "lastName": "Jaelani Sidiq",
    "email": "ahmad.zaelan@gmail.com",
    "phone": "085772670969"
  }
}
```
Response Body (Failed):
```json
{
  "errors": "error on update data" 
}
```

## Get Contact

Endpoint: GET /api/contact/{id}

Request Header :

- X-API-TOKEN: Token {Mandatory}
  Response Body (Success):

Request Body:

Response Body (Success):
```json
{
  "data": {
    "id": "randomstring",
    "firstName": "Ahmad",
    "lastName": "Jaelani Sidiq",
    "email": "ahmad.zaelan@gmail.com",
    "phone": "085772670969"
  }
}
```
Response Body (Failed):
```json
{
  "errors": "contact not found" 
}
```

## Search Contact

Endpoint: POST /api/contact

Query Param:

- name: String
- phone: String
- email: String
- page : Integer
- size : Integer

Request Header :

- X-API-TOKEN: Token {Mandatory}
  Response Body (Success):

Request Body:

Response Body (Success):
```json
{
  "data": [
    {
      "id": "randomstring",
      "firstName": "Ahmad",
      "lastName": "Jaelani Sidiq",
      "email": "ahmad.zaelan@gmail.com",
      "phone": "085772670969"
    }
  ],
  "paging": {
    "currentpage": 0,
    "totalPage": 10,
    "size": 10
  }
}
```

Response Body (Failed):

## Delete Contact

Endpoint: DELETE /api/contact/{id}

Request Header :

- X-API-TOKEN: Token {Mandatory}
  Response Body (Success):

Request Body:

Response Body (Success):
```json
{
  "data": "success" 
}
```

Response Body (Failed):
```json
{
  "errors": "error on delete contact" 
}
```