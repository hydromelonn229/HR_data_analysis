# 📊 Workforce Analytics Dashboard
### Understanding Employee Performance, Compensation, and Attrition Drivers

---

## 📌 Project Overview

This project is an end-to-end workforce analytics dashboard built in **Power BI**, analyzing over **2 million employee records** across 7 countries and 5 departments. The goal is to uncover patterns in employee attrition, compensation equity, and performance distribution — translating raw HR data into actionable business insights.

> *"Attrition is not a company-wide crisis — it is a Junior talent problem driven by compensation."*

---

## 🗂️ Dataset

| Property | Detail |
|---|---|
| Source | [Kaggle — HR Dataset Clean and Raw (2M Rows)](https://www.kaggle.com/datasets/rashadalaa/hr-dataset-clean-and-raw-2m-rows/data) |
| Rows | ~2,000,000 |
| Columns | 18 |
| Countries | 7 (UK, Germany, France, Spain, Italy, Netherlands, Poland) |
| Departments | 5 (Sales, IT, Operations, Finance, HR) |

**Key columns:** `Employee_ID`, `Department`, `Job_Level`, `Job_Title`, `Hire_Date`, `Status`, `Work_Mode`, `Salary`, `Country`, `Age`, `Experience_Years`, `Tenure_Years`, `Performance_Rating`, `Attrition`

---

## 🛠️ Tools Used

- **Python** — Data cleaning and preprocessing
- **Power BI Desktop** — Dashboard development, DAX measures, data modelling
- **Power Query** — Feature engineering (Tenure Band, Salary Band, Age Group)
- **GitHub** — Version control and portfolio hosting

---

## 📐 DAX Measures

Key measures created for the dashboard:

```dax
Total Employees = COUNTROWS(hr_data_clean)

Attrition Rate = DIVIDE([Attrition Count], [Total Employees], 0)

Voluntary Attrition Rate = DIVIDE([Resigned Count], [Total Employees])

Involuntary Attrition Rate = DIVIDE([Terminated Count], [Total Employees])

Median Salary = MEDIAN(hr_data_clean[Salary])
```

---

## 📊 Dashboard Pages

### 1. Workforce Overview
High-level snapshot of the workforce composition including department distribution, country breakdown, job level spread, and salary band distribution.

### 2. Salary Insights
Compensation analysis covering salary vs experience by job level, median salary benchmarks by department and job level, and experience distribution by salary band.

### 3. Performance Insights
Performance rating distribution across the workforce, segmented by work mode, tenure band, and department using heatmap matrix and 100% stacked bar charts.

### 4. Attrition Analysis *(Main Focus)*
Deep-dive into voluntary attrition drivers including analysis by job level, salary band, department, and experience years. Features an interactive heatmap matrix of attrition rate by department and job level.

### 5. Key Insights
Narrative conclusions page summarising the main findings and strategic recommendations derived from the data.

---

## 🔥 Key Findings

**Workforce Composition**
- Junior and Mid-level employees make up ~76% of the workforce — retention failures at these levels have outsized organisational impact
- Sales is the largest department at 30% of total headcount

**Salary is the Strongest Attrition Driver**
- Employees earning below $50K leave at nearly 3x the rate of those earning above $120K (17% vs 3%)
- Junior employees have the lowest median salary at $50K — directly linking the compensation gap to attrition patterns
- HR has the lowest median department salary ($65K) and simultaneously the highest attrition rate

**Performance is Consistent but Flat**
- The majority of employees rate as "Good" across all departments and work modes
- Performance distribution is nearly identical across Remote, Hybrid, and On-site workers — work mode does not appear to influence performance

**Attrition is Voluntary and Predictable**
- 77% of attrition is voluntary (resigned) vs 22% involuntary (terminated)
- Attrition risk peaks in the first 2 years at ~14% then drops sharply after year 5
- HR Junior (16%) and Operations Junior (15%) are the highest-risk segments

**The Single Biggest Opportunity**
- Addressing compensation for Junior employees earning below $80K would simultaneously target the highest-risk job level, salary band, and tenure window — one intervention, maximum impact

---

## 📁 Files

| File | Description |
|---|---|
| `HR_Attrition_Analysis.pbix` | Power BI dashboard file |
| `HR_Attrition_Analysis.pdf` | Static PDF export of all dashboard pages |
| `hr_data_clean.csv` | Cleaned dataset used for analysis |

---

## 🚀 How to View

**Option A — Interactive (recommended)**
1. Download `HR_Attrition_Analysis.pbix`
2. Open with [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
3. Explore all pages and interact with slicers and drill-downs

**Option B — Static**
1. Open `HR_Attrition_Analysis.pdf` directly in any PDF viewer

---

## 👤 Author

**Khant Min Lwin**  
Aspiring Data Analyst  
[GitHub](https://github.com) • [LinkedIn](https://linkedin.com)

---

*Built as a portfolio project to demonstrate end-to-end data analytics skills — from raw data to published interactive dashboard.*
