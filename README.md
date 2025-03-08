This repository contains the python & git bash scripts for creating a database for MySql, initializing it & managing it with MySql Workbench.
This repository also contains the python scripts for schemas created with Flask & Marshmallow.

CRUD Endpoints
User Endpoints:
GET /users: Retrieve all users
GET /users/<id>: Retrieve a user by ID
POST /users: Create a new user
PUT /users/<id>: Update a user by ID
DELETE /users/<id>: Delete a user by ID
Product Endpoints:
GET /products: Retrieve all products
GET /products/<id>: Retrieve a product by ID
POST /products: Create a new product
PUT /products/<id>: Update a product by ID
DELETE /products/<id>: Delete a product by ID
Order Endpoints:
POST /orders: Create a new order (requires user ID and order date)
PUT /orders/<order_id>/add_product/<product_id>: Add a product to an order (prevent duplicates)
DELETE /orders/<order_id>/remove_product/<product_id>: Remove a product from an order
GET /orders/user/<user_id>: Get all orders for a user
GET /orders/<order_id>/products: Get all products for an order

Project Structure:
ecommerce_api_project/
│
├── app.py                # Main Flask app
├── models.py             # SQLAlchemy models
├── schemas.py            # Marshmallow schemas
├── requirements.txt      # List of dependencies
└── postman_collection.json # Postman collection file

Setup instructions:
Clone the repository:

bash
Copy
git clone https://github.com/your-username/ecommerce-api.git
Navigate to the project folder:

bash
Copy
cd ecommerce-api
Set up a virtual environment and install dependencies:

bash
Copy
python3 -m venv venv
source venv/bin/activate  # On Mac/Linux
.\venv\Scripts\activate  # On Windows
pip install -r requirements.txt
Run the Flask app:

bash
Copy
python app.py
