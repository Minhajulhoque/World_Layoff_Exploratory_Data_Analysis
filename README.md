# World Layoffs Exploratory Data Analysis (EDA) — SQL Portfolio Project

## Overview
This project performs Exploratory Data Analysis (EDA) on a cleaned global layoffs dataset using MySQL. The objective is to identify **patterns, trends, and concentration of layoffs** across companies, industries, countries, funding stages, and time periods.

The analysis leverages aggregation functions, window functions, Common Table Expressions (CTEs), and time-based grouping to extract actionable insights from the data.

---

## Dataset
- **Table Used:** `layoffs_staging_2`
- **Status:** Cleaned and standardized
- **Time Range:** Multi-year global layoff events
- **Metrics Analyzed:**
  - Total employees laid off
  - Percentage of workforce laid off
  - Temporal distribution
  - Company, industry, country, and stage-level impact

---

## Tools & Technologies
- **Database:** MySQL
- **SQL Techniques Applied:**
  - Aggregations (`SUM`, `MAX`, `MIN`)
  - Date functions (`YEAR`, `SUBSTRING`)
  - Window functions (`DENSE_RANK`, `SUM OVER`)
  - Common Table Expressions (CTEs)
  - Grouped ranking and rolling totals

---

## Analysis Workflow & Key Queries

### 1. Initial Data Exploration
- Reviewed the full dataset to understand structure and available fields.
- Identified maximum values for:
  - `total_laid_off`
  - `percentage_laid_off`

**Insight:**  
Highlighted extreme layoff events and companies that reduced 100% of their workforce.

---

### 2. Full Workforce Layoffs (100%)
- Filtered records where `percentage_laid_off = 1`.
- Analyzed these events by:
  - Total layoffs
  - Funds raised prior to layoffs

**Insight:**  
Several well-funded companies experienced complete workforce reductions, indicating severe operational or market failures.

---

### 3. Company-Level Layoff Impact
- Aggregated total layoffs by company.
- Ranked companies by cumulative layoffs.

**Insight:**  
A small number of companies accounted for a disproportionately large share of total layoffs.

---

### 4. Temporal Coverage
- Identified the earliest and latest layoff dates in the dataset.

**Insight:**  
Confirmed multi-year coverage, enabling meaningful trend and cycle analysis.

---

### 5. Industry-Level Analysis
- Summed total layoffs by industry.
- Ranked industries by impact.

**Insight:**  
Technology-related sectors accounted for the highest number of layoffs, reflecting sector-wide contractions.

---

### 6. Country-Level Analysis
- Aggregated layoffs by country.

**Insight:**  
Layoffs were heavily concentrated in a limited number of countries, with the United States leading by a significant margin.

---

### 7. Yearly Layoff Trends
- Grouped layoffs by year.

**Insight:**  
Layoffs peaked during periods of macroeconomic tightening and market corrections.

---

### 8. Company Stage Analysis
- Aggregated layoffs by funding stage.

**Insight:**  
Late-stage and post-IPO companies contributed the largest absolute number of layoffs, indicating cost optimization at scale.

---

### 9. Monthly Trend Analysis
- Aggregated layoffs by month (`YYYY-MM`).
- Ordered chronologically to visualize trends.

**Insight:**  
Layoffs exhibited clustering during specific economic downturn periods.

---

### 10. Rolling Layoff Totals
- Used a CTE to calculate monthly totals.
- Applied a rolling cumulative sum using a window function.

**Insight:**  
Provided a clear view of how layoffs accumulated over time, highlighting acceleration phases.

---

### 11. Company-Year Impact Ranking
- Aggregated layoffs by company and year.
- Ranked companies within each year using `DENSE_RANK`.

**Insight:**  
Identified the top 5 companies responsible for layoffs in each year, offering year-over-year comparison of corporate impact.

---

## Key Findings Summary
- Layoffs are highly concentrated among a small set of companies and industries.
- Technology and digital sectors dominate total layoff figures.
- Economic stress periods show clear spikes in monthly and yearly layoffs.
- Even well-funded and late-stage companies are not immune to workforce reductions.

---

## Analytical Value
This EDA demonstrates:
- Advanced SQL aggregation and windowing capabilities
- Strong temporal and categorical analysis skills
- Ability to translate raw data into structured insights
- Portfolio-ready analytical thinking using real-world data

---

## Potential Next Steps
- Visualization of trends using BI tools
- Correlation analysis with funding levels
- Regional impact comparison
- Predictive modeling using external macroeconomic indicators

---

## Author
**Minhajul Hoque**  
SQL • Data Analytics • Exploratory Data Analysis Portfolio Project

---
