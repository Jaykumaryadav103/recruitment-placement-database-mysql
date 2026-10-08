# Recruitment & Placement Database Management System — MySQL

## 📌 Project Overview

The **Recruitment & Placement Database Management System** is a MySQL-based database project designed to manage recruitment-related information such as candidates, clients, job openings, applications, placements, and billing records.

The project demonstrates practical SQL and database skills including **Joins, Aggregations, Subqueries, CTEs, Window Functions, Views, Stored Procedures, Primary Keys, Foreign Keys, Indexes, and Data Quality Checks**.

This project is designed as a portfolio project for **Database Intern, SQL Intern, Data Analyst, and MIS/Reporting roles**.

---

## 🎯 Project Objectives

The main objectives of this project are:

- Store recruitment data in a structured relational database.
- Manage candidate and client information.
- Track job openings and candidate applications.
- Monitor successful placements.
- Maintain placement-related billing information.
- Generate useful recruitment and management reports.
- Identify duplicate, missing, and inconsistent data.
- Improve query performance using indexes and optimized SQL queries.

---

## 🗄️ Database Structure

The database contains the following main tables:

### 1. Candidates

Stores information about candidates.

**Important columns:**
- candidate_id — Primary Key
- candidate_name
- email
- phone
- city
- qualification
- experience_years
- skills
- registration_date

### 2. Clients

Stores information about companies/clients.

**Important columns:**
- client_id — Primary Key
- client_name
- industry
- city

### 3. Jobs

Stores available job openings.

**Important columns:**
- job_id — Primary Key
- client_id — Foreign Key
- job_title
- required_skill
- salary_min
- salary_max
- job_status

### 4. Applications

Stores candidate applications for jobs.

**Important columns:**
- application_id — Primary Key
- candidate_id — Foreign Key
- job_id — Foreign Key
- application_date
- application_status

### 5. Placements

Stores successful candidate placements.

**Important columns:**
- placement_id — Primary Key
- candidate_id — Foreign Key
- job_id — Foreign Key
- placement_date
- joining_date
- placement_status
- salary

### 6. Billing

Stores billing information related to placements.

**Important columns:**
- billing_id — Primary Key
- client_id — Foreign Key
- placement_id — Foreign Key
- invoice_date
- invoice_amount
- payment_status

---

## 🔗 Table Relationships

The database follows a relational structure.

```text
Clients
   │
   └── Jobs
        │
        └── Applications
              │
              └── Candidates

Candidates
   │
   └── Placements
          │
          └── Billing
```

Primary and foreign keys are used to maintain relationships between tables and reduce data inconsistency.

---

## 🛠️ Technologies Used

- **MySQL**
- **SQL**
- **MySQL Workbench**
- **GitHub**
- CSV Dataset

---

## 💡 SQL Concepts Demonstrated

### Basic SQL
- SELECT
- WHERE
- ORDER BY
- DISTINCT
- LIMIT
- CASE WHEN

### Aggregations
- COUNT()
- SUM()
- AVG()
- MIN()
- MAX()
- GROUP BY
- HAVING

### Joins
- INNER JOIN
- LEFT JOIN
- RIGHT JOIN

### Advanced SQL
- Subqueries
- Common Table Expressions (CTEs)
- Window Functions
- ROW_NUMBER()
- RANK()
- DENSE_RANK()

### Database Development
- Primary Keys
- Foreign Keys
- Constraints
- Normalisation
- Views
- Stored Procedures
- Indexes

### Data Quality
- Duplicate detection
- Missing-value checks
- Invalid records
- Inconsistent values
- Referential integrity checks

---

## 📊 Example Business Questions

The project answers practical questions such as:

1. How many candidates are registered?
2. Which candidates have applied for each job?
3. Which clients have the highest number of job openings?
4. What is the average salary offered for each job?
5. Which candidates have successfully been placed?
6. What is the placement rate?
7. Which clients have pending invoices?
8. What is the total billing amount for each client?
9. Which candidates have applied for multiple jobs?
10. What are the top-paying job positions?
11. Which skills are most frequently required?
12. Which clients have the highest number of successful placements?

---

## 📁 Project Folder Structure

```text
recruitment-placement-database-mysql/
│
├── README.md
│
├── database/
│   ├── 01_create_database.sql
│   ├── 02_create_tables.sql
│   ├── 03_insert_data.sql
│   ├── 04_basic_queries.sql
│   ├── 05_joins.sql
│   ├── 06_aggregations.sql
│   ├── 07_subqueries_cte.sql
│   ├── 08_window_functions.sql
│   ├── 09_views.sql
│   ├── 10_stored_procedures.sql
│   ├── 11_indexes.sql
│   └── 12_data_quality_checks.sql
│
├── dataset/
│   ├── candidates.csv
│   ├── clients.csv
│   ├── jobs.csv
│   ├── applications.csv
│   ├── placements.csv
│   └── billing.csv
│
└── screenshots/
    ├── database_tables.png
    ├── query_results.png
    └── mysql_workbench.png
```

---

## ⚙️ How to Run the Project

### Step 1 — Install MySQL

Install **MySQL Server** and **MySQL Workbench**.

### Step 2 — Create the Database

Open MySQL Workbench and run:

```sql
CREATE DATABASE recruitment_db;
```

Then select the database:

```sql
USE recruitment_db;
```

### Step 3 — Create Tables

Run:

```text
02_create_tables.sql
```

This creates the required relational tables.

### Step 4 — Insert Data

Run:

```text
03_insert_data.sql
```

This loads sample recruitment data.

### Step 5 — Run SQL Queries

Execute the SQL files in order to practice:

- Basic queries
- Joins
- Aggregations
- Subqueries
- CTEs
- Window functions
- Views
- Stored procedures
- Indexes
- Data-quality checks

---

## 🔍 Query Optimization

Indexes are used to improve query performance for frequently searched columns.

Example:

```sql
CREATE INDEX idx_candidate_email
ON candidates(email);
```

The project also demonstrates how better filtering, joins, and indexing can reduce unnecessary database processing.

---

## 🧹 Data Quality Checks

The project includes SQL checks for:

- Duplicate candidate records
- Missing email addresses
- Missing phone numbers
- Invalid salary values
- Jobs without valid clients
- Applications without valid candidates
- Applications without valid jobs
- Duplicate billing records

These checks help ensure that reports are based on reliable data.

---

## 📈 Expected Project Outcome

After completing the project, the database can be used to generate reports about:

- Candidate registrations
- Job openings
- Applications
- Candidate placements
- Client performance
- Salary information
- Recruitment trends
- Billing and payment status

---

## 🎓 Skills Demonstrated

This project demonstrates my ability to:

- Design a relational database.
- Create tables with appropriate keys.
- Write accurate SQL queries.
- Work with multiple related tables.
- Use advanced SQL techniques.
- Perform data-quality checks.
- Create reusable database objects.
- Understand basic query optimization.
- Extract clean data for reporting.

---

## 💼 Relevance to Database Intern Roles

This project is especially relevant to entry-level **Database / SQL Intern** positions because it covers common responsibilities such as:

- SQL query writing
- MySQL database management
- Joins and aggregations
- Subqueries and window functions
- Views and stored procedures
- Database relationships
- Data validation
- Query optimization
- Reporting data extraction

---

## 👨‍💻 Author

**Jay Kumar Yadav**

Aspiring Data Analyst / SQL & Database Enthusiast

GitHub: `https://github.com/Jaykumaryadav103`

---

## ⭐ Conclusion

The **Recruitment & Placement Database Management System** is a practical SQL portfolio project that demonstrates database design, SQL query writing, data validation, reporting, and basic performance optimization using MySQL.

It was developed to strengthen practical database skills and demonstrate readiness for entry-level SQL and Database Intern opportunities.
