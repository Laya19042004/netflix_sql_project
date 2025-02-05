
# Netflix Movies and TV shows Date Analysis using SQL

![Netflix Logo](https://github.com/Laya19042004/netflix_sql_project/blob/main/netflix%20logo.jpg)

Here's an overview you can use for your GitHub repository when uploading your **Netflix Movies and TV Shows Date Analysis using SQL** project.  

---

# 📌 Netflix Movies & TV Shows Date Analysis using SQL  

## 📋 Project Overview  
This project analyzes the release dates, trends, and patterns of Netflix movies and TV shows using SQL. The dataset contains details like titles, genres, release years, ratings, and more. The goal is to derive insights into content trends, popular release years, and the distribution of movies vs. TV shows over time.  

## 📂 Dataset  
- The dataset is sourced from [Netflix Movies and TV Shows dataset](https://www.kaggle.com/datasets/shivamb/netflix-shows).  
- It includes attributes like:  
  - **Title** (Movie/TV Show name)  
  - **Type** (Movie or TV Show)  
  - **Director** (Name of the director)  
  - **Cast** (Actors featured)  
  - **Country** (Where it was produced)  
  - **Date Added** (When it was added to Netflix)  
  - **Release Year** (Original release year)  
  - **Rating** (Content rating)  
  - **Duration** (Movie runtime or TV show seasons)  
  - **Genres** (Category of the show/movie)  

## 🔍 Key Analyses  
Using SQL, we performed the following analyses:  
1. **Count of Movies vs. TV Shows** – Understanding the content distribution.  
2. **Most Popular Release Years** – Identifying peak years for new content.  
3. **Monthly Trends of Netflix Additions** – Analyzing when Netflix adds most content.  
4. **Top Genres by Count** – Finding the most frequent genres.  
5. **Country-wise Content Production** – Identifying leading content-producing nations.  
6. **Directors with Most Movies/TV Shows** – Highlighting top creators.  
7. **Content Ratings Distribution** – Checking the spread of age-appropriate ratings.  

## 🛠️ SQL Queries Used  
Some key SQL queries used in the analysis:  
```sql
-- Count of Movies vs. TV Shows
SELECT type, COUNT(*) AS count 
FROM netflix_data 
GROUP BY type;

-- Most popular release years
SELECT release_year, COUNT(*) AS count 
FROM netflix_data 
GROUP BY release_year 
ORDER BY count DESC 
LIMIT 10;

-- Monthly trends of Netflix additions
SELECT strftime('%Y-%m', date_added) AS month, COUNT(*) AS count 
FROM netflix_data 
WHERE date_added IS NOT NULL
GROUP BY month
ORDER BY month;
```

## 🚀 Technologies Used  
- **Database:** SQLite / MySQL / PostgreSQL  
- **Querying Language:** SQL  
- **Visualization:** Python (Matplotlib, Seaborn) *(optional, if used)*  

## 📈 Insights & Findings  
- Netflix has added the most content in recent years, with a peak around **2018-2020**.  
- **Movies** outnumber **TV shows** significantly.  
- **Drama & Comedy** are the most common genres.  
- **United States, India, and the UK** lead in content production.  
- **TV-MA (Mature Audience)** is the most frequent rating on Netflix.  

## 💡 Future Enhancements  
- Integrating **Power BI/Tableau** for interactive dashboards.  
- Expanding the dataset with **IMDb ratings** for quality analysis.  
- Running **time-series forecasting** to predict future content trends.  

## 📜 How to Use  
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/netflix-sql-analysis.git
   cd netflix-sql-analysis
   ```
2. Import the dataset into your SQL database.  
3. Run the provided SQL queries for analysis.  

---

Would you like me to refine any sections or add more details? 🚀
