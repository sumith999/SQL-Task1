Library Management System - SQL Task

This repository contains a simple **Library Management System** created using **MySQL**.

---

## What's Included

- **Task1.sql** – SQL script that:
  - Creates a `Library` database
  - Adds tables:
    - `Books`
    - `Members`
    - `IssuedBooks`
- **ER_Diagram.png** – A visual ER diagram (Entity Relationship) representing how the tables are related

---

## Tables Overview

### Books Table
'''sql
BookID INT PRIMARY KEY AUTO_INCREMENT,
Title VARCHAR(255) NOT NULL,
Author VARCHAR(100),
Publisher VARCHAR(100),
YearPublished INT
'''

### Members Table
'''sql
MemberID INT PRIMARY KEY AUTO_INCREMENT,
Name VARCHAR(100),
Email VARCHAR(100) UNIQUE,
JoinDate DATE
'''

### IssuedBooks Table
'''sql
IssueID INT PRIMARY KEY AUTO_INCREMENT,
BookID INT,
MemberID INT,
IssueDate DATE,
ReturnDate DATE,
FOREIGN KEY (BookID) REFERENCES Books(BookID),
FOREIGN KEY (MemberID) REFERENCES Members(MemberID)
'''

---

## How to Run the SQL File

1. Open **MySQL Workbench**
2. Connect to your MySQL server (default: `MySQL80`)
3. Open a new SQL tab and paste the contents of `Task1.sql`
4. Run the script to create the database and tables
5. Check the left panel under **Schemas** to verify everything is created

---

## Notes

- Make sure the MySQL service is running before executing the script
- You can create the ER diagram using:  
  `Database > Reverse Engineer` in MySQL Workbench

---

## About Me

Hi, I'm **Sumith Poojary**. This is one of my early SQL projects and a step forward in understanding how databases are structured and used.  
Feel free to explore and suggest improvements!

🔗 GitHub: [sumith999](https://github.com/sumith999)

---

## License

This project is shared for educational and learning purposes only.> README.md
