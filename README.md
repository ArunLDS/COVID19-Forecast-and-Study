# Covid-19 Forecast & Study

## Overview
The primary objective of this project is to analyze and visualize the global impact of COVID-19, with a focus on infection rates, recovery, and mortality. Additionally, the project also aims to predict the number of cases expected in the upcoming week based on current trends. ALso, by studying the COVID-19 data, we aim to derive valuable insights, create informative visualizations, and apply advanced time series modeling for accurate future projections.

## Dataset
This dataset gives a detailed look at the COVID-19 pandemic, containing data on confirmed cases, deaths, and recoveries across various countries and regions. Each entry includes information on the location (country/region and latitude/longitude), date, and the number of confirmed, active, recovered, and deceased cases. Additionally, it classifies each entry by the WHO region. Starting from January 22, 2020 to July 27, 2020

## EDA & Data Preprocessing
- The dataset includes 10 columns and it has a significant portion of missing values in the Province/State column (34,404 missing out of 49,068).
- The Date column is initially in an object format and later converted to datetime.
- The Confirmed, Deaths, and Recovered columns represent cumulative counts per entry
- The Province/State column has 78 unique values. The Country/Region column has 187 unique values, with China having the highest frequency.
- No duplicate entries are found and the incomplete Province/State feature is dropped

## Data Visualization
- The dataset was first grouped by date to sum up global counts of confirmed, deaths, recovered, and active cases.
- A line graph was created to visualize the progression of COVID-19 worldwide, highlighting trends over time.
- A bar chart was created to visualize the top 20 regions most impacted by COVID-19 as of the last date in the dataset (July 27, 2020). The regions are ranked by the number of confirmed cases, and additional metrics for active cases, recoveries, and deaths are displayed.
- An interactive Sunburst chart was plotted showing the distribution of confirmed cases across different regions and countries
- An interactive Choropleth Map was plotted using plotly, which visualizes recovered cases worldwide, highlighting the geographic area and recovery rates of that area.
- An Animated Choropleth Map was plotted which shows the progression of COVID-19 cases over time, providing a dynamic view of the pandemic's spread.

## Model Building & Forecasting
- Time series models are built using the Prophet library to forecast future trends in confirmed and recovered cases.
- These dataframes are grouped by date, and columns are renamed for compatibility with the Prophet model.
- Trends for infection and recovery rates are visualized using interactive plots. The visualizations include the overall trend and weekly seasonality for both confirmed and recovered cases.
- A forecast plot is created to visualize the predicted COVID-19 cases, with actual values shown as dotted lines.
