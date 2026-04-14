 Milestone 1 Report — Economic Factors and Happiness
Project Overview

The goal of this project is to understand how economic conditions affect happiness levels across different countries. I'm interested in exploring whether factors like income, unemployment, and inflation are related to how happy people are in a given country.
Data Collection

I used two main data sources:

World Happiness Report (2015–2024)
Source: Kaggle (originally from the World Happiness Report)
Contains happiness scores and related factors for ~140 countries per yearKey columns: Happiness Score, GDP per capita, Social Support, Healthy Life Expectancy, Freedom, Generosity, Perceptions of Corruption

World Bank Indicators (2015–2024)
Source: data.worldbank.org
I downloaded three economic indicators:
GDP per capita growth (annual %)
Inflation, GDP deflator (annual %)
Unemployment, total (% of labor force)

After merging both datasets on Country and Year, I ended up with 1502 rows before cleaning.

Data Cleaning

I checked for missing values across all columns. The World Bank indicators had some missing data:
GDP Growth: 217 missing
Inflation: 217 missing
Unemployment: 224 missing

I dropped rows where any of these three economic indicators were missing. After cleaning, the final dataset has 1272 rows and 14 columns

Exploratory Data Analysis (EDA)

Correlation Heatmap
I created a correlation matrix to see how all variables relate to each other. The strongest correlations with Happiness Score were:
- Social Support: 0.76 (strongest)
- GDP per capita: 0.66
- Healthy Life Expectancy: 0.69
- Unemployment: -0.18 (negative, as expected)
- Inflation: -0.15 (negative, weak)
GDP per Capita vs Happiness Score
The scatter plot shows a clear positive trend — countries with higher GDP per capita tend to have higher happiness scores. Western European countries cluster at the top right, while Sub-Saharan African countries are mostly at the bottom left.

Average Happiness by Region
North America & ANZ and Western Europe are the happiest regions on average. Sub-Saharan Africa and South Asia have the lowest average happiness scores.

Hypothesis Tests

I ran Pearson correlation tests to check whether the relationships between economic indicators and happiness are statistically significant.

| Variable | Correlation | p-value | Result |
|---|---|---|---|
| GDP per capita | 0.657 | 0.0000 | Significant |
| GDP Growth | 0.012 | 0.6727 | Not Significant |
| Inflation | -0.149 | 0.0000 | Significant |
| Unemployment | -0.180 | 0.0000 | Significant |

Key findings:
GDP per capita has a strong and statistically significant positive relationship with happiness.
Inflation and unemployment both have a small but significant negative relationship with happiness.
Interestingly, GDP growth rate is not significantly related to happiness — what matters is the overall income level, not how fast the economy is growing.

Summary

The data suggests that wealthier countries tend to be happier, and higher unemployment and inflation are associated with lower happiness. However, social support turned out to be the strongest predictor of happiness overall, which suggests that economic factors alone don't tell the whole story.

Next steps will include building predictive models and doing deeper analysis.
