# weather-energy-analytics

## Project Overview
This project focuses on analyzing weather patterns and their correlation to energy consumption across the eastern coast of the USA. By leveraging historical weather data and energy consumption records, we aim to uncover insights that can help in predicting energy demand based on weather conditions. The resulting analysis will be visualized through a Power BI dashboard hosted on GitHub Pages, allowing users to interact with the data and gain valuable insights.

## Details
## Architecture & Data Pipeline

### Data Collection
- **Sources**: Open-Meteo Weather API and U.S. Energy Information Administration API
- **Tool**: Google Colab with Python and Pandas
- **Process**: Python scripts fetched data from both APIs and performed initial data cleaning and transformation

### Data Storage & Processing

#### Azure Blob Storage (Landing Zone)
Raw API data was archived to Azure Blob Storage before transformation. This serves as:
- **Data backup**: Original, unmodified API responses preserved
- **Audit trail**: Complete record of source data

The raw files are stored in a structured blob container organized by date and source (weather vs. energy data).

#### Data Transformation
- Cleaned and standardized both datasets using Pandas
- Aggregated weather and energy data by state and date
- Merged datasets on common dimensions (date, location)
- Created enriched dataframe ready for analytics

### Supabase PostgreSQL Database (Project Backend)
The cleaned and merged dataset was loaded into a Supabase PostgreSQL database, which:
- **Centralizes data**: Single source of truth for all analytics
- **Enables real-time queries**: Power BI connects directly to the database
- **Provides scalability**: Easily accommodate additional states or time periods
- **Supports analysis**: SQL queries for filtering, aggregation, and statistical analysis

### Analytics & Visualization
Power BI Desktop connected to the Supabase PostgreSQL database via the PostgreSQL connector to:
- Query 16 east coast states' weather and energy consumption data
- Explore correlations between temperature, humidity, and residential electricity usage
- Build interactive dashboards with filtering and drill-down capabilities

### Publishing
The final dashboard was published via Power BI Publish to Web and embedded into this GitHub Pages portfolio site for public access.

---

## Tech Stack
- **Data Collection**: Python, Pandas, REST APIs
- **Data Storage**: Azure Blob Storage, Supabase PostgreSQL
- **Analytics & Visualization**: Power BI Desktop
- **Hosting**: GitHub Pages

## Usage
To access the Power BI dashboard and view the results of the analysis, please visit GitHub Pages site: [https://levim03.github.io/]
