echo "# 📚 Library Management System - SQL Task



This project is a basic \*\*Library Management System\*\* developed using \*\*MySQL\*\* as part of a database assignment/internship task. It includes the creation of essential tables like Books, Members, and IssuedBooks using SQL queries and visualizes them using an ER diagram.



---



\## 📁 Project Structure



\- \\`Task1.sql\\` - SQL script to:

&nbsp; - Create a database \\`Library\\`

&nbsp; - Create tables:

&nbsp;   - \\`Books\\`

&nbsp;   - \\`Members\\`

&nbsp;   - \\`IssuedBooks\\`

\- \\`ER\_Diagram.png\\` - ER diagram showing relationships between entities (if included)



---



\## 🛠 Tables Created



\### 📖 Books

\\`\\`\\`sql

BookID INT PRIMARY KEY AUTO\_INCREMENT,

Title VARCHAR(255) NOT NULL,

Author VARCHAR(100),

Publisher VARCHAR(100),

YearPublished INT

\\`\\`\\`



\### 👥 Members

\\`\\`\\`sql

MemberID INT PRIMARY KEY AUTO\_INCREMENT,

Name VARCHAR(100),

Email VARCHAR(100) UNIQUE,

JoinDate DATE

\\`\\`\\`



\### 🔁 IssuedBooks

\\`\\`\\`sql

IssueID INT PRIMARY KEY AUTO\_INCREMENT,

BookID INT,

MemberID INT,

IssueDate DATE,

ReturnDate DATE,

FOREIGN KEY (BookID) REFERENCES Books(BookID),

FOREIGN KEY (MemberID) REFERENCES Members(MemberID)

\\`\\`\\`



---



\## ✅ How to Run



1\. Open \*\*MySQL Workbench\*\*

2\. Connect to your local server

3\. Copy the contents of \\`Task1.sql\\` into a new SQL tab

4\. Execute the script

5\. Check the \\`Schemas\\` tab to see the created database and tables



---



\## 📌 Notes



\- Make sure MySQL server is running (\\`MySQL80\\`)

\- ER Diagram can be generated via MySQL Workbench > Database > Reverse Engineer



---



\## 💡 Author



\*\*Sumith Poojary\*\*  

GitHub: \[sumith999](https://github.com/sumith999)



---



\## 📄 License



This project is for educational purposes only." > README.md



