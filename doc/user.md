# User API Spec

## Register User

- Endpoint : POST /api/users

Request Body:

```json
{
  "username": "",
  "password": "",
  "name": ""
}
```

Response Body (Success):

```json
{
  "data": "ok"
}
```

Response Body (Failed,401):

```json
{
  "errors": "username or password wrong"
}
```

## Login User

- Endpoint : POST /api/auth/login

Request Body:

```json
{
  "username": "ahmad",
  "password": "rahasia"
}
```

Response Body (Success):

```json
{
  "data": {
    "token": "jwttoken",
    "expiredat": 2312121
  }
}
```

Response Body (Failed,401):

```json
{
  "errors": "username or password wrong"
}
```

## Get User

- Endpoint : GET /api/users/current

Request Header :

- X-API-TOKEN: Token {Mandatory}

Response Body (Success):

```json
{
  "data": {
    "username": "ahmadjaelani",
    "name": "Ahmad Jaelani Sidiq"
  }
}
```

Response Body (Failed,401):

```json
{
  "errors": "Unauthorized"
}
```

## Update User

Request Header :

- X-API-TOKEN: Token {Mandatory}

- Endpoint : PATCH /api/users/current

Request Body:

```json
{
  "name": "Ahmad jaelani sidiq",
  "password": "new password"
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "ahmadjaelani",
    "name": "Ahmad Jaelani Sidiq"
  }
}
```

Response Body (Failed,401):

```json
{
  "errors": "Unauthorized"
}
```


## Logout User

Endpoint : DELETE /api/auth/logout

Request Header :

- X-API-TOKEN: Token {Mandatory}
  Response Body (Success):

```json
{
  "data": "sucess"
}
```