# Tactical DDD

## Introduction

Welcome to the "Tactical DDD" project. This project serves as a case study, demonstrating the principles of Domain-Driven Design (DDD) applied to a simple solution encompassing three core domains: Customers, Products, and Orders.

The purpose is to explore the intricacies of DDD by providing a practical example, illustrating the implementation of domains and infrastructural components. This environment bridges the gap between theory and practice, offering insights into how these elements interact in a real-world application.

By delving into "Tactical DDD", you will discover the powerful design benefits that DDD brings to software development. This project is a valuable resource for developers at all levels, from beginners to veterans.

Feel free to navigate through the project, inspect the code, and share your questions, suggestions, or feedback. All contributions are welcome!

## Stack

In the "Tactical DDD" project, we have chosen a combination of technologies to ensure robustness, scalability, and maintainability. Here’s an overview of our technology stack:

### TypeScript

TypeScript, a strongly typed superset of JavaScript, is our main programming language. It compiles to plain JavaScript and introduces static types, interfaces, and classes to enhance reliability and development experience. These features align well with our aim to implement Domain-Driven Design (DDD).

### Sequelize

For our backend infrastructure, we use Sequelize, a promise-based ORM for Node.js supporting various databases including Postgres, MySQL, MariaDB, SQLite, and Microsoft SQL Server. It provides solid transaction support, relations, eager and lazy loading, and more.

For this study case, Sequelize is utilized with an in-memory database to simulate database operations without requiring a separate database setup, making the project more accessible for quick setup and exploration.

### Jest

Testing is a critical part of our application. We use Jest, a delightful JavaScript testing framework focusing on simplicity. It offers features like a simple API for structuring tests, snapshots for UI changes, setup and teardown mechanisms, and parallel test execution.

Jest enables us to write both unit and integration tests, supporting Test-Driven Development (TDD), a core practice in the DDD approach.

## Project Structure

The project is organized according to DDD principles, divided into Domain and Infrastructure layers:

### Domain

#### Checkout
- **Entity**: 
  - `Order`: Represents an order.
  - `OrderItem`: Represents an item within an order.
- **Repository**:
  - `OrderRepository`: Interface for order data access.
- **Service**:
  - `OrderService`: Handles order-related business logic.
- **Factory**:
  - `OrderFactory`: Creates order instances.

#### Customer
- **Entity**:
  - `Customer`: Represents a customer.
  - `Address`: Value object representing a customer's address.
- **Repository**:
  - `CustomerRepository`: Interface for customer data access.
- **Factory**:
  - `CustomerFactory`: Creates customer instances.

#### Product
- **Entity**:
  - `Product`: Represents a product.
- **Repository**:
  - `ProductRepository`: Interface for product data access.
- **Service**:
  - `ProductService`: Handles product-related business logic.
- **Event**:
  - `ProductCreatedEvent`: Event triggered when a product is created.
  - `SendEmailWhenProductIsCreatedHandler`: Event handler for sending an email when a product is created.
- **Factory**:
  - `ProductFactory`: Creates product instances.

### Infrastructure

#### Order / Repository / Sequelize
- **OrderRepository**: Concrete implementation of the order repository.
- **OrderModel**: Sequelize model for order.

#### Customer / Repository / Sequelize
- **CustomerRepository**: Concrete implementation of the customer repository.
- **CustomerModel**: Sequelize model for customer.

#### Product / Repository / Sequelize
- **ProductRepository**: Concrete implementation of the product repository.
- **ProductModel**: Sequelize model for product.

## Conclusion

Thank you for your interest in the "Tactical DDD" project. We appreciate your time and attention, and warmly invite your suggestions or constructive criticism. Feel free to raise issues, submit pull requests, or share your thoughts. Your contribution helps us improve and learn.

Once again, thank you, and happy exploring!
