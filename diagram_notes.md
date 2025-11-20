## 🖼️ Design Diagram Blueprints (ERD & Workflow)

### 1. Entity-Relationship Diagram (ERD) Plan

The ERD will visually map the relationships between the four core entities defined in db_schema.md using the following connections. 

[Image of an Entity-Relationship Diagram]


* **FACULTY** to **COURSE**: **One-to-Many** relationship. (One Faculty member can teach Many Courses).
    * *Link:* COURSE table uses FACULTY_ID as a Foreign Key (FK).
* **STUDENT** to **MARKS**: **One-to-Many** relationship. (One Student can have Many Marks records).
    * *Link:* MARKS table uses STUDENT_ID as a Foreign Key (FK).
* **COURSE** to **MARKS**: **One-to-Many** relationship. (One Course can be associated with Many Marks records).
    * *Link:* MARKS table uses COURSE_ID as a Foreign Key (FK).

### 2. Workflow Diagram Plan

The Workflow Diagram will map the steps for the most complex feature: **Marks Input and Grade Generation**. 

[Image of a Workflow Diagram]


* **Start:** Faculty/Admin logs into the system (Authentication).
* **Step 1 (Input):** User selects a Course and inputs Student IDs and raw scores.
* **Step 2 (Validation):** System validates input (e.g., checks if score is between 0 and Max_Marks).
* **Step 3 (Calculation):** System automatically calculates the **Percentage** and assigns the final **Grade**.
* **Step 4 (Storage):** System performs a secure database transaction (JDBC) to save the final record in the **MARKS** table.
* **Step 5 (Confirmation):** System confirms successful record creation to the user.
* **End.**