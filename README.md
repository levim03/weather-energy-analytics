# weather-energy-analytics

## Project Overview
This project focuses on analyzing weather patterns and their correlation to energy consumption across the eastern coast of the USA. By leveraging historical weather data and energy consumption records, we aim to uncover insights that can help in predicting energy demand based on weather conditions. The resulting analysis will be visualized through a Power BI dashboard hosted on GitHub Pages, allowing users to interact with the data and gain valuable insights.

## Details
Data was pulled from two public REST APIs (Open-Meteo and U.S. Energy Information Administration) using a Jupyter Notebook hosted on Google Colab. Python and Pandas were used to clean, transform, and aggregate the data into structured dataframes. Raw data files were archived to Azure Blob Storage as a landing zone before transformation. The cleaned and merged dataset was loaded into a Supabase PostgreSQL database which serves as the project backend. Supabase was connected to Power BI Desktop via the PostgreSQL connector to build interactive visualizations exploring the correlation between temperature, humidity, and residential electricity consumption across 16 east coast states. The finished dashboard was published publicly via Power BI Publish to Web and embedded into a GitHub Pages portfolio site.

## Features
- Comprehensive analysis of weather data including temperature, humidity, precipitation
- Correlation analysis between weather patterns and energy consumption metrics.
- Interactive visualizations utilizing Power BI to display data trends and insights.
- Accessibility across different devices with responsive design.

## Usage
To access the Power BI dashboard and view the results of the analysis, please visit GitHub Pages site: [https://levim03.github.io/]
