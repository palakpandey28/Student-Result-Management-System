-------- Database Schema Design for Student Result Management System---------------

This schema outlines the four main tables (entities) and their attributes (columns). 
This design is required for the ER Diagram and Schema Design sections of your Project Report.

### 1. STUDENT Table (Personal & Enrollment Data)

| Column Name | Data Type | Key/Notes |
| :--- | :--- | :--- |
| **student_id** | INTEGER | **Primary Key (PK)** |
| first_name | TEXT | |
| last_name | TEXT | |
| enrollment_year | INTEGER | |
| department | TEXT | (e.g., "Computer Science") |
| contact_email | TEXT | |

### 2. COURSE Table (Subject Details)

| Column Name | Data Type | Key/Notes |
| :--- | :--- | :--- |
| **course_id** | TEXT | **Primary Key (PK)** (e.g., 'CS301') |
| course_name | TEXT | |
| credits | INTEGER | (e.g., 3 credits) |
| max_marks | INTEGER | Total possible score (e.g., 100) |
| faculty_id | INTEGER | **Foreign Key (FK)** to FACULTY |

### 3. FACULTY Table (User/Login Data)

| Column Name | Data Type | Key/Notes |
| :--- | :--- | :--- |
| **faculty_id** | INTEGER | **Primary Key (PK)** |
| email | TEXT | Used for login (Unique) |
| password_hash | TEXT | **SECURITY NFR:** Stores secure, hashed password. |
| role | TEXT | ('Admin' or 'Faculty') |

### 4. MARKS Table (The Core Transaction Data)

| Column Name | Data Type | Key/Notes |
| :--- | :--- | :--- |
| **marks_id** | INTEGER | **Primary Key (PK)** |
| **student_id** | INTEGER | **Foreign Key (FK)** to STUDENT |
| **course_id** | TEXT | **Foreign Key (FK)** to COURSE |
| score_achieved | INTEGER | Raw score |
| percentage | REAL | Calculated result |
| grade | TEXT | Calculated result (e.g., 'A', 'B+') |
| exam_session | TEXT | (e.g., 'Spring 2024') |