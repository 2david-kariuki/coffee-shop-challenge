# Coffee Shop Challenge
A Python project implementing a coffee shop ordering system with Customer, Coffee, and Order models, built to practice object-oriented programming and relationships.
Project Structure
coffee-shop-challenge/
├── Pipfile
├── debug.py
├── customer.py
├── coffee.py
├── order.py
└── tests/
    ├── customer_test.py
    ├── coffee_test.py
    └── order_test.py

Setup

Clone the repository:
git clone git@github.com:2david-kariuki/coffee-shop-challenge.git
cd coffee-shop-challenge


Set up the Python environment:
pipenv install
pipenv shell



Features
Models

Customer: Stores a name (string, 1–15 characters). Supports creating orders and retrieving their orders/coffees.
Coffee: Stores an immutable name (string, 3+ characters). Tracks orders and customers.
Order: Links a Customer, Coffee, and price (float, 1.0–10.0). Immutable price with type/range validation.

Relationships

Order: Access associated Customer and Coffee instances.
Customer: List all orders and unique coffees ordered.
Coffee: List all orders and unique customers.

Aggregates

Customer.create_order(coffee, price): Creates a new order.
Coffee.num_orders(): Counts total orders for the coffee.
Coffee.average_price(): Calculates the mean price of orders (returns 0 if none).

Usage
Run debug.py to test the implementation or explore the tests/ directory for unit tests.
