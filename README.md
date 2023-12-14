# E-commerce-Hub Command Line Interface (CLI)

## Author
### AARON KIPTOO

## Description:
The E-commerce-Hub CLI is a versatile command-line interface designed to facilitate the management of an e-commerce database. This project provides a set of commands to interact with different models, enabling users to seamlessly add, delete, update, and list items within the database. Additionally, the CLI includes a command to visually represent sales data through a simple sales chart, leveraging the Matplotlib library.


## Table of Contents

- [Getting Started](#getting-started)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Available Actions](#available-actions)
- [Database Structure](#database-structure)
- [Relationship](#relationship)
- [Graph](#graph)
- [Dependencies](#dependencies)
- [Contributing](#contributing)

## Getting Started

## Technologies Used

    * Python: Python is a popular high-level programming language known for its simplicity, readability, and versatility.

    * SQLAlchemy: SQLAlchemy is the Python SQL toolkit and Object Relational Mapper that gives application developers the full power and flexibility of SQL.
    It provides a full suite of well known enterprise-level persistence patterns, designed for efficient and high-performing database access, adapted into a simple and Pythonic domain language.

## Installation
To get started with project, follow these steps:

Clone the repository to your local machine using the following command:

    * git@github.com:arronkiptoo/-E-commerce-Hub.git

Navigate to the project directory:
    
    * cd -E-commerce-Hub.git

Install the required dependencies:

    * pipenv --python 3.9
    
    * pipenv install

    * pipenv shell

    * pip install SQLAlchemy

    * pip install plotly

    * pip install matplotlib

    * Sudo apt install alembic

## Usage
Running the Program

To start the Ecommerce Management CLI, open a terminal and run the cli.py script:

* bash

* python cli.py list-customers

## Available Actions

Once the CLI is running, you will be presented with a menu of actions to choose from. Each action corresponds to a specific operation in the school management system. Here are the available actions:

    1. list-customers

    2. add-customer

    3. delete-customer

    4. update-customer

    * (Repeat the pattern for other models: products, sales, inventory, inventory alerts, users, order details)

    5. display-sales-chart

    6. Quit: Exit the program.

## Database Structure

The E-commerce-Hub CLI project utilizes an SQLite database to manage information related to customers, products, sales, inventory, inventory alerts, users, and order details. The database structure and key relationships are outlined below:

    Customers (customers table):
        customer_id (Primary Key): Unique identifier for each customer.
        customer_name: Name of the customer.
        email: Email address of the customer.
        phone_number: Phone number of the customer.

    Products (products table):
        product_id (Primary Key): Unique identifier for each product.
        product_name: Name of the product.
        description: Description of the product.
        price: Price of the product.

    Sales (sales table):
        order_id (Primary Key): Unique identifier for each sales order.
        customer_id (Foreign Key referencing customers.customer_id): Reference to the customer associated with the sale.
        product_id (Foreign Key referencing products.product_id): Reference to the product sold.
        order_date: Date of the sales order.
        quantity_sold: Quantity of the product sold.
        unit_price: Unit price of the product at the time of sale.

    Inventory (inventory table):
        sproduct_id (Primary Key and Foreign Key referencing products.product_id): Reference to the product in inventory.
        quantity_in_stock: Quantity of the product currently in stock.

    Inventory Alerts (inventory_alerts table):
        alert_id (Primary Key): Unique identifier for each inventory alert.
        product_id (Foreign Key referencing products.product_id): Reference to the product associated with the alert.
        alert_date: Date when the alert was triggered.
        threshold_quantity: Quantity threshold that triggered the alert.
        current_quantity: Current quantity of the product at the time of the alert.

    Users (users table):
        user_id (Primary Key): Unique identifier for each user.
        username: Username of the user.
        password_hash: Hashed password of the user.
        role: Role of the user (admin or user).
        customer_id (Foreign Key referencing customers.customer_id): Reference to the customer associated with the user.
    
   Order Details (order_details table):
        order_detail_id (Primary Key): Unique identifier for each order detail.
        order_id (Foreign Key referencing sales.order_id): Reference to the sales order.
        product_id (Foreign Key referencing products.product_id): Reference to the product in the order.
        quantity: Quantity of the product in the order.
        subtotal: Subtotal for the product in the order.

For more detailed information about the database structure and relationships, please refer to the models.py file in the project.

## Relationship
https://dbdiagram.io/d/Ecommerce-Database-6576f02f56d8064ca0c9589d

## graph
![sales_chart](https://github.com/arronkiptoo/Restaurant-SQLAlchemy/assets/144256231/7d2a0e9c-c7b5-4896-ba4a-88edbe14dfea)

## Dependencies
    * Python 3.9 or higher is recommended for this program as it was developed in version 3.8 but should work on any newer

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

    1. Fork the project on GitHub.
    2. Create a new branch for your feature or bug fix.
    3. Make your changes and commit them.
    4. Push your changes to your fork.
    5. Submit a pull request to the original repository.