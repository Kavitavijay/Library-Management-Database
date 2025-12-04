# Library-Management-Database
An Oracle SQL project that models a functional Library Management Database. Includes structured table creation , relational constraints, 100% executable insert statements, and real-world queries to track issued, overdue, and low-stock books. Designed to showcase SQL skills including joins, GROUP BY operations, and date-based condition

---

## 📘 Project Objective
To design and query a relational database that manages:
- Books and their availability
- Library members
- Book issue details (who borrowed which book and when)
- Tracking overdue books

All SQL commands are written to work inside the default **SCOTT** schema without requiring special privileges.

---

## 🛠 Database Schema

### **1️⃣ BOOKS Table**
Stores book details and available copies.
- `book_id`  
- `title`  
- `author`  
- `category`  
- `copies_available`

### **2️⃣ MEMBERS Table**
Stores library member information.
- `member_id`  
- `name`  
- `email`  
- `phone`

### **3️⃣ ISSUED_BOOKS Table**
Tracks issued books and return status.
- `issue_id`  
- `member_id` (FK → MEMBERS)  
- `book_id` (FK → BOOKS)  
- `issue_date`  
- `due_date`  
- `return_date`

---

## 📥 Sample Data
The project includes sample entries for:
- Books  
- Members  
- Issued books  

These records help test and demonstrate all SQL queries.

---

## 🔍 SQL Queries Included

### ✔ **Issued Book Report**
Shows which member borrowed which book and when.

### ✔ **Books Issued Count**
Counts how many books each member has issued.

### ✔ **Low Stock Books**
Finds books with fewer than 3 copies available.

### ✔ **Overdue Books**
Lists books not returned past their due date.

These queries help understand joins, filtering, GROUP BY, and date comparisons.

---
