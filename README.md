WEEK 8 DATABASE ASSIGNMENT 
---

### 📄 `README.md`

```markdown
# Week-8-assignment-PLP

## 📘 Question One of Two: Library Management System Database (MySQL)

This repository contains the solution to **Question One** of the **Week 8 Assignment** for the Power Learn Project (PLP) Software Engineering track.

The objective was to **design and implement a full-featured relational database system using only MySQL**, based on a real-world use case.

---

## 📚 Project Overview

**Use Case Selected:** Library Management System

This system is designed to help manage the core operations of a typical library, including:

- Cataloging books by categories and authors
- Tracking members and staff
- Recording book borrowings and returns (loans)

---

## 🎯 Objectives Achieved

### ✅ Designed a well-structured relational database:
- Used **Primary Keys (PK)** and **Foreign Keys (FK)** to enforce integrity.
- Applied **constraints** such as `NOT NULL`, `UNIQUE`, and composite keys.
- Implemented **relationships**:
  - One-to-Many (1-M)
  - Many-to-Many (M-M)
  - Logical normalization for real-world data modeling

### ✅ Delivered:
- A single `.sql` file containing:
  - `CREATE TABLE` statements with proper structure
  - **Sample data** for all tables
  - Comments and explanations for clarity

---

## 🧱 Database Schema Overview

| Table         | Description                                       |
|---------------|---------------------------------------------------|
| `authors`     | Stores information about book authors             |
| `categories`  | Stores book genres/categories                     |
| `books`       | Stores book details, including category           |
| `book_author` | Maps books to their authors (Many-to-Many)        |
| `members`     | Stores registered library members                 |
| `staff`       | Stores library staff information                  |
| `loans`       | Records book loan transactions                    |

---

## 🗂️ Files Included

- `library_management_system.sql`  
  Contains:
  - Database creation statement
  - All table creation scripts
  - Sample `INSERT` data
  - Well-commented explanations

---

## 🛠️ How to Use / Run This Project

To use the database:

### 💻 Requirements
- MySQL installed (local server or hosted)
- MySQL Workbench, phpMyAdmin, or any SQL client

### 🧪 Steps to Run

1. **Clone this repository:**

```bash
git clone https://github.com/your-username/Week-8-assignment-PLP.git
cd Week-8-assignment-PLP
```

2. **Open the SQL file in your MySQL client** (e.g., MySQL Workbench)

3. **Run the entire script** or copy-paste section-by-section to see how each part works.

4. You can test the data using SQL queries like:

```sql
-- List all books and their authors
SELECT b.title, CONCAT(a.first_name, ' ', a.last_name) AS author
FROM books b
JOIN book_author ba ON b.book_id = ba.book_id
JOIN authors a ON ba.author_id = a.author_id;
```

---

## 📌 Notes

- This is **Question 1 of 2** in the Week 8 Assignment.
- The second question will be added to this repository once completed.
- Sample data uses fictional entries for demonstration purposes.

---

## 🤝 Contributing

Feel free to fork the repo or suggest improvements. For questions or collaboration, reach out through the PLP community.

---

## 🧠 Author

**Emmanuel M Jesse**
PLP February Cohort 7 – Software Engineering Student

---

## 📅 Submission Info

**Assignment:** Week 8 – Full Database Management System  
**Track:** Software Engineering  
**Platform:** Power Learn Project (PLP)  
**Date:** April 2025

---

## 🔗 License

This project is licensed for academic use under the MIT License.
