
# 📊 COVID-19 Dashboard Project

## 📁 Project Overview
This project presents a comprehensive **COVID-19 Dashboard** using global and Indonesian data, focused on visualizing key metrics such as new cases and total deaths. The project is designed for insights on pandemic trends and vaccine rollout across regions, especially Indonesia.

---

## 🗂️ File Structure

| File Name                 | Description |
|--------------------------|-------------|
| `cleaned_covid_data.csv` | Cleaned dataset with global COVID-19 statistics |
| `COVID-19 Global Dashboard.twbx`          | Tableau Dashboard |
| `data_covid19.ipynb`     | Python notebook used for cleaning, analyzing, or preparing data |

---

## 🏗️ Database Design

The core table is:

```sql
CREATE TABLE covid_data (
    iso_code TEXT,
    continent TEXT,
    location TEXT,
    date DATE,
    total_cases DOUBLE PRECISION,
    new_cases DOUBLE PRECISION,
    total_deaths DOUBLE PRECISION,
    new_deaths DOUBLE PRECISION,
    total_vaccinations DOUBLE PRECISION,
    people_vaccinated DOUBLE PRECISION,
    people_fully_vaccinated DOUBLE PRECISION
);
```

---

## 📌 Key SQL Queries

### Top 10 Countries by Vaccinations:
```sql
SELECT location, MAX(people_vaccinated) AS vaccinated
FROM covid_data
GROUP BY location
ORDER BY vaccinated DESC
LIMIT 10;
```

### Daily New Cases in Indonesia:
```sql
SELECT date, new_cases
FROM covid_data
WHERE location = 'Indonesia'
ORDER BY date;
```

---

## 📊 Dashboard Features

- Top Country by Total Case
- Covid-19 Trend by Over Time
- Global Case Distribution
  
---
📊 Tableau Dashboard
🔗 [View Tableau Dashboard](https://public.tableau.com/app/profile/lita/viz/COVID-19GlobalDashboard_17504317088400/COVID-19GlobalDashboard)
![COVID-19 Global Dashboard](https://github.com/user-attachments/assets/7cceae12-f62b-40b8-a500-02e098cc7c5e)


## 🛠️ Tools Used

- Tableau Public – for building interactive dashboards
- PostgreSQL/MySQL – for SQL-based data querying
- Python (Jupyter Notebook) – for data cleaning and preprocessing
- Pandas, NumPy – for data manipulation
- Matplotlib/Seaborn – for inline plots (optional in `.ipynb`)

---

🧷 Credits

📂 Dataset: [Our World in Data (via Kaggle/CSV)](https://docs.owid.io/projects/covid/en/latest/dataset.html)

💻 Author: Lita

🗓 Date: June 2025

---

📎 Connect With Me

🌐 [LinkedIn](https://www.linkedin.com/in/lita-utami-wulandari/)

💼 [GitHub](https://github.com/litascripts)

📧 Email: litautamiwulandari@gmail.com
