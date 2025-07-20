
# Canada Birth Probability Analysis (2000–2020)

## Project Overview

This project was completed as part of a technical exercise for a **Data and System Analyst** position. The objective was to analyze publicly available data to determine the **probability that a person born in a given year was born in Canada**, and to **explore trends in Canada's birth rate** over time.

---

##  Goal

- Retrieve global **birth rate** and **population** data per country per year
- Estimate **number of births per country per year**
- Store the cleaned data in a **SQLite database**
- Calculate the **probability of being born in Canada**, both for a selected year (2010) and across all years from 2000–2020
- Forecast Canada's birth rate up to 2030 using **regression models**
- Present findings with **clear visualizations and interpretations**

---

##  Data Sources

-  [Birth rate (World Bank)](https://api.worldbank.org/v2/country/all/indicator/SP.DYN.CBRT.IN?format=json)
-  [Population (World Bank)](https://api.worldbank.org/v2/country/all/indicator/SP.POP.TOTL?format=json)

---

## Tools & Technologies

- Python (Pandas, Requests, SQLite, Matplotlib, Seaborn, Scikit-learn)
- SQLite for structured querying
- Jupyter Notebook for development and presentation

---

##  Key Results

### Probability of Being Born in Canada
- In **2010**, the probability of being born in Canada was **0.0258%**
- Over the 2000–2020 period, the probability remained stable between **0.0235% and 0.0263%**
- **Peak year:** 2008, with the highest global birth share for Canada

### Birth Rate Forecast
- A **linear regression model** predicted the birth rate in 2030 will be **approximately 10.0 births per 1,000 people**
- Historical trend shows a steady decline since 2008
- Model:  
  \[
  \text{Birth Rate} = 84.859 - 0.0369 \times \text{Year}
  \]

---

##  Visualizations

Charts are saved in the `output/` folder and include:

- `canada_birth_probability_trend.png`: Probability of being born in Canada (2000–2020)
- `canada_vs_world_births_split.png`: Estimated births in Canada vs. globally
- `canada_birth_rate_trend.png`: Birth rate trend in Canada
- `canada_population_trend.png`: Population growth in Canada
- `canada_birth_rate_forecast.png`: Forecast of Canada’s birth rate to 2030

---

##  Insights & Interpretation

- Canada's global share of births has been consistent despite population growth
- Birth rate decline mirrors patterns in other high-income countries due to urbanization, delayed parenthood, and socio-economic factors
- If trends continue, Canada may face **demographic challenges** including a shrinking labor force and increased aging dependency

---

## Project Structure

```
canada_birth_probability/
├── data/                   # Raw JSON data from API
├── db/                     # SQLite database file
├── output/                 # All charts and visualizations
├── notebooks/              # Main notebook (.ipynb)
├── requirements.txt        # Python dependencies
└── README.md               # This file
```

---

##  How to Run

1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter notebook:
   ```bash
   jupyter notebook notebooks/01_canada_birth_probability_analysis.ipynb
   ```

---

## Future Recommendations

- Use time series models like **ARIMA** or **Prophet** for more advanced forecasting
- Explore **province-level data** using Statistics Canada APIs
- Build an **interactive dashboard** using Streamlit or Dash for dynamic analysis

---


