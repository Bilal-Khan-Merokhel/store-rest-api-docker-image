

# Flask Rest Api
Store REST API which contains CRUD and Auth mechanism with confirmation tokens.
once you register go to this endpoint ``` Method GET /api/v1/confirmation/user/{user_id}``` and get your confirmation token after that
go to this endpoint ``` Method GET /api/v1/user/confirmation/{confirmation_token}/confirmed```
 and replace your confirmation token so you can confirm your account.


## Installation
- Fetch from docker hub via ```docker pull bilalkhan/store_rest_api:latest```.
- RUN ```docker run -d -p 80:5000 bilalkhan/store_rest_api:latest```.
- Go to ```127.0.0.1``` and you'll see **404** error, below are the endpoints.

## Description
  You can use postman or curl to fetch these endpoints.
  but before that make sure to use your mailgun domain and api key.
  Or you can use any other email service

## Endpoints
### Auth Endpoints
- ```Method POST /api/v1/user/register```

  ```
  {
     "username":test_username,
     "email": "this.rex@protonmail.com",
     "password":1234       
  }
  ```
- ``` Method GET /api/v1/user/confirmation/{confirmation_token}/confirmed```
- ``` Method GET /api/v1/confirmation/user/{user_id}```
- ``` Method POST /api/v1/user/login```

  ```
  {

    "username" : "bilalkhan",
    "password" : "1234"

  }
  ```
- ``` Method GET /api/v1/user/{user_id}```
- ``` Method POST /api/v1/user/token/refresh```
- ``` Method POST /api/v1/user/logout```

### Posting and fetching store names with items in it
- ``` Method POST /api/v2/store/{store_name}```
- ``` Method GET /api/v2/stores```

### Posting/Updating and fetching items
- ``` Method POST /api/v2/item/{item_name}```

  ```
  {

    "price": 12.99,
    "store_id": 1

  }
  ```
- ``` Method PUT /api/v2/item/{item_name}```

  ```
  {
    "price": 20.99
  }
  ```

- ```Method GET /api/v2/items```
