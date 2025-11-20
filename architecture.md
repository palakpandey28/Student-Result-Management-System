## 🏛️ System Architecture Design (Three-Tier Blueprint)

This blueprint outlines the organization of your modular Java packages for the required System Architecture Diagram.

| Tier/Layer | Purpose | Example Java Packages/Classes |
| :--- | :--- | :--- |
| **1. Presentation** | Handles user menus, input, and output. | `com.project.ui` (e.g., `AppMain.java`) |
| **2. Business Logic/Service** | Core processing: Calculates grades, validates marks, generates reports. | `com.project.service` (e.g., `ResultService.java`) |
| **3. Data Access (DAO)** | Runs all SQL commands using **JDBC** to talk to the database. | `com.project.dao` (e.g., `StudentDAO.java`, `MarksDAO.java`) |