# 🎓 AI Learning Lab Data Analysis

> End-to-End Data Analysis Project using Python, Pandas, Matplotlib, SQLite, and SQL.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![SQLite](https://img.shields.io/badge/SQLite-Database-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-red)

---

# 📌 Project Overview

The **AI Learning Lab Data Analysis Project** is designed to analyze student learning behavior, performance, attendance, and engagement.

The project follows a complete Data Analytics workflow from raw data to insights and reporting.

### Objectives

- Explore educational data
- Clean and preprocess messy records
- Analyze student performance
- Generate visual reports
- Export analytical summaries
- Store data in SQLite
- Execute SQL queries for insights

---

# 🔄 Project Workflow

```text
Raw Dataset (CSV)
        │
        ▼
Data Loading
        │
        ▼
Data Exploration
        │
        ▼
Data Cleaning
        │
        ▼
Feature Engineering
        │
        ▼
Data Analysis
        │
        ▼
Data Visualization
        │
        ▼
JSON Report Generation
        │
        ▼
SQLite Database Storage
        │
        ▼
SQL Analysis
```

---

# 📂 Project Structure

```text
AI-Learning-Lab-Data-Analysis/
│
├── MiniProject/
│   │
│   ├── ai_learning_lab.csv
│   ├── cleaned_ai_learning_lab.csv
│   │
│   ├── task1_load_explore.ipynb
│   ├── task2_clean_data.ipynb
│   ├── task3_analyze_data.ipynb
│   ├── task4_visual_report.ipynb
│   ├── bonus_sql_analysis.ipynb
│   │
│   ├── topic_score_chart.png
│   ├── performance_level_chart.png
│   ├── attendance_chart.png
│   ├── study_hours_chart.png
│   │
│   ├── learning_summary.json
│   └── learning_lab.db
│
├── requirements.txt
└── README.md
```

---

# 🛠️ Technologies Used

| Technology | Purpose |
|------------|----------|
| Python | Programming Language |
| Pandas | Data Processing |
| NumPy | Numerical Operations |
| Matplotlib | Data Visualization |
| SQLite | Database Storage |
| SQL | Data Querying |
| JSON | Report Export |

---

# 📊 Task 1 – Data Exploration

### Operations Performed

✔ Load CSV Dataset

✔ Display Dataset Shape

✔ View First 5 Rows

✔ Display Column Names

✔ Check Data Types

✔ Identify Missing Values

✔ Identify Duplicate Records

✔ Attendance Analysis

✔ Topic Analysis

### Workflow

```text
CSV File
    │
    ▼
Load DataFrame
    │
    ▼
Explore Structure
    │
    ▼
Check Missing Values
    │
    ▼
Check Duplicates
```

---

# 🧹 Task 2 – Data Cleaning

### Cleaning Steps

#### Remove Duplicates

```python
df.drop_duplicates()
```

#### Remove Extra Spaces

- student_name
- topic
- tool_used

#### Standardize Text

- attendance
- lab_completed
- api_used

#### Handle Invalid Values

| Column | Validation Rule |
|----------|----------|
| assignment_score | 0–100 |
| quiz_score | 0–100 |
| study_hours | ≥ 0 |
| feedback_rating | 1–5 |

#### Missing Value Treatment

| Column | Method |
|----------|----------|
| assignment_score | Mean |
| quiz_score | Mean |
| study_hours | Median |
| feedback_rating | Median |

### Cleaning Workflow

```text
Raw Data
   │
   ▼
Remove Duplicates
   │
   ▼
Fix Text Formatting
   │
   ▼
Handle Invalid Values
   │
   ▼
Fill Missing Values
   │
   ▼
Clean Dataset
```

---

# 📈 Task 3 – Data Analysis

## Feature Engineering

### Total Score

```text
total_score =
assignment_score +
quiz_score
```

### Performance Classification

| Score Range | Level |
|-------------|--------|
| 160+ | Excellent |
| 120–159 | Good |
| 80–119 | Average |
| Below 80 | Needs Support |

---

## Analysis Performed

- Average Assignment Score
- Average Quiz Score
- Average Study Hours
- Topic-wise Analysis
- Batch-wise Analysis
- Performance Distribution
- Needs Support Students

### Analysis Workflow

```text
Clean Data
    │
    ▼
Create total_score
    │
    ▼
Assign Performance Level
    │
    ▼
Group & Analyze Data
    │
    ▼
Generate Insights
```

---

# 📊 Task 4 – Data Visualization

### Generated Charts

| Chart | File |
|---------|---------|
| Average Total Score by Topic | topic_score_chart.png |
| Performance Level Count | performance_level_chart.png |
| Attendance Distribution | attendance_chart.png |
| Average Study Hours by Topic | study_hours_chart.png |

### Visualization Workflow

```text
Analyzed Data
      │
      ▼
Group Data
      │
      ▼
Generate Charts
      │
      ▼
Save PNG Files
```

---

# 📄 JSON Summary Report

Generated File:

```text
learning_summary.json
```

Contains:

```json
{
    "total_students": 100,
    "average_assignment_score": 78.5,
    "average_quiz_score": 75.2,
    "average_study_hours": 6.4,
    "most_common_topic": "Python"
}
```

---

# 🗄️ Bonus Task – SQLite & SQL

### Database

```text
learning_lab.db
```

### Table

```text
student_learning
```

### SQL Queries

#### Average Assignment Score by Topic

```sql
SELECT topic,
AVG(assignment_score)
FROM student_learning
GROUP BY topic;
```

#### Student Count by Batch

```sql
SELECT batch,
COUNT(*)
FROM student_learning
GROUP BY batch;
```

#### Students with Total Score Below 80

```sql
SELECT student_name,
total_score
FROM student_learning
WHERE total_score < 80;
```

### Database Workflow

```text
Clean Dataset
      │
      ▼
SQLite Database
      │
      ▼
student_learning Table
      │
      ▼
SQL Queries
      │
      ▼
Insights
```

---

# 🚀 How to Run

## Install Dependencies

```bash
pip install -r requirements.txt
```

## Run Project

Execute notebooks or scripts in order:

```text
Task 1 → Explore Data
Task 2 → Clean Data
Task 3 → Analyze Data
Task 4 → Visualize Data
Task 5 → SQL Analysis
```

---

# 📚 Skills Demonstrated

- Data Cleaning
- Data Analysis
- Exploratory Data Analysis (EDA)
- Data Visualization
- Feature Engineering
- JSON Export
- SQLite Database Management
- SQL Querying
- Python Programming

---

# 🎯 Learning Outcomes

Through this project, I learned how to:

- Work with real-world datasets
- Clean and preprocess data
- Generate meaningful insights
- Create professional visual reports
- Store data in databases
- Query databases using SQL
- Build an end-to-end analytics pipeline

---



⭐ If you found this project useful, consider giving it a star!
