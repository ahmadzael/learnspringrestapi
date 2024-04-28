# Address API Spec

## Create Address

Endpoint: POST /api/contact/{idContact}/addresses

Request Header :

- X-API-TOKEN: Token {Mandatory}
  Response Body (Success):

Request Body:
```json
{
 "street": "jalan bintaro",
  "city": "Tangerang Selatan",
  "prvince": "Banten",
  "country": "Indonesia",
  "postalCode": "123456"
}
```

Response Body (Success):
```json
{
  "id": "stringID",
 "street": "jalan bintaro",
  "city": "Tangerang Selatan",
  "prvince": "Banten",
  "country": "Indonesia",
  "postalCode": "123456"
}
```

Response Body (Failed):
```json
{
  "errors": "Contact is not found" 
}
```

## Update Address

Endpoint: PUT /api/contact/{idContact}/addresses/{idAddress}

Request Header :

- X-API-TOKEN: Token {Mandatory}
  Response Body (Success):

Request Body:
```json
{
  "id": "stringID",
  "street": "jalan bintaro",
  "city": "Tangerang Selatan",
  "prvince": "Banten",
  "country": "Indonesia",
  "postalCode": "123456"
}
```

Response Body (Success):
```json
{
  "id": "stringID",
  "street": "jalan bintaro",
  "city": "Tangerang Selatan",
  "prvince": "Banten",
  "country": "Indonesia",
  "postalCode": "123456"
}
```
Response Body (Failed):
```json
{
  "errors": "error on update data" 
}
```

## Get Address

Endpoint: GET /api/contact/{idContact}/addresses/{idAddresses}

Request Header :

- X-API-TOKEN: Token {Mandatory}
  Response Body (Success):

Request Body:

Response Body (Success):
```json
{
  "id": "stringID",
  "street": "jalan bintaro",
  "city": "Tangerang Selatan",
  "prvince": "Banten",
  "country": "Indonesia",
  "postalCode": "123456"
}
```
Response Body (Failed):
```json
{
  "errors": "addresses not found" 
}
```

## List Address

Endpoint: DELETE /api/contact/{idContact}addresses/{idAddresses}

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
  "errors": "error on delete addresses" 
}
```

Response Body (Success):
```json
{
  "data": [
    {
      "id": "stringID",
      "street": "jalan bintaro",
      "city": "Tangerang Selatan",
      "prvince": "Banten",
      "country": "Indonesia",
      "postalCode": "123456"
  }
  ]
}
```
Response Body (Failed):
```json
{
  "errors": "addresses not found" 
}
```