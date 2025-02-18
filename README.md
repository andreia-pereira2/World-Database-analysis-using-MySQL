# 🌍 World Database SQL Analysis

## 📌 Project Overview
In this project, I explored the **World** database, a commonly used dataset for practicing SQL queries. This dataset provides information on countries, cities, and populations, making it a great resource for data analysts to sharpen their **MySQL** skills.

### 🧐 Why Use the World Database?
The **World** database is essential for data analysts and SQL learners because it:
- Offers real-world data on **countries, cities, and population statistics**.
- Allows practice with key SQL concepts such as **JOINs, filtering, ordering, and aggregation**.
- Helps in building **data-driven insights** into global demographic trends.

## 📊 SQL Queries & Insights
Below are some of the SQL queries I worked on, along with their insights:

### 🔎 1. Retrieve the Capital City of Spain
```sql
SELECT city.name
FROM city
JOIN country ON city.id = country.capital
WHERE country.name = 'Spain';
```
**Insight:** This query finds the capital city of Spain by joining the **city** and **country** tables using the `capital` field.

📌 **Result:** *<img width="66" alt="Screenshot 2025-02-18 at 15 46 26" src="https://github.com/user-attachments/assets/91cac454-abfc-4968-8757-226f3793a346" />*

---

### 🌍 2. List All Capital Cities in Europe (Ordered Alphabetically)
```sql
SELECT city.name
FROM city
JOIN country ON city.id = country.capital
WHERE continent = 'Europe'
ORDER BY name;
```
**Insight:** This query provides a sorted list of European capital cities, making it easier to analyze geographical distributions.

📌 **Result:** *<img width="123" alt="Screenshot 2025-02-18 at 15 47 17" src="https://github.com/user-attachments/assets/4b15265a-8571-4b9c-915d-8174c5889653" />*

---

### 📈 3. Find the Average Population Per Country
```sql
SELECT name, AVG(population) AS 'Average'
FROM country
GROUP BY name
ORDER BY AVG(population) DESC;
```
**Insight:** This query calculates the average population per country and sorts them in descending order, highlighting the most populous countries.

📌 **Result:** *<img width="211" alt="Screenshot 2025-02-18 at 15 48 03" src="https://github.com/user-attachments/assets/5de7aef4-fe81-491b-ba56-b8f0b613ae06" />*

---

## 🚀 How to Use This Project
If you'd like to explore this dataset and SQL queries yourself, follow these steps:
1. **Download** the **World** database from [MySQL Sample Databases](https://dev.mysql.com/doc/index-other.html).
2. **Import** it into your MySQL environment.
3. Run the provided SQL queries to analyze the data.
4. Modify and expand queries to uncover more insights!

## 🏆 Key Takeaways
- Learned how to **join tables** to extract meaningful relationships.
- Practiced **filtering, sorting, and aggregating data**.
- Developed insights into **population trends and geographic distributions**.

📢 Feel free to fork this repository and try out the queries yourself. Let's keep learning and growing in data analysis! 🚀
