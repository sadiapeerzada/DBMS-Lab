# DBMS-Lab
# 🗄️ DBMS Laboratory — B.Sc. (Hons.) Computer Application IV Semester

<div align="center">

![AMU](https://img.shields.io/badge/Aligarh_Muslim_University-006747?style=for-the-badge&logoColor=white)
![Course](https://img.shields.io/badge/Course_Code-CABSMJ4P04-8B0000?style=for-the-badge)
![Credits](https://img.shields.io/badge/Credits-02-0057A8?style=for-the-badge)
![Semester](https://img.shields.io/badge/Semester-IV-gold?style=for-the-badge)
![Session](https://img.shields.io/badge/Session-2025--2026-333333?style=for-the-badge)

> *"When a nation becomes devoid of art and learning, it invites poverty and when poverty comes it brings in its wake thousands of crimes."*
> — **Sir Syed Ahmad Khan**

</div>

---

## 📋 Table of Contents

- [About the Course](#-about-the-course)
- [Course Details](#-course-details)
- [Assessment Scheme](#-assessment-scheme)
- [Weekly Lab Index](#-weekly-lab-index)
- [Tech Stack](#-tech-stack)
- [Lab File Format](#-lab-file-format)
- [Department Info](#-department-info)

---

## 📖 About the Course

This laboratory course is designed for **B.Sc. (Computer Application) IV Semester** students to develop hands-on expertise in **Database Management Systems (DBMS)**. The course covers the full spectrum from ER diagram design to advanced PL/SQL programming including stored procedures, cursors, and triggers.

Students work with industry-standard tools — **Oracle Express Edition** and **MySQL** — to simulate real-world database design and management scenarios.

---

## 📌 Course Details

| Field | Details |
|---|---|
| **Course Title** | Laboratory Course-IV |
| **Course Code** | CABSMJ4P04 |
| **Programme** | B.Sc. (Hons.) Computer Application |
| **Semester** | IV |
| **Credits** | 02 |
| **Periods Per Week** | 03 |
| **Department** | Computer Science, AMU Aligarh |
| **Edition** | Revised — January 2026 |

### 🎯 Course Objectives

- Design Entity-Relationship (ER) diagrams and Schema diagrams
- Create fully-fledged databases from ER diagrams
- Write DDL, DML, and DCL SQL queries
- Implement PL/SQL blocks, Cursors, Triggers, Procedures, and Functions

### ✅ Course Outcomes

After completing this course, students will be able to:

- Understand Relational and Object-Relational DBMS concepts
- Comprehend query languages and their practical usage
- Identify logical entities and their relationships
- Draw ER diagrams for any real-world system
- Create cursors, functions, procedures, triggers, and other database objects

---

## 📊 Assessment Scheme

```
Total Marks: 100
├── Continuous Assessment  →  60 Marks
│   ├── Sessional I        →  30 Marks
│   │   ├── Lab Report (signed)   →  20 Marks
│   │   ├── Lab Question (in-lab) →   5 Marks
│   │   └── Viva Voce             →   5 Marks
│   └── Sessional II       →  30 Marks
│       ├── Lab Report (signed)   →  20 Marks
│       ├── Lab Question (in-lab) →   5 Marks
│       └── Viva Voce             →   5 Marks
└── Final Lab Examination   →  40 Marks
```

> ⚠️ **Minimum Requirement:** At least **10** timely completed and duly signed weekly assignments are compulsory to appear in the Final Lab Examination.

---

## 📅 Weekly Lab Index

### Week 1 — DBMS Basics & Tool Installation

**Objectives:** Learn basics of DBMS types; install and access Oracle XE and MySQL.

| # | Problem |
|---|---|
| 1 | Write a step-by-step report for MySQL installation (modelled after the Oracle XE installation guide) |

**Tools:** Oracle Database 21c Express Edition, MySQL Community Server

---

### Week 2 — ER Diagram & Schema Design (Basic)

**Objectives:** Design ER diagrams and schema diagrams for a given scenario.

| # | Problem |
|---|---|
| 1 | Design ER diagram and Schema for **AMU Computer Science Laboratory** (Students, Instructors, Computer Systems, Lab Sessions) |

**Entities:** Student · Lab Instructor · Computer System · Lab Session

---

### Week 3 — ER Diagram, Schema & Database Design

**Objectives:** Design ER diagrams and construct databases using automated tools.

| # | Problem |
|---|---|
| 1 | Design ER diagram, schema, and database for a **Car Dealership** system (sales, customers, service facility, mechanics, parts) |

**Entities:** Salesperson · Customer · Car · Invoice · ServiceTicket · Mechanic · Parts

---

### Week 4 — Table Creation & Data Insertion (DDL/DML)

**Objectives:** Create tables, insert records, understand table concepts.

| # | Problem |
|---|---|
| 1 | Create and populate `CLIENT_MASTER`, `PRODUCT_MASTER`, and `SALESMAN_MASTER` tables with full datasets |

**Tables Created:**

```sql
CLIENT_MASTER    → ClientNo, Name, City, PinCode, State, BalDue
PRODUCT_MASTER   → ProductNo, Description, ProfitPercent, UnitMeasure, QtyOnHand, ReorderLvl, SellPrice, CostPrice
SALESMAN_MASTER  → SalesmanNo, SalesmanName, Address1, Address2, City, PinCode, State, SalAmt
```

---

### Week 5 — Querying, Updating, Deleting & Altering Tables

**Objectives:** Write queries for retrieval, update, delete; alter and rename tables.

| # | Operations Covered |
|---|---|
| 1 | Backup · SELECT queries · UPDATE records · DELETE records · ALTER TABLE · DROP TABLE · RENAME TABLE |

**Key Operations:**

```sql
-- Sample queries practiced this week
SELECT name, city FROM CLIENT_MASTER;
UPDATE CLIENT_MASTER SET city = 'Bangalore' WHERE clientno = 'C00005';
DELETE FROM SALESMAN_MASTER WHERE salamt = 3500;
ALTER TABLE CLIENT_MASTER ADD telephone NUMBER(10);
DROP TABLE CLIENT_MASTER;
RENAME SALESMAN_MASTER TO sman_mast;
```

---

### Week 6 — Hospital Management Database (DDL/DML)

**Objectives:** Design and implement a real-world hospital database.

| # | Problem |
|---|---|
| 1 | Create `Hospital_DB` with Patient, Doctor, and Appointment tables; insert records; perform queries |
| 2 | Write advanced SQL queries — UPDATE, DELETE, ALTER, RENAME on Hospital_DB |

**Schema:**

```
Patient      (Patient_ID PK, Patient_Name, Age, Gender, Contact_No)
Doctor       (Doctor_ID PK, Doctor_Name, Specialization, Room_No)
Appointment  (Appointment_ID PK, Patient_ID FK, Doctor_ID FK, Appointment_Date, Appointment_Time)
```

**Test Coverage:** 11 test cases including FK constraint violation checks

---

### Week 7 — Constraints, Joins & Complex Queries

**Objectives:** Create tables with constraints; write advanced queries using joins.

| # | Problem |
|---|---|
| 1 | **Insurance Database** — PERSON, CAR, ACCIDENT, OWNS, PARTICIPATED tables with PKs, FKs |
| 2 | **Banking Database** — BRANCH, ACCOUNT, DEPOSITOR, CUSTOMER, LOAN, BORROWER tables with ER diagram |

**Sample Queries:**

```sql
-- Find total people who owned cars involved in accidents (2008-2020)
-- Find customers with at least two accounts at Aligarh branch
-- Find customers with balance > 100000
```

---

### Week 8 — Library Database with Full Constraint Application

**Objectives:** Apply NOT NULL, UNIQUE, CHECK, PRIMARY KEY, FOREIGN KEY constraints.

| # | Problem |
|---|---|
| 1 | College Library Database — Student, Book, Issue tables with all constraint types |

**Constraints Demonstrated:**

```sql
Student  → PRIMARY KEY, NOT NULL, UNIQUE (Mobile_No)
Book     → PRIMARY KEY, NOT NULL, CHECK (Price > 0)
Issue    → PRIMARY KEY, FOREIGN KEY (Student_ID), FOREIGN KEY (Book_ID), NOT NULL
```

**Includes:** Constraint violation test cases (duplicate mobile, negative price, invalid FK)

---

### Week 9 — Sales Information System

**Objectives:** Design a sales database; write complex retrieval queries.

| # | Problem |
|---|---|
| 1 | Full Sales System — Product, Client, Order, Salesman tables with ER + Schema + SQL queries |

**Key Queries Practiced:**

```sql
-- LIKE patterns: Find clients with 'a' as second letter
SELECT * FROM CLIENT WHERE client_name LIKE '_a%';

-- Sorted product listing by selling price
SELECT * FROM PRODUCT WHERE sell_price <= 5000 ORDER BY sell_price;
```

---

### Week 10 — Mobile Phone Service Center Database

**Objectives:** Design service-center database; implement JOINs and FK relationships.

| # | Problem |
|---|---|
| 1 | Mobile Service Center — Customer, Mobile, Service_Request tables; 13 test cases |

**Test Coverage:** Table creation · INSERT · SELECT · JOIN · FK violation · multiple records per entity

---

### Week 11 — Inter-University Database

**Objectives:** Build a complex multi-entity database; create secondary indexes; write advanced queries.

| # | Problem |
|---|---|
| 1 | Inter-University DB — University, Department, Program, Course, Syllabus, Faculty tables |

**Complex Queries (10):**

```
i.   Universities in Mumbai
ii.  Programs run by AMU
iii. Departments of JNU
iv.  Programs of University of Jammu
v.   Universities offering "MCA"
vi.  MCA Courses at AMU
vii. Faculty specializing in "Information Security"
viii.Syllabus of "Computer Architecture" across universities
ix.  CS Faculty of Delhi University
x.   University with maximum programs
```

---

### Week 12 — PL/SQL Stored Procedures & Functions

**Objectives:** Write PL/SQL stored procedures and functions.

| # | Problem |
|---|---|
| 1 | Stored procedure to display **"Hello World"** |
| 2 | Procedure to calculate **sum of digits at even positions** of a number |
| 3 | Procedure to count **prime and composite numbers** |
| 4 | Function to **compare three numbers** and display in ascending/descending order |
| 5 | Function for **arithmetic operations** (Add, Subtract, Multiply, Divide) |

**PL/SQL Template:**

```sql
CREATE OR REPLACE PROCEDURE hello_world AS
BEGIN
    DBMS_OUTPUT.PUT_LINE('Hello World');
END;
/
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| ![Oracle](https://img.shields.io/badge/Oracle_21c_XE-F80000?style=flat-square&logo=oracle&logoColor=white) | Primary RDBMS |
| ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) | Open-source RDBMS |
| **SQL** | DDL · DML · DCL · TCL |
| **PL/SQL** | Procedures · Functions · Cursors · Triggers |

---

**Deliverables per exercise (teacher-signed):**
- ER Diagram and Schema Diagram *(for Weeks 3, 7–8, 9–10, 11)*
- SQL / PL/SQL query with screenshot output

---

## 📁 Lab File Format

```
Lab File Index Template
─────────────────────────────────────────────────────
Week No. │ Problems with Description │ Page No. │ Teacher Signature & Date
─────────────────────────────────────────────────────
   1     │ 1#, 2#, 3#                │          │
   2     │ 1#, 2#, 3#                │          │
  ...    │ ...                       │          │
─────────────────────────────────────────────────────
Header: Page Number
Footer: Roll Number & Name
```

---

## 🏛️ Department Info

| Field | Details |
|---|---|
| **Department** | Department of Computer Science |
| **University** | Aligarh Muslim University, Aligarh (U.P.) India |
| **Lab Manual Edition** | Revised — January 2026 |
| **Chairperson** | Prof. Arman Rasool Faridi |
| **Design & Compilation** | Dr. Faisal Anwer · Dr. Faraz Masood · Dr. Mohammad Luqman |

---

<div align="center">

**Department of Computer Science · Aligarh Muslim University**

*Lab Manual CABSMJ4P04 · Revised Edition January 2026*

</div>
