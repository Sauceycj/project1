# project1
#  Aviation Safety Data Analysis Project

##  Overview
This project explores aviation accident data from 1962 to 2023 using data cleaning, analysis, and visualizations to help a business make informed decisions about entering the aviation industry.

The dataset is sourced from the National Transportation Safety Board (NTSB) and includes civil aviation accidents and selected incidents.

---

##  Business Understanding

###  Objective
The company is considering expanding into the aviation industry. To mitigate risk, they want to identify which aircraft are safest to purchase for commercial and private operations.

###  Stakeholder
The **Head of the Aviation Division** — a non-technical decision-maker who will use our analysis to choose aircraft based on safety records.

###  Key Business Questions
1. Which aircraft **categories** are the safest?
2. Which **manufacturers (Make)** have the lowest total injuries?
3. Does the **purpose of flight** affect the number of injuries?
4. How do **number of engines** relate to total injuries?
5. How have accidents trended **year over year**?

---

##  Data Understanding & Analysis

###  Source
National Transportation Safety Board  
- Format: CSV  
- Size: ~89,000 rows, 31 columns  
- Encoding: Latin-1

###  Key Columns Used
- `Aircraft.Category`
- `Make`
- `Purpose.of.flight`
- `Number.of.Engines`
- `Total.Fatal.Injuries`, `Total.Serious.Injuries`, `Total.Minor.Injuries`, `Total.Uninjured`
- `Event.Date`

###  Cleaning Steps
1. Dropped rows with nulls in key columns.
2. Combined injury columns to form `Total.Injuries`.
3. Removed extreme outliers using IQR.
4. Converted dates to datetime and extracted year.
5. Used `.groupby()` and `.sum()` for aggregations.

---

## Visualizations

### 1. Injuries by Aircraft Category
![Injuries by Aircraft Category](images/injuries_by_category.png)

### 2. Injuries by Make (Top 10)
![Injuries by Make](images/injuries_by_make.png)

### 3. Purpose of Flight vs Injuries
![Injuries by Purpose](images/injuries_by_purpose.png)

### 4. Number of Engines vs Injuries
![Injuries by Engines](images/injuries_by_engines.png)

### 5. Accidents Per Year
![Accidents Over Time](images/accidents_per_year.png)

---

##  Recommendations

1. **Avoid Multi-Engine Aircraft** with high total injuries.
2. Favor **aircraft categories** with lower injury totals (e.g. gliders or lighter fixed-wing).
3. Choose **manufacturers** with lower incident/injury rates.
4. Avoid using aircraft for **non-commercial purposes** like ferry or personal use, which had more injuries.
5. Monitor **year-over-year accident trends** to understand risk environments.

---

##  Conclusion

By analyzing accident and injury trends from 60+ years of aviation data, we can identify aircraft and usage patterns that present the lowest risk. This will guide strategic decisions in acquiring aircraft for the company’s new aviation venture.

---

##  Files in this Repository

- `aviation_analysis.ipynb` — Cleaned and analyzed notebook
- `presentation.pdf` — Non-technical stakeholder presentation
- `AviationData.csv` — Raw dataset
- `/images/` — Visuals for README and presentation
- `.gitignore` — Standard Python ignore list

---

##  Author

**CJ Mungai**  
[LinkedIn Profile](https://www.linkedin.com/) (insert your link here)

---

## Questions?

For more details, feel free to reach out on [LinkedIn](https://www.linkedin.com/).

