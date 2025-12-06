# Inventory Management API

A lightweight RESTful API built with **Node.js**, **Express**, and **SQLite** for managing product inventory data. This application enables users to perform CRUD (Create, Read, Update, Delete) operations on product records, tracking details such as batch numbers, expiration dates, and stock quantities.

## 🚀 Features

* **Product Management:** Store and retrieve detailed product information including brand, category, and pricing.
* **Database Integration:** Uses **SQLite3** for a self-contained, serverless, and zero-configuration database engine.
* **RESTful Endpoints:** Clean API architecture supporting GET, POST, PUT, and DELETE methods.
* **Automatic Initialization:** The database table is automatically created and seeded with sample data upon the first run.

## 🛠️ Tech Stack

* **Runtime:** Node.js
* **Framework:** Express.js
* **Database:** SQLite3
* **Middleware:** Body-Parser

## ⚙️ Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/inventory-management-api.git](https://github.com/yourusername/inventory-management-api.git)
    cd inventory-management-api
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```
    *(Note: Ensure your `package.json` includes `express`, `sqlite3`, and `body-parser`)*

3.  **Start the server:**
    ```bash
    node server.js
    ```
    The server will start on port **8080**.
    
    > **Console Output:** `Server is running on 8080` and `Connected to the Database`

## wq API Documentation

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| **GET** | `/api/products` | Retrieve a list of all products in the inventory. |
| **POST** | `/api/products` | Add a new product to the database. |
| **PUT** | `/api/products` | Update details of an existing product. |
| **DELETE** | `/api/product/delete/:id` | Remove a product by its ID. |

### Example JSON Payload (POST/PUT)

```json
{
    "productName": "Basmathi Rice",
    "description": "High-quality imported rice",
    "category": "Grains",
    "brand": "CIC",
    "expireDate": "2025.12.31",
    "manufacturedDate": "2024.01.01",
    "batchNumber": 1024,
    "unitPrice": 500,
    "quantity": 50,
    "createdDate": "2024.01.02"
}
