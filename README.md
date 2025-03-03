### 📚 **Mastering SQL with Goodreads: Book Ratings & Reading Trends**  

## 🚀 **Project Overview**  
How do personal book ratings compare to **Goodreads’ global scores**? Are **certain genres consistently overrated or underrated**?  

This project **leverages SQL** to analyze **reading habits, book ratings, and genre trends** using a structured **SQLite database**. It showcases **advanced SQL skills**, including **data querying, aggregation, joins, and trend analysis**—key competencies for **data analytics roles at Meta, TikTok, and top tech companies**.  

---

## 🎯 **Key Objectives**  
✅ **Personal vs. Goodreads Ratings:** Analyzing rating discrepancies  
✅ **Genre Trends:** Identifying which book genres receive **higher/lower ratings**  
✅ **Reading Habits Over Time:** Exploring **yearly reading patterns**  
✅ **SQL Query Optimization:** Efficiently structuring and executing **complex queries**  

---

## 📊 **Dataset Overview**  
This **SQLite-based dataset** contains:  
- 📚 **Book Titles & Authors**  
- ⭐ **Personal Ratings vs. Goodreads Ratings**  
- 📖 **Genres & Reading Year Trends**  

---

## 🔍 **SQL-Driven Insights**  
This project is built **entirely in SQL**, showcasing **strong querying and database structuring skills**.  

### ✅ **Example Query: Top 5 Highest Rated Books (Personal vs. Goodreads)**  
```sql
SELECT title, author, my_rating, goodreads_rating 
FROM books_read 
ORDER BY my_rating DESC, goodreads_rating DESC 
LIMIT 5;
```
🔹 **Key Findings:**  
✔ **Some books have higher personal ratings than Goodreads consensus.**  
✔ **"One Hundred Years of Solitude" scored highest in personal ratings (5/5).**  

---

### ✅ **Query: Average Rating by Genre**
```sql
SELECT genre, 
       ROUND(AVG(my_rating), 2) AS avg_personal_rating, 
       ROUND(AVG(goodreads_rating), 2) AS avg_goodreads_rating
FROM books_read
GROUP BY genre
ORDER BY avg_goodreads_rating DESC;
```
🔹 **Key Findings:**  
✔ **Magical realism & historical fiction have the highest average ratings.**  
✔ **Genres like autobiography tend to be rated lower.**  

---

### ✅ **Query: Yearly Reading Trends**
```sql
SELECT year_read, COUNT(*) AS books_read
FROM books_read
GROUP BY year_read
ORDER BY year_read DESC;
```
🔹 **Key Findings:**  
✔ **Reading activity increased significantly from 2019 to 2022.**  
✔ **Historical fiction and literary fiction were most popular in recent years.**  

---

## 📈 **Data Visualization & Trends**  
📌 **Reading Volume Trends** – Books read per year  
📌 **Genre Popularity Analysis** – Most frequently read genres  
📌 **Personal vs. Goodreads Rating Discrepancies**  

✅ **Example: Ratings Comparison Plot (Personal vs. Goodreads)**  
```python
import matplotlib.pyplot as plt

df.plot(kind="bar", x="genre", y=["my_rating", "goodreads_rating"], title="Personal vs. Goodreads Ratings")
plt.show()
```
---

## 🔮 **Future Scope**  
🔹 **Book Recommendation System based on ratings & genre preferences**  
🔹 **Exploring sentiment analysis on Goodreads reviews**  
🔹 **Automated ETL pipeline for real-time book tracking**  

---

## 🛠 **How to Run This Project**  
1. Clone the repo:  
   ```bash
   git clone https://github.com/shrunalisalian/goodreads-sql-analysis.git
   ```
2. Open the **Jupyter Notebook** and execute the SQL queries.  

---

## 📌 **Connect with Me**  
- **LinkedIn:** [Shrunali Salian](https://www.linkedin.com/in/shrunali-salian/)  
- **Portfolio:** [Your Portfolio Link](#)  
- **Email:** [Your Email](#)  
