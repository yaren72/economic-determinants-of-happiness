# economic-determinants-of-happiness
## Project Overview
This project investigates whether macroeconomic indicators (income level, unemployment, inflation, GDP growth) can explain differences in national happiness across countries. Data from the World Happiness Report (2015–2024) and World Bank Open Data were combined and analyzed using statistical tests and machine learning models.
## Research Questions

- Can macroeconomic indicators explain differences in national happiness?
- Which factors — economic or social — are most predictive of happiness?
- Does GDP growth rate matter, or is it the existing level of wealth that counts?

## Repository Structure
- `dsa_proje.ipynb` — Main analysis notebook
- `final_report_dsa.pdf` — Final report
- `happiness_economic_clean.csv` — Cleaned dataset
- `world_happiness_combined.csv` — Raw happiness data
- `requirements.txt` — Required packages
## Data Sources

**World Happiness Report (2015–2024):** Kaggle
**World Bank Indicators (2015–2024):** data.worldbank.org

- GDP per capita growth (annual %)
- Inflation, GDP deflator (annual %)
- Unemployment, total (% of labor force)



## How to Run

Clone the repository
Install dependencies:

   pip install -r requirements.txt

Open dsa_proje.ipynb in Jupyter and run all cells

## Key Findings

- Social support is the strongest predictor of national happiness (r=0.76)
- GDP growth rate has no significant relationship with happiness (p=0.67)
- Tree-based models (Gradient Boosting, Random Forest) outperform linear models
- Best model: Regularized Gradient Boosting with R²=0.841

## AI Tools Usage
- AI tools was used for guidance on data cleaning decisions, model selection, Lasso analysis, and report writing. All code was written and executed by the author.
