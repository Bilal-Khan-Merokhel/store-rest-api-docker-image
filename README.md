
# Flask-Store_Rest_Api
Store REST API

## Installation
- Clone the repo ```git clone https://github.com/Bilal-Khan-Merokhel/store-rest-api-docker-image.git```.
- Change dir to  ```cd /store-rest-api-docker-image```.
- Fetch from docker hub via ```docker pull bilalkhan/store_rest_api:latest```.
- RUN ```docker run -d -p 5000:5000 bilalkhan/store_rest_api:latest```.
- Go to ```127.0.0.1``` and you'll see 404 not found.

## Description
  You can use postman or curl to fetch these endpoints.
  but before that make sure to use your mailgun domain and api key.
  Or you can use any other email service

## Endpoints
### Auth Endpoints
- ```Method POST /api/v1/user/register```
- ``` Method GET /api/v1/user/confirmation/{confirmation_token}/confirmed```
- ``` Method GET /api/v1/confirmation/user/{user_id}```
- ``` Method POST /api/v1/user/login```
- ``` Method GET /api/v1/user/{user_id}```
- ```Method POST /api/v1/user/token/refresh```
- ``` Method POST /api/v1/user/logout```

### Posting and fetching store names with items in it
- ``` Method POST /api/v2/store/{store_name}```
- ``` Method GET /api/v2/stores```

### Posting and fetching items
- ``` Method POST /api/v2/item/{item_name}```
- ```Method GET /api/v2/items```

