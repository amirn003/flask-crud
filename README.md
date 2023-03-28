# CRUD with Flask

1. Install the required packages

    python3 -m pip install flask flask_cors

2. Run the app

    python3 products.py

3. Test your app

    curl http://localhost:5000/products

4. Add a product to the list

    curl -X POST -H "Content-Type: application/json" \
    -d '{"id": 145, "name": "Pen", "price": 2.5}' \
    http://localhost:5000/products