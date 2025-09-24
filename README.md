# Database_Phase1_Final_Project
📦 E-commerce Database Management System
📖 Project Overview
This project is the Final Assignment for Week 8 of the Database Design & Programming with SQL module at PLP Academy. It demonstrates the design and implementation of a relational database system using MySQL, along with an Entity Relationship Diagram (ERD) to visualize the schema.

The database models a simple E-commerce Store, covering customers, products, orders, and payments. It showcases one-to-one, one-to-many, and many-to-many relationships.

🎯 Objectives
Design a full-featured relational database schema.

Implement the schema in MySQL with proper constraints.

Demonstrate relationships between entities.

Provide a .sql file and ERD diagram as deliverables.

🗂 Database Schema
Entities
Customers: Stores customer details.

Products: Stores product catalog.

Orders: Records customer purchases.

OrderItems: Bridge table for many-to-many relationship between Orders and Products.

Payments: Records payments for orders.

Relationships
One-to-Many: Customers → Orders

Many-to-Many: Orders ↔ Products (via OrderItems)

One-to-One: Orders → Payments

🛠 SQL Implementation
The schema is implemented in the file: final_project.sql

Key features:

PRIMARY KEY, FOREIGN KEY, UNIQUE, and NOT NULL constraints.

Composite primary key in OrderItems.

Referential integrity enforced with foreign keys.

🧪 Sample Data
Example inserts are included in the .sql file to test the schema:

sql
INSERT INTO Customers (name, email, phone)
VALUES ('John Doe', 'john@example.com', '08012345678');

INSERT INTO Products (name, price, stock)
VALUES ('Laptop', 250000.00, 10),
       ('Headphones', 15000.00, 50);

INSERT INTO Orders (customer_id, order_date)
VALUES (1, '2025-09-24');

INSERT INTO OrderItems (order_id, product_id, quantity)
VALUES (1, 1, 1), (1, 2, 2);

INSERT INTO Payments (order_id, amount, payment_date)
VALUES (1, 280000.00, '2025-09-24');
🖼 ERD Diagram
The ERD diagram (ecommerce_erd.png) illustrates the database structure and relationships.

Customers (1) → (∞) Orders

Orders (∞) → (∞) Products (via OrderItems)

Orders (1) → (1) Payments

📤 Deliverables
final_project.sql → Database schema and sample data.

ecommerce_erd.png → ERD diagram.

README.md → Documentation (this file).

🚀 How to Run
Open MySQL Workbench or CLI.

Run the script:

sql
SOURCE final_project.sql;
Verify tables with:

sql
SHOW TABLES;
Query data, e.g.:

sql
SELECT * FROM Customers;