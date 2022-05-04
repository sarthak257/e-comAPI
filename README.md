
# Eccomerce-API

This is a bare-bones example of a Eccomerce application providing a REST API for CRUD
.

# How to setup on local machine
1. check pre-requisits by these.
```go
node --version
npm --version
git --version
```
2. Now clone this repository
```go
git clonehttps://github.com/sarthak257/e-comAPI
```
3. Change directory to Ecomerce-API
```go
cd Ecommerce-API/
```

3. Install dependencies
```go
npm i --save
```
4. Start mongo db this command may differ... system to system.
```go
sudo systemctl start mongod
```
5. That's... it  run the application
```go
npm start
```
6. click [here](http://localhost:8000) or link in terminal to access your application.




# REST API

The REST API to the example app is described below.
`GET /products/`

  GET http://localhost:8000/v1/products HTTP/1.1

  ### Response

  HTTP/1.1 200 OK

X-Powered-By: Express

Content-Type: application/json; charset=utf-8

Content-Length: 199

ETag: W/"c7-a3iICZCv9q2bAAChM6PUPuGQbEM"

Connection: close


# Create a new product

### Request

`POST /product/create`

POST http://localhost:8000/v1/products/create HTTP/1.1

Content-Type: application/x-www-form-urlencoded

name=
&quantity=

## Response

HTTP/1.1 200 OK

X-Powered-By: Express

Content-Type: application/json; charset=utf-8

Content-Length: 40

ETag: W/"28-jMlj/AjT2uXiqUcTdIfYf/TaCaM"

Connection: close

{
  "product": {
    "name": "Ipod",
    "quantity": 1
  }

# Delete a product

`Delete/product/:id`

http://localhost:8000/v1/products/:id 

HTTP/1.1 200 OK

X-Powered-By: Express

Content-Type: application/json; charset=utf-8

Content-Length: 29

ETag: W/"1d-ShlPhHook6Z47t9nJNwXXKnmIZ8"

Connection: close

{
  "message": "product deleted"
}

# Update A quantity


### Request

`POST /products/:id/update_quantity/?number=`
http://localhost:8000/v1/products/id:/update_quantity/?number= HTTP/1.1

### Response

HTTP/1.1 200 OK

X-Powered-By: Express

Content-Type: application/json; charset=utf-8

Content-Length: 109

ETag: W/"6d-8nqm8qkV4YuiYHpNtk7+/y+fnhI"

{
  "product": {
    "id": "6262d1b31028071986219372",
    "name": "Iphone",
    "quantity": 100
  },
  "message": "updated successfully"
}


# View all products

### Request
`GET /product/`

http://localhost:8000/v1/products 

### Response

HTTP/1.1 200 OK

X-Powered-By: Express

Content-Type: application/json; charset=utf-8

Content-Length: 384

ETag: W/"180-Abxv8rjHaumplRicGh8iL99FP4c"

Connection: close