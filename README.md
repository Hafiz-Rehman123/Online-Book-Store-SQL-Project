# 📚 Online Book Store SQL Analytics & Database Project

An end-to-end relational database project built using **MySQL** to manage and analyze operational data for an online bookstore[cite: 1, 2]. The project includes database design, data loading scripts, and comprehensive analytical queries targeting key business metrics like revenue, inventory management, and customer ordering behavior[cite: 3, 4].

---

<p align="center">
  <img src="screenshot.png" alt="SQL Project on Online Book store" width="100%">
</p>

---

## 📊 Dataset Overview

The dataset contains three relational tables:
* **`Books`**: Catalog details including Book ID, Title, Author, Genre, Published Year, Price, and Stock level (500 records)[cite: 2].
* **`Customers`**: Demographic details including Customer ID, Name, Email, Phone, City, and Country (500 records)[cite: 2].
* **`Orders`**: Transaction logs containing Order ID, Customer ID, Book ID, Order Date, Quantity, and Total Amount (500 records)[cite: 2].

---

## 🛠️ Key Features & Queries Covered

### 1. Database Schema & Data Definition (DDL)
* Primary Key and Foreign Key relational constraints to maintain data integrity[cite: 2].
* Data type optimization for text, pricing (`DECIMAL`), and dates (`DATE`).

### 2. Basic Data Analysis[cite: 3]
* Filtering catalog by Genre, Published Year, and Country[cite: 3].
* Aggregate metrics: total inventory stock, total order revenue ($75,628.66), and minimum/maximum product prices[cite: 3].
* Date filtering for orders placed during specific promotional periods (e.g., November 2023)[cite: 3].

### 3. Advanced Business Intelligence Queries[cite: 4]
* **Revenue & Sales Analytics:** Multi-table `JOIN` operations to compute total unit sales by genre and author[cite: 4].
* **Customer Behavior Analytics:** Identification of top-spending customers and customer order frequency using `GROUP BY` and `HAVING` filters[cite: 4].
* **Inventory Tracking:** Real-time remaining stock calculations (`Stock - Total_Ordered`) using `LEFT JOIN` and `COALESCE` to handle unsold items[cite: 4].

---

## 🚀 How to Run the Project

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/online-bookstore-sql-analysis.git](https://github.com/YOUR_USERNAME/online-bookstore-sql-analysis.git)
   cd online-bookstore-sql-analysis
   ```

2. **Setup the MySQL Database:**
   Execute `sql/01_schema_setup.sql` in MySQL Workbench or via the command line to construct the database and tables[cite: 1, 2].

3. **Load the Data:**
   Use the `Table Data Import Wizard` in MySQL Workbench or execute `sql/02_data_import.sql` after specifying the correct local paths for the CSV files[cite: 2].

4. **Execute Analytical Queries:**
   Run scripts in `sql/03_basic_queries.sql` and `sql/04_advanced_queries.sql` to reproduce the analytical findings[cite: 3, 4].

---

## 💡 Tech Stack
* **Database Management System:** MySQL
* **Tools:** MySQL Workbench / Command Line Client
* **Languages:** SQL (DDL, DML, DQL)
