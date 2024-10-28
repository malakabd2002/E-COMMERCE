Here's a README file for your Simple E-Commerce Management System project:


---

Simple E-Commerce Management System

Description

This project is a Simple E-Commerce Management System built with Laravel 10 that provides a RESTful API for managing users, products, categories, and orders. It allows users to perform CRUD operations on products, categories, and orders, with user roles to differentiate between admin and customer privileges. The project is built using clean code principles and the repository design pattern.

Key Features:

User Roles: Role-based access control for admin and customer users.

CRUD Operations: Full CRUD support for managing products, categories, and orders.

Category Association: Each product can belong to multiple categories and vice versa.

Order Management: Customers can place orders, each containing one product.

Soft Deletes: Products are soft-deleted to allow recovery if needed.

Middleware Protection: Admin dashboard access is restricted to admin users only.

API Authentication: Secure API using Laravel Sanctum for authenticated access.

Filtering and Sorting: List products by category or get a full list.

Repository Design Pattern: Ensures clean separation of concerns.

Form Requests: Handles validation with custom form request classes.

API Response Service: Provides unified responses for all API endpoints.

Pagination: Paginated results for better performance and usability.

Resources: Structured and consistent API responses using Laravel resources.

Seeders: Populates the database with initial data for testing and development.


Technologies Used:

Laravel 10

PHP

MySQL

XAMPP (for local development environment)

Composer (PHP dependency manager)

Postman Collection: Includes all API requests for testing and interacting with the API.



---

Installation

Prerequisites

Ensure you have the following installed on your machine:

XAMPP: For running MySQL and Apache servers locally.

Composer: PHP dependency management.

PHP: Required for running Laravel.

MySQL: Database for the project.

Postman: For testing the API requests.


Steps to Run the Project

1. Clone the Repository

git clone https://github.com/YourUsername/Ecommerce-Management-System.git


2. Navigate to the Project Directory

cd ecommerce-management-system


3. Install Dependencies

composer install


4. Create Environment File

cp .env.example .env

Update the .env file with your database configuration (MySQL credentials, database name, etc.).


5. Generate Application Key

php artisan key:generate


6. Run Migrations

php artisan migrate


7. Seed the Database

php artisan db:seed


8. Run the Application

php artisan serve


9. Test API Endpoints via Postman
Import the Postman collection to test the API endpoints: Postman Collection Link




---

API Endpoints

This project includes several API endpoints for managing users, products, categories, and orders. Below are some of the primary endpoints:

Authentication Endpoints:

POST /api/register: Register a new user.

POST /api/login: Log in an existing user.


Product Endpoints:

GET /api/products: List all products.

GET /api/products/{category}: List products by category.

POST /api/products: Add a new product (Admin only).

PUT /api/products/{id}: Update a product (Admin only).

DELETE /api/products/{id}: Soft delete a product (Admin only).


Order Endpoints:

POST /api/orders: Place a new order (Customer only).

GET /api/orders: View all orders (Admin only).



Notes

Admin Users: Can manage products, categories, and view orders.

Customer Users: Can fetch products and place orders.



---

Project Structure

This project follows a repository design pattern, with repositories and services to ensure a clean separation of concerns. Custom request classes handle validation, and Laravel resources are used to format API responses.

Repositories: Provides a layer for managing database operations.

Services: Contains business logic and communicates with repositories.

Middleware: Protects routes and restricts access based on user roles.



---

License
