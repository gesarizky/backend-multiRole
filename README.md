# Backend For MultiRole Website

## How to install and run

### Running Programm

1. Clone the repository
2. Install dependencies

    ```bash
    npm install
    ```

3. Update your credential in .env
4. To Start your Program

    ```bash
    npm run start
    ```

### Install to Docker

1. make sure your docker server is running
2. Install your program to docker server

    ```bash
    npm run docker:windows //for Windows
    npm run docker:linux //for Linux
    ```

## API Endpoints

### AUTH

- `POST /login` - login with json body :

    ```bash
    {
    "email":"admin@gmail.com",
    "password": "123456"
    }
    ```

- `DELETE /logout` - logout
- `POST /me - Display details of who is logged in to the website

### USER

- `POST /users` - create user with json body :

    ```bash
    {
    "name":"john",
    "email":"john@gmail.com",
    "password": "123456",
    "confPassword":"123456",
    "role":"user"
    }
    ```

- `PATCH /users/:id` - update user with json body :

    ```bash
    {
    "name":"john updated",
    "email":"john@gmail.com",
    "password": "",
    "confPassword":"",
    "role":"user"
    }
    ```

- `DELETE /users/:id` - delete specific user
- `GET /users` - Get all users
- `GET /users/:id` - Get specific users

### PRODUCT

- `POST /products` - create product with json body :

    ```bash
    {
    "name":"product 6",
    "price": 991
    }
    ```

- `PATCH /products/:id` - update product with json body :

    ```bash
    {
    "name":"product updated",
    "price": 888
    }
    ```

- `DELETE /products/:id` - delete specific product
- `GET /products` - Get all products
- `GET /products/:id` - Get specific products

## Postman Collection

Import the provided Postman Collection for testing the API endpoints.

### How to Import Postman Collection

1. Open Postman
2. Click on `Import` button
3. Select the file `.postman_collection.json` from the `postman` directory
4. Start testing the endpoints

## Postman Collection File

The Postman Collection file is located in the `postman` directory and is named `.postman_collection.json`.
