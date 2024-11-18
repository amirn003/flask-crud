# CRUD with Flask

This project provides a simple CRUD API for managing products using Flask.


## Installation

1. Install the required packages:

    ```sh
    python3 -m pip install flask flask_cors
    ```

## Running the Application

1. Run the app:

    ```sh
    python3 products.py
    ```

## API Endpoints

### Get All Products

- **URL:** `/products`
- **Method:** `GET`
- **Description:** Returns a list of all products.

    ```sh
    curl http://localhost:5000/products
    ```

### Get a Product by ID

- **URL:** `/products/{id}`
- **Method:** `GET`
- **Description:** Returns a product based on the product ID.

    ```sh
    curl http://localhost:5000/products/144
    ```

### Add a Product

- **URL:** `/products`
- **Method:** `POST`
- **Description:** Adds a new product to the list.

    ```sh
    curl -X POST -H "Content-Type: application/json" \
    -d '{"id": 145, "name": "Pen", "price": 2.5}' \
    http://localhost:5000/products
    ```

### Update a Product

- **URL:** `/products/{id}`
- **Method:** `PUT`
- **Description:** Updates an existing product based on the product ID.

    ```sh
    curl -X PUT -H "Content-Type: application/json" \
    -d '{"name": "Updated Pen", "price": 3.0}' \
    http://localhost:5000/products/145
    ```

### Delete a Product

- **URL:** `/products/{id}`
- **Method:** `DELETE`
- **Description:** Deletes a product based on the product ID.

    ```sh
    curl -X DELETE http://localhost:5000/products/145
    ```

## Testing

You can test the API using the provided `curl` commands or any API testing tool like Postman.

## Swagger Documentation

The API is documented using Swagger. You can find the Swagger JSON file in the `static` directory.
