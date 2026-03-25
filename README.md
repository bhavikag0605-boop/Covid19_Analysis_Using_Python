# Covid19_Analysis_Using_Python

## 📌 Project Overview

An end-to-end exploratory data analysis (EDA) project on India's COVID-19 pandemic data, combining case-level analysis with vaccination rollout insights. Using Python for data wrangling and visualization, the project uncovers state-wise infection trends, mortality patterns, recovery rates, and vaccination disparities across India's states and union territories.

## 🎯 Business Problem

During the COVID-19 pandemic, tracking the spread, recovery, and vaccination rollout at a state level was critical for public health decision-making. This project answers key questions: Which states faced the highest active case burdens? Where were mortality rates elevated? How equitable was the vaccine distribution across India?

## 📂 Datasets Used

| Dataset | Description |
|---------|-------------|
| `covid_19_india.csv` | State-wise daily confirmed, cured, and death counts |
| `covid_vaccine_statewise.csv` | State-wise vaccination data including gender breakdown and dose counts |

## 🔍 Analysis Performed

### 🦠 COVID-19 Case Analysis
- **Data Cleaning** — Dropped irrelevant columns (Sno, Time, ConfirmedIndianNational, ConfirmedForeignNational), parsed dates
- **Active Cases Feature Engineering** — Derived `Active_Cases = Confirmed − (Cured + Deaths)`
- **State-wise Pivot Table** — Aggregated max Confirmed, Deaths, Cured per state; computed Recovery Rate and Mortality Rate
- **Top 10 Active Cases** — Bar chart of states with highest active case peaks
- **Top 10 Deaths** — Bar chart ranking states by total death toll
- **Growth Trend Analysis** — Line chart tracking active case trajectory for the top 5 most affected states (Maharashtra, Karnataka, Delhi, Tamil Nadu, Uttar Pradesh)

### 💉 Vaccination Analysis
- **Data Cleaning** — Renamed columns, dropped sparse dose-specific columns, filtered out national-level aggregate rows
- **Gender Vaccination Split** — Pie chart comparing total male vs. female individuals vaccinated nationally
- **Top 5 Most Vaccinated States** — Bar chart of states leading the vaccination drive
- **Least 5 Vaccinated States** — Bar chart exposing states with the lowest vaccination coverage

## 🛠️ Tools & Technologies

- **Python** — Core analysis language
- **Pandas** — Data manipulation, pivot tables, groupby aggregations
- **NumPy** — Numerical computations
- **Matplotlib & Seaborn** — Static visualizations (bar charts, line charts)
- **Plotly Express** — Interactive pie chart for gender vaccination breakdown
- **Jupyter Notebook** — Development and presentation environment

## 📊 Key Visualizations

1. Top 10 states with highest active COVID-19 cases
2. Top 10 states with highest COVID-19 deaths
3. Active case growth trends — Top 5 states (time-series)
4. Male vs. Female vaccination distribution (interactive pie chart)
5. Top 5 and Bottom 5 states by total vaccination coverage

## 📈 Key Insights

- **Maharashtra, Karnataka, and Delhi** consistently led in active cases and deaths throughout the pandemic
- **Recovery rates exceeded 95%** across most states, while mortality rates highlighted regional healthcare disparities
- **Male vaccination rates were higher** than female across India, pointing to gender-based access gaps
- **Vaccination coverage was highly unequal** — top-performing states administered multiples of the doses seen in the least-covered states

## 🚀 Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/covid19-india-analysis.git
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn plotly jupyter
   ```
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook Covid_19_Analysis.ipynb
   ```
