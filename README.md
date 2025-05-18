

# Coffee Shop Challenge

A Python project to model a simple coffee shop ordering system, implementing object relationships and aggregate methods.

## Project Structure


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

## Models

## Customer
- **Attributes:**
  - `name` (1–15 characters, str)
- **Methods:**
  - `orders()` - Returns all orders for the customer.
  - `coffees()` - Returns unique list of coffees ordered by the customer.
  - `create_order(coffee, price)` - Creates a new order linked to this customer.

## Coffee
- **Attributes:**
  - `name` (at least 3 characters, str, immutable)
- **Methods:**
  - `orders()` - Returns all orders for this coffee.
  - `customers()` - Returns unique list of customers who ordered this coffee.
  - `num_orders()` - Returns total number of orders for this coffee.
  - `average_price()` - Returns the average price of all orders for this coffee.

## Order
- **Attributes:**
  - `customer` (Customer instance)
  - `coffee` (Coffee instance)
  - `price` (1.0–10.0, float, immutable)
- **Relationships:**
  - `customer` - Returns the customer instance linked to the order.
  - `coffee` - Returns the coffee instance linked to the order.

## Getting Started

1. Clone the repository:
   ```bash
   git clone git@github.com:2david-kariuki/coffee-shop-challenge.git
   cd coffee-shop-challenge


Set up your Python environment:

Bash

pipenv install
pipenv shell
Run the tests:

Bash

pytest tests/
License
This project is licensed under the MIT License.