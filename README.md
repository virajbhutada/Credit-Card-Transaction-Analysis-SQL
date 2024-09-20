# Credit Card Transaction Analysis using SQL 💳📊

This repository provides a comprehensive **SQL-based analysis** of consumer credit card transactions. This project aims to offer **actionable insights** into consumer **spending behavior**, **repayment patterns**, and overall financial trends using real-world data. By leveraging SQL queries, we can explore key customer metrics such as **average credit limits**, **popular spending categories**, and **repayment behaviors**.  

Through this project, you'll gain hands-on experience with:
- **SQL database design** for structured financial data storage.
- **Advanced querying techniques** to extract valuable insights from large datasets.
- **Business-critical analysis**, helping financial institutions identify trends, optimize credit offerings, and enhance customer engagement.

This project is an ideal resource for **data analysts**, **database administrators**, and **financial analysts** looking to deepen their understanding of credit card transaction data.

---

## 📋 **Project Overview**

The **Credit Card Transaction Analysis** project is designed to offer **in-depth insights** into consumer credit card usage patterns through **SQL-based queries**. By analyzing various data points such as transactions, repayments, and customer profiles, the project uncovers critical patterns that can help financial institutions and analysts **make data-driven decisions**. These decisions include **personalized offers**, **credit risk management**, and **targeted marketing strategies** based on customer behavior and demographics.

This project caters to:
- **Data Analysts** looking to explore financial data to extract trends and insights.
- **Database Engineers** focusing on the efficient management of relational data systems.
- **Financial Institutions** interested in better understanding their customer base to create tailored products, reduce credit risk, and boost profitability.

It is especially useful for:
- **Identifying high-value customers** based on credit limits and spending.
- **Understanding repayment behaviors** to mitigate risks and detect potential defaulters.
- **Optimizing product offerings** by analyzing which categories customers spend the most on (e.g., travel, dining).

---

## 🚀 **Features & Objectives**

This project was built with specific **features** and **objectives** to address financial analysis needs:

- **Data Import & Storage**: The project incorporates a structured SQL database schema that is designed to handle large volumes of **customer**, **repayment**, and **transaction data**. The data is stored in normalized tables for easy access and scalability.
- **Pre-Built SQL Queries**: The repository contains a set of SQL queries that are crafted to answer various **business-critical questions**. These queries can be executed to extract insights about customer behavior, spending patterns, and repayment behaviors.
- **Customer Segmentation & Insights**: By analyzing customer demographics, credit limits, and transaction data, the project helps identify **high-value customers** and **customer segments**. These segments can be used for more targeted financial products and personalized credit offers.

---

## 📊 **Dataset Details**

The datasets used in this project simulate real-world financial data, providing a robust base for analysis. Each dataset offers insights into different aspects of **credit card transactions** and **repayment patterns**.

- **Customer Data** (`customer_data.csv`): This dataset includes vital customer information such as **age**, **gender**, **city**, **credit limit**, and account status. Analyzing this data helps us segment customers based on demographics and financial capability.
  
- **Repayment Data** (`repayment_data.csv`): This dataset tracks **monthly repayment behavior**. It includes details about the **repayment amount**, **amount due**, and **overdue balances**, providing a comprehensive view of customer repayment trends. It can also be used to predict **delinquency risks**.

- **Spending Data** (`spend_data.csv`): This file contains detailed records of customer transactions, including **transaction dates**, **merchant categories**, and **amounts spent**. These insights are critical for understanding which categories (e.g., travel, dining, retail) contribute the most to customer spending, and how customers manage their finances.

The structured nature of these datasets allows us to perform **multi-dimensional analysis** by linking customer data with their corresponding transactions and repayment histories.

---

## 🧑‍💻 **Database Schema**

The **database schema** for this project is designed with normalization and efficient querying in mind. It includes three core tables that track essential aspects of credit card usage:

1. **Customers Table**: Contains demographic details such as **name**, **age**, **city**, and **credit limits**. This data provides valuable insights into **customer profiles** and helps in segmentation.

2. **Repayments Table**: This table tracks **monthly repayments**, **overdue balances**, and **outstanding dues**. By analyzing the repayment patterns, we can uncover trends such as **delayed payments**, **regularity in repayment**, and potential **risk factors** for delinquency.

3. **Transactions Table**: The transactions table captures details about each **credit card transaction**. This includes the **amount spent**, the **merchant category**, and the **transaction date**. It offers insights into **spending behavior**, such as which categories customers spend the most on and their spending frequency.

### Schema Diagram:

![schema](https://github.com/user-attachments/assets/f423d03f-6fc1-44f8-bfa4-608bd351d0b3)

The schema is optimized to support efficient querying for large-scale financial analysis. By linking these tables, the project provides a **360-degree view** of customer behavior, including how they spend and how they manage their repayments.


---

## 🔧 **Installation & Setup**

### **Requirements**:
- A relational database management system (RDBMS) such as MySQL, PostgreSQL, or SQLite.
- SQL client or a database management tool (e.g., MySQL Workbench, pgAdmin).
  
### **Setup Instructions**:
1. **Clone the repository**:
   ```bash
   git clone https://github.com/virajbhutada/Credit-Card-Transaction-Analysis-SQL.git
   cd Credit-Card-Transaction-Analysis-SQL
   ```

2. **Create the database** by executing the schema provided in `schema/schema.sql` to create tables.

3. **Load the datasets**:
   - Import the `customer_data.csv`, `repayment_data.csv`, and `spend_data.csv` into their respective tables.

4. **Run SQL Queries**:
   - Execute the queries in `analysis/analysis.sql` to analyze the data and generate insights.

---

## 🔍 **SQL Analysis**

This project answers several critical questions through SQL queries. Some key analyses performed include:

1. **Average Credit Limit by Age Group**:
   ```sql
   SELECT age_group, AVG(credit_limit) AS avg_limit
   FROM customers
   GROUP BY age_group;
   ```

2. **Top Spending Categories**:
   ```sql
   SELECT category, SUM(amount) AS total_spent
   FROM transactions
   GROUP BY category
   ORDER BY total_spent DESC
   LIMIT 5;
   ```

3. **Repayment Status by Customer**:
   ```sql
   SELECT customer_id, SUM(repayment_amount) AS total_repaid, SUM(due_amount) AS total_due
   FROM repayments
   GROUP BY customer_id;
   ```

These queries provide insights into how customers spend, their repayment patterns, and their credit limits. For the full list of SQL queries used in this project, refer to the [`analysis.sql`](https://github.com/virajbhutada/Credit-Card-Transaction-Analysis-SQL/blob/main/scripts/analysis.sql) file.

---

## 📈 **Key Insights**

The **Credit Card Transaction Analysis** project provides answers to several key business questions through **SQL-based data analysis**:

- **Average Credit Limit by Customer Age Group**: Segmenting customers by age and analyzing their credit limits helps identify **high-value customers** and detect patterns in how credit limits are distributed across age groups.
  
- **Top Spending Categories**: Analyzing **transaction data** allows us to understand which categories (e.g., **travel, retail, dining**) contribute the most to overall spending. These insights can be used by banks to **create targeted offers** or develop **new financial products** for specific customer segments.

- **Repayment Behavior**: This analysis focuses on understanding the repayment behavior of customers. By tracking **repayments and overdue balances**, we can flag potential **high-risk customers** and help financial institutions **mitigate risks** and optimize their **loan recovery strategies**.

These insights are vital for **customer segmentation**, **risk management**, and **product optimization** in the credit card industry.

---

## 📝 **Conclusion**

The **Credit Card Transaction Analysis** project provides a comprehensive view of customer **spending patterns**, **repayment behaviors**, and **credit usage**. The data-driven insights derived from this analysis enable financial institutions to make **informed decisions** about customer segmentation, risk management, and product strategies.

Key takeaways include:
- Identifying **high-value customers** based on their **credit limits** and **spending patterns**.
- Detecting **top spending categories**, which allow financial institutions to tailor offers and develop **targeted marketing campaigns**.
- Understanding repayment behaviors to identify **delinquent customers** and **mitigate risks** associated with non-repayment.

This project provides a strong foundation for extending further analysis into **credit risk assessment**, **fraud detection**, and **financial forecasting**.


---

## 📜 **License**

This project is licensed under the MIT License. For more details, please see the [LICENSE](LICENSE) file.

---

## 🤝 **Connect with Me**

If you have any questions, suggestions, or want to discuss potential collaborations, feel free to reach out:



**[![LinkedIn](https://img.shields.io/badge/LinkedIn-Viraj%20Bhutada-blue?logo=linkedin)](https://www.linkedin.com/in/virajnbhutada24/) [![GitHub](https://img.shields.io/badge/GitHub-Viraj%20Bhutada-2b3137?logo=github)](https://github.com/virajbhutada) [![Email](https://img.shields.io/badge/Email-virajnbhutada24%40gmail.com-D14836?logo=gmail&logoColor=white)](mailto:virajnbhutada24@gmail.com)**


