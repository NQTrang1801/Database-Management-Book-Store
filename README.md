# Bookstore Management System - Database Transactions and Concurrency Handling

## Overview
The **Bookstore Management System** is designed to efficiently manage books, employees, customers, invoices, and suppliers. The system ensures **data integrity**, **security**, and **efficient business operations** through robust transaction management and concurrency handling.

## Features
- **CRUD Operations**: Add, delete, update, and search for books, employees, customers, invoices, and suppliers.
- **User Authentication & Role Management**: Secure login with access control.
- **Invoice & Order Management**: Generate invoices and purchase orders.
- **Automatic Updates & Reports**: Keeps track of stock, total sales, and customer points.
- **Transaction Management**: Ensures consistency through stored procedures and triggers.

## Database Transactions & Concurrency Control
### **1. Transaction Management**
- Automatic **ID generation** for new records.
- Auto-update **total invoice amount** and **customer loyalty points** after purchases.
- Auto-update **book stock levels** upon sales and restocking.
- Maintain **data integrity** by enforcing constraints and relationships.

### **2. Triggers Implementation**
Several **PL/SQL triggers** ensure data consistency:
- **Stock Updates:** Adjust stock count when books are sold.
- **Data Validation:** Prevent invalid entries (e.g., future birthdates for customers).
- **Loyalty Points System:** Update customer classification (Regular, VIP) based on spending history.
- **Invoice Integrity:** Prevent incorrect calculations before finalizing an invoice.

### **3. Concurrency Control & Data Consistency**
Handling multiple users accessing the database simultaneously:
- **Lost Update:** Prevented using locking mechanisms to avoid accidental data overwrites.
- **Dirty Read:** Transactions are isolated to prevent reading uncommitted changes.
- **Non-Repeatable Read:** Ensures stability in multiple reads within the same transaction.
- **Phantom Read:** Implemented with serializable isolation level to maintain data accuracy.

## Technologies Used
- **Database**: Oracle SQL
- **Programming Languages**: PL/SQL
- **Frameworks**: SQL Triggers, Procedures, Functions
- **Security Measures**: Role-based authentication and transaction isolation

## Contributors
- **Nguyen Quoc Trang** - 21521556
- **Nguyen Trieu Vy** - 21522812
- **Huynh Le Phong** - 21520086

