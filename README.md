# London Housing Analysis

A comprehensive, research‑grade analysis of London's housing market using 13,549 monthly records (1995–2020) and 1,071 yearly socioeconomic records (1999–2019). This project integrates time‑series modelling, clustering, econometrics, and exploratory data analysis to uncover long‑term price dynamics, affordability trends, and the socioeconomic forces shaping London's housing landscape.

## Methodology

- **Exploratory data analysis** — London-wide and borough-level price trends, seasonality, crime, salary, population, and wellbeing indicators
- **Affordability analysis** — price-to-income ratio by borough over time
- **K-Means clustering (with PCA)** — groups boroughs into meaningful market segments
- **Correlation analysis** — relationships between price, salary, crime, and wellbeing metrics
- **Time series decomposition & stationarity testing** — trend/seasonal/residual breakdown, ACF/PACF for SARIMA order selection
- **SARIMA forecasting** — models the London-wide price series and forecasts 24 months beyond the test period

## Key Findings

- London house prices rose **~500%** in nominal terms from 1995 to 2020, with a clear seasonal pattern (peaks in spring, dips in Jan–Feb)
- A **10x+ price gap** exists between the most expensive boroughs (Kensington & Chelsea, Westminster) and the least expensive outer boroughs — a gap that has widened over time
- The price-to-income ratio crossed the **8x affordability-crisis threshold** for many inner boroughs after 2010, deteriorating most sharply in inner east London
- Crime and price show a **positive correlation** across boroughs, reflecting a central-density paradox — expensive inner-city areas also record more absolute crimes
- K-Means clustering (k=4) identifies four borough groups: prime central, gentrifying inner, established outer, and affordable periphery
- SARIMA(1,1,1)(1,1,1,12) fits the price series well (**MAPE < 3%**) and projects continued moderate growth

Full analysis, charts, and the forecast are in the notebook.

## Tech Stack

Python, pandas, NumPy, statsmodels (SARIMA, seasonal decomposition), scikit-learn (K-Means, PCA), seaborn, matplotlib, SciPy

## Data Sources

London Housing Datasets — ONS / Land Registry (monthly and yearly borough-level variables)

## How to Run

```
pip install pandas numpy matplotlib seaborn scipy scikit-learn statsmodels
```
Open `london_housing_analysis.ipynb` in Jupyter and run all cells top to bottom (both CSV files are included in this repo).

## Author

Tateyama Orpa
