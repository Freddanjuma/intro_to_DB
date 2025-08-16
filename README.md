# í³š ALX Book Store Database

This project is part of the **Intro to Databases** module.  
It defines a MySQL schema for an **online bookstore**.

---

## í·‚ Database Name
`alx_book_store`

---

## í³Œ Schema Overview

### 1. Authors
Stores information about authors.
- `author_id` (Primary Key)
- `author_name` (VARCHAR 215)

### 2. Books
Stores information about books.
- `book_id` (Primary Key)
- `title` (VARCHAR 130)
- `author_id` (Foreign Key â†’ Authors)
- `price` (DOUBLE)
- `publication_date` (DATE)

### 3. Customers
Stores information about customers.
- `customer_id` (Primary Key)
- `customer_name` (VARCHAR 215)
- `email` (VARCHAR 215, Unique)
- `address` (TEXT)

### 4. Orders
Stores information about customer orders.
- `order_id` (Primary Key)
- `customer_id` (Foreign Key â†’ Customers)
- `order_date` (DATE)

### 5. Order_Details
Stores details of each book in an order.
- `orderdetailid` (Primary Key)
- `order_id` (Foreign Key â†’ Orders)
- `book_id` (Foreign Key â†’ Books)
- `quantity` (DOUBLE)

---

## íº€ Usage
1. Open MySQL shell.
2. Run:
   ```sql
   SOURCE alx_book_store.sql;

