# Data Visualization Portfolio

A semester-long collection of data visualization projects covering time-series decomposition, geospatial mapping, hierarchical charts, exploratory data analysis, multi-source business analysis, and the ethics of visual communication. Each notebook in this repository solves a different real-world problem and uses a different family of visualization techniques.

<p align="center">

<!-- Programming and Tooling -->

![Programming](https://img.shields.io/badge/Programming-Python%203.10+-3776AB?style=flat-square&logo=python&logoColor=white)
![Environment](https://img.shields.io/badge/Environment-Jupyter%20%2F%20Colab-F37626?style=flat-square&logo=jupyter&logoColor=white)
![Data Processing](https://img.shields.io/badge/Data%20Processing-Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Numerical](https://img.shields.io/badge/Numerical-NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Statistics](https://img.shields.io/badge/Statistics-statsmodels-3B5998?style=flat-square)
![Static Plots](https://img.shields.io/badge/Static%20Plots-Matplotlib-11557C?style=flat-square)
![Statistical Plots](https://img.shields.io/badge/Statistical%20Plots-Seaborn-3776AB?style=flat-square)
![Interactive Plots](https://img.shields.io/badge/Interactive%20Plots-Plotly-3F4F75?style=flat-square&logo=plotly&logoColor=white)
![Geospatial](https://img.shields.io/badge/Geospatial-Folium%20%2F%20GeoPandas-77B829?style=flat-square)
![Version Control](https://img.shields.io/badge/Version%20Control-GitHub-181717?style=flat-square&logo=github&logoColor=white)

<br/>

<!-- Visualization Techniques -->

![Time Series](https://img.shields.io/badge/Time%20Series-STL%20Decomposition-1F4E79?style=flat-square)
![Forecasting](https://img.shields.io/badge/Forecasting-Trend%20%2F%20Seasonality-2E7D32?style=flat-square)
![Anomaly Detection](https://img.shields.io/badge/Anomaly%20Detection-Z--Score%20Method-C62828?style=flat-square)
![Choropleth](https://img.shields.io/badge/Mapping-Choropleth-455A64?style=flat-square)
![Flow Maps](https://img.shields.io/badge/Mapping-Sankey%20Flows-37474F?style=flat-square)
![Treemap](https://img.shields.io/badge/Hierarchical-Treemap-6A1B9A?style=flat-square)
![Sunburst](https://img.shields.io/badge/Hierarchical-Sunburst-7B1FA2?style=flat-square)
![Dashboards](https://img.shields.io/badge/Dashboards-Interactive%20Plotly-5D4037?style=flat-square)
![EDA](https://img.shields.io/badge/Analysis-Exploratory%20Data%20Analysis-AD1457?style=flat-square)
![Feature Eng](https://img.shields.io/badge/Modeling-Feature%20Engineering-1565C0?style=flat-square)

<br/>

<!-- Data Sources -->

![Census API](https://img.shields.io/badge/Data%20Source-US%20Census%20API-006241?style=flat-square)
![WHO Data](https://img.shields.io/badge/Data%20Source-WHO%20COVID--19%20Open%20Data-005EB8?style=flat-square)
![OEC](https://img.shields.io/badge/Data%20Source-OEC%20Trade%20API-CA6F1E?style=flat-square)
![OWID](https://img.shields.io/badge/Data%20Source-Our%20World%20in%20Data-D4691E?style=flat-square)
![Zillow](https://img.shields.io/badge/Data%20Source-Zillow%20ZHVI-1A237E?style=flat-square)
![Apify](https://img.shields.io/badge/Data%20Collection-Apify%20Scraper-FF9012?style=flat-square)

</p>

---

## Table of Contents

- [Overview](#overview)
- [Project Index](#project-index)
- [Project 1: Time-Series Decomposition and Forecasting](#project-1-time-series-decomposition-and-forecasting)
- [Project 2: Geospatial Visualization with Choropleth and Sankey Flows](#project-2-geospatial-visualization-with-choropleth-and-sankey-flows)
- [Project 3: Hierarchical Visualization with Treemaps and Sunbursts](#project-3-hierarchical-visualization-with-treemaps-and-sunbursts)
- [Project 4: Mid-Term — Multi-Source Business Analysis](#project-4-mid-term--multi-source-business-analysis)
- [Project 5: Exploratory Data Analysis and Feature Engineering](#project-5-exploratory-data-analysis-and-feature-engineering)
- [Project 6: Ethics, Dashboards, and Responsible Visualization](#project-6-ethics-dashboards-and-responsible-visualization)
- [Project 7: Stock Portfolio Investment Pitch](#project-7-stock-portfolio-investment-pitch)
- [Tech Stack](#tech-stack)
- [Repository Structure](#repository-structure)
- [How to Reproduce](#how-to-reproduce)
- [About](#about)

---

## Overview

This portfolio brings together every major assignment completed during a one-semester course in data visualization. Each project takes a different dataset, asks a different question, and demonstrates a different visualization technique. Read together, they cover most of the work a data analyst is expected to do day-to-day: explore data, find patterns, build the right chart for the right question, and communicate the result to a non-technical reader.

The projects are arranged in the order they were completed, which roughly mirrors the order a working analyst would learn the same techniques: temporal patterns first, then geography, then hierarchy, then full multi-source analysis, then ethics and presentation.

---

## Project Index

| # | Project | Technique Focus | Dataset |
| --- | --- | --- | --- |
| 1 | Time-Series Decomposition and Forecasting | STL decomposition, anomaly detection, interactive dashboards | Synthetic website traffic, 2 years |
| 2 | Geospatial Visualization | Choropleth, Sankey flow maps, interactive tooltips | US states, interstate migration |
| 3 | Hierarchical Visualization | Treemap, Sunburst, multi-level drill-down | US Exports (OEC API), World Energy (OWID) |
| 4 | Mid-Term Multi-Source Analysis | Time series, geospatial, scoring models | WHO COVID-19, Apify Levi's stores, US Census, Zillow ZHVI |
| 5 | Exploratory Data Analysis | Histograms, box plots, scatter plots, transformations, feature engineering | Student scores, employee salaries, time series, housing |
| 6 | Ethics and Dashboard Design | Critical analysis, KPI hierarchy, color and accessibility | Published academic papers, real dashboards |
| 7 | Stock Portfolio Pitch | Financial visualization, risk-return positioning, narrative-driven slides | ASML, Broadcom, AMD financials |

---

## Project 1: Time-Series Decomposition and Forecasting

**File:** [`Class_5_Assignment_Final.ipynb`](./Class_5_Assignment_Final.ipynb)

This notebook works through a complete time-series workflow on two years of simulated daily website traffic data. The data is generated with a known structure (linear growth trend, weekly seasonality, annual seasonality, and random noise) so that the decomposition results can be validated against ground truth.

The five exercises in the notebook build on each other:

1. **Identify temporal patterns.** Plot daily traffic, add a 30-day moving average to expose the trend, and apply a z-score test with a threshold of ±2 to flag anomalies that deviate from the overall pattern.
2. **Choose the right time scale.** Compare hourly, daily, and weekly views of the same data to show that the right aggregation depends entirely on the question being asked.
3. **STL decomposition.** Use `statsmodels.tsa.seasonal.STL` to separate the series into trend, seasonal, and residual components. Compute trend strength and seasonal strength using the standard variance-ratio formulas, then validate the residuals are random using an ACF plot.
4. **Forecasting visualization.** Project the trend forward and visualize forecast confidence bands.
5. **Interactive dashboard.** Build a multi-panel Plotly dashboard with linked controls for time range, comparison view, and seasonal drill-down.

The annual growth rate of the simulated traffic was calculated using a compound growth formula and verified against the construction parameters of the synthetic data.

---

## Project 2: Geospatial Visualization with Choropleth and Sankey Flows

**File:** [`In_Class6_Assignment.ipynb`](./In_Class6_Assignment.ipynb) and [`Class_6_in_Class_Assignment.pdf`](./Class_6_in_Class_Assignment.pdf)

This assignment covers two complementary mapping techniques: choropleth maps for showing magnitude across a region, and Sankey-style flow maps for showing movement between regions.

**Choropleth maps.** Three versions of US-state choropleth maps are built using Folium and GeoPandas. The first uses a randomly generated density variable as a teaching example. The second joins an external pandas DataFrame of state-level unemployment rates onto the GeoJSON boundary file and colors each state using the `YlGn` palette. The third version adds an interactive tooltip layer with hover and highlight behavior, demonstrating how to combine GeoJson layers with style and highlight functions.

**Sankey flow maps.** Interstate migration data (origin state, destination state, number of migrants) is visualized two ways. The first version draws curved geographic flow lines on a US map using `plotly.graph_objects.Scattergeo`, with line width proportional to migrant volume. The second version replaces the geographic projection with a pure Sankey diagram showing flows from regional origins (North America, Europe, Asia) through industries (Manufacturing, Services, Agriculture) to final destinations (Exports, Domestic). Each version answers a different kind of question — the geographic one shows where flows physically go, while the abstract Sankey shows how volume is distributed across categories.

---

## Project 3: Hierarchical Visualization with Treemaps and Sunbursts

**File:** [`Class_7_Assignment.ipynb`](./Class_7_Assignment.ipynb)

Two separate hierarchical-data projects built from live public APIs.

**US Exports Treemap (2022).** Data is pulled directly from the Observatory of Economic Complexity API at the HS2 commodity level with parent Section drilldowns, so that every commodity is automatically grouped under its parent sector. The raw response is cleaned (zero-value records removed, trade values converted to billions of dollars, long commodity names truncated for display), and then summarized at the sector level to expose how the total export portfolio splits across sectors. A two-level Plotly Express treemap (Sector → Commodity) sized by trade value uses a custom 21-color palette so that every sector is visually distinct. Hover and click interactions let the reader drill into any sector to see the underlying commodities.

**Global Energy Consumption Sunburst (2023).** Data is pulled from Our World in Data's energy dataset directly off GitHub. The country list is filtered to real countries only (aggregates like "World" and "Asia" are removed), the top 25 countries by total consumption are selected, and each country is mapped to its continent. The data is then melted from wide format to long format so each row is a single country-energy_source pair. Two sunburst diagrams are built: one organized by Continent → Country → Energy Source, and a second organized by Type (Fossil vs Renewable) → Source → Country. The two diagrams answer different questions — the first shows the energy mix of each country, the second shows which countries dominate each energy source.

---

## Project 4: Mid-Term — Multi-Source Business Analysis

**File:** [`Mid_Term_Projects_Final.ipynb`](./Mid_Term_Projects_Final.ipynb)

The mid-term combines everything from Projects 1, 2, and 3 into three independent analyses on three completely different datasets. The raw data files are uploaded separately to this repository.

### 4.1 COVID-19 Variant Analysis Across Time

WHO COVID-19 open data from 2020 through 2023 is loaded and aggregated to global weekly cases and global weekly deaths. The three major variant waves (Delta from June 2021 to October 2021, Omicron from December 2021 to March 2022, and Omicron XBB from November 2022 to February 2023) are overlaid on the time series as semi-transparent colored bands using `axvspan`, so the reader can see exactly when each variant was dominant and how each one shaped the global infection curve.

The country-level comparison takes the same data, filters to the United States, India, and Brazil, applies a 3-period rolling mean to smooth weekly volatility, and renders an animated Plotly line chart with one frame per month from January 2020 to December 2023. The animation shows how the three countries' death curves diverged over time. Finally, two world choropleth maps show cumulative case rates and cumulative death rates per country across the entire study window.

### 4.2 Levi's Direct-to-Consumer Expansion Recommendation

This analysis builds a scoring model to identify the best US cities for new Levi's retail stores. It uses three independent data sources:

| Source | Purpose |
| --- | --- |
| Apify Google Maps scraper | Current Levi's store locations and counts per city |
| simplemaps US cities database | City-level latitude, longitude, and population |
| US Census ACS5 API (B19013, B01001) | Median household income and 18–35 age group population per state |

The three datasets are cleaned, standardized on city and state keys, and merged into a single table. An opportunity score is calculated for each city using a weighted combination of median income, 18–35 population share, and total city population, with a penalty applied to cities where Levi's already has stores. The top expansion candidates are plotted on a Folium map alongside existing stores in different colors so the reader can immediately see where the model recommends new locations and how those locations relate to the current footprint.

### 4.3 Real Estate Investment Analysis Using Housing Price Trends

Zillow Home Value Index data is reshaped from wide format (one column per month) to long format (one row per city-month), missing values are handled, and time components are extracted. A 12-month moving average reveals long-term trends in the US national price index. Major cities are compared side-by-side on a per-year basis to surface which markets are accelerating and which are flattening. STL decomposition is applied to monthly data (period 12) to separate the cyclical and structural components of housing prices. Finally, a per-city investment score is calculated using long-term growth rate, recent momentum, and price stability, so that the analysis ends with a ranked recommendation rather than a chart.

---

## Project 5: Exploratory Data Analysis and Feature Engineering

**File:** [`Group_Assignment_4.ipynb`](./Group_Assignment_4.ipynb)

A comprehensive walkthrough of the EDA techniques that sit underneath every other project in this portfolio. Organized as Easy, Medium, and Hard problems.

**Easy problems.**

- *Exercise 1 — Simple Histogram Analysis.* Load student exam scores, compute mean, median, and standard deviation, then plot a histogram with 20 bins and overlay vertical lines for the mean (red dashed) and median (green dashed). Interpret skewness from the gap between mean and median.
- *Exercise 2 — Box Plot Comparison.* Load employee salaries, run data-quality checks (duplicates, missing values, unique departments), then build side-by-side box plots with Seaborn comparing salary distribution across departments. Identify outliers and highest-median department.
- *Exercise 3 — Scatter Plot Relationship.* Compute correlation between two continuous variables and build a scatter plot to visualize the relationship.

**Medium problems.**

- *Exercise 4 — Multi-Variable Distribution Analysis.* Apply log, square-root, and Box-Cox transformations to skewed variables, compare the resulting distributions side-by-side, and use IQR-based outlier detection to flag values outside 1.5×IQR.
- *Exercise 6 — Time Series Pattern Detection.* Prepare a time series, plot it with rolling statistics, analyze seasonality, and detect anomalies.

**Hard problem.**

- *Exercise 9 — Complete EDA with Feature Engineering.* A full end-to-end EDA: initial data profiling, univariate analysis on every variable, target-related analysis against the dependent variable, bivariate analysis between feature pairs, feature engineering driven by what the EDA exposed, final dataset preparation, and a written comprehensive report. This is the closest thing in the portfolio to a real-world analyst workflow from a raw CSV to a model-ready feature set.

---

## Project 6: Ethics, Dashboards, and Responsible Visualization

**File:** [`Class_10_Ethics_Data_Viz_Presentation.pptx`](./Class_10_Ethics_Data_Viz_Presentation.pptx)

A presentation analyzing what makes a visualization ethical, accessible, and useful, using paired bad-versus-good examples drawn from real published academic papers in *Nature*, the *Journal of Accounting and Economics*, the *Journal of Applied Clinical Medical Physics*, *Frontiers in Cardiovascular Medicine*, and *BMJ Evidence-Based Medicine*.

The deck is organized in three sections:

1. **Ethics and responsible visualization.** Walks through a real chart from a 2025 *Nature* paper on the readability of financial reports and identifies four specific problems: color misuse with nine near-identical hues, cherry-picking and survivorship bias from inconsistent start dates, affective priming through poorly chosen red highlights, and cognitive overload from packing 18 visual elements into one plot. The good counter-example is a 2008 paper from the *Journal of Accounting and Economics* that splits the same comparison into separate panels, uses a consistent time range, and applies a colorblind-safe palette.
2. **Dashboard design and KPI visualization.** Contrasts a clinical dashboard suffering from KPI overload (ten metrics shown at equal hierarchy, donut charts plus treemaps plus maps stacked together) against a real-time emergency-care dashboard that uses a clean hierarchy, color-coded urgency, and clear primary metrics.
3. **AI visualization and ROC analysis.** Examines a 2022 cardiovascular paper with ROC-curve mistakes and pairs it with a 2024 *BMJ EBM* article that explains how to avoid the same errors.

The deliverable is the presentation itself; there is no notebook for this assignment.

---

## Project 7: Stock Portfolio Investment Pitch

**File:** [`Final_Presentation_1.pptx`](./Final_Presentation_1.pptx)

A 28-slide investment pitch built around a single thesis: *In every gold rush, the people who reliably get rich are not the miners, they are the suppliers of picks and shovels.* The AI boom is treated as today's gold rush, and the portfolio invests in the companies whose hardware every AI company depends on.

The deck applies a four-step risk-analysis methodology to each holding: understand the competitive moat, review the latest earnings and valuation, classify risks by category and severity, and synthesize a final risk-reward view.

| Position | Thesis |
| --- | --- |
| ASML Holding | The world's only supplier of EUV lithography machines; sub-5nm chip production cannot happen without them. $45.5B backlog. Treated as the lowest-competition-risk semiconductor exposure available. |
| Broadcom Inc | Semiconductor and infrastructure software combined; benefits from both AI hardware buildout and the long-tail enterprise software layer above it. Bull-flag pattern and RSI analysis used to time entry. |
| AMD | The credible challenger to Nvidia in AI compute; new-generation chips launching 2025–2027 powering national AI infrastructure deals. |

The presentation includes risk vs return positioning charts, budget allocation across the three holdings within a $10M portfolio targeting 2030, five-year price charts with technical analysis annotations, and a 2025 shareholder-letter-driven argument that the entire AI industry is hitting a compute wall — which is precisely where this portfolio is positioned.

---

## Tech Stack

**Languages and environments.** Python 3.10+, Jupyter Notebook, Google Colab.

**Data manipulation.** Pandas, NumPy.

**Statistical analysis.** statsmodels (STL decomposition, ACF), SciPy (transformations and statistical tests).

**Static visualization.** Matplotlib, Seaborn.

**Interactive visualization.** Plotly Express (treemap, sunburst, animated charts), Plotly Graph Objects (Sankey, Scattergeo, Figure layouts), Folium (Choropleth, GeoJson, tooltips), GeoPandas.

**Data sources used.** WHO COVID-19 open data, Observatory of Economic Complexity API, Our World in Data, US Census ACS5 API, simplemaps US cities database, Zillow Home Value Index, Apify Google Maps scraper.

**Document tooling.** PowerPoint (presentations), PDF, Markdown.

---

## Repository Structure

```
Data-Visualization-Portfolio/
├── README.md                                       This file
├── Data
├── Class_5_Assignment_Final.ipynb                  Project 1 — time series
├── In_Class6_Assignment.ipynb                      Project 2 — choropleth and Sankey
├── Class_6_in_Class_Assignment.pdf                 Project 2 — class reference materials
├── Class_7_Assignment.ipynb                        Project 3 — treemap and sunburst
│
├── Mid_Term_Projects_Final.ipynb                   Project 4 — mid-term, three analyses
├── data/                                           (uploaded separately)
│   ├── WHO-COVID-19-global-data.csv
│   ├── Levis_stores_apify.csv
│   ├── uscities.csv
│   └── zillow_zhvi.csv
│
├── Group_Assignment_4.ipynb                        Project 5 — full EDA + feature engineering
│
├── Class_10_Ethics_Data_Viz_Presentation.pptx      Project 6 — ethics presentation
└── Final_Presentation_1.pptx                       Project 7 — stock portfolio pitch
```

---

## How to Reproduce

The notebooks run end-to-end in either a local Jupyter environment or Google Colab. Python 3.10 or later is required.

```
git clone <this repo>
cd Data-Visualization-Portfolio
pip install pandas numpy statsmodels matplotlib seaborn plotly folium geopandas requests openpyxl
jupyter notebook
```

Each notebook is self-contained. A few of them pull data live from public APIs (OEC for trade, Our World in Data for energy, US Census for demographics) and will work without any local data file. The COVID, Levi's, US cities, and Zillow analyses inside `Mid_Term_Projects_Final.ipynb` expect their CSV files to be present in the working directory; those files are uploaded separately to the `data/` folder of this repository.

---

## About

These projects were completed during the Data Visualization course as part of an analytics master's program. The work is part-individual and part-team, depending on the assignment. The team — *Radical Raccoons* — is credited inside the notebooks where the work was collaborative.

The portfolio is shared publicly so that future students, recruiters, and analysts can see a worked example of how to approach a wide range of visualization problems. If anything here is useful to your own work, feel free to fork the repository or open an issue with questions.
