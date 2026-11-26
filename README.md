# Air Quality & Weather Data Integration

## Project Overview

This project investigates the relationship between
meteorological conditions and PM10 concentrations
in the provinces of Milan and Sondrio, Italy.

The analysis compares the first quarters of 2024
and 2025, integrating air quality measurements
from eight monitoring stations with historical
weather data.

The project was developed as part of the Data
Management course of the MSc in Data Science at
the University of Milano-Bicocca (2025/2026).

## Objectives

- Collect data from multiple heterogeneous sources.
- Build a data acquisition and integration pipeline.
- Clean and standardize environmental data.
- Store and integrate data using a NoSQL database.
- Investigate relationships between weather
  conditions and PM10 concentrations.
- Compare pollution patterns in urban and alpine
  environments.

## Data Sources

- **ARPA Lombardia:** PM10 measurements and
  monitoring station metadata, obtained through
  the Regione Lombardia Open Data portal.
- **Open-Meteo API:** Historical weather data,
  including minimum temperature, maximum wind
  speed, precipitation amount and precipitation
  duration.

The analysis covers January–March 2024 and
January–March 2025.

## Technologies and Tools

- Python
- Pandas
- MongoDB
- REST API (Open-Meteo)
- Jupyter Notebook
- Flourish

## Methodology

1. **Data Acquisition:** Collection of air quality
   datasets and historical weather data through
   API requests.

2. **Data Cleaning:** Filtering, date formatting,
   coordinate standardization and numerical
   data conversion.

3. **Data Storage:** Organization of the datasets
   in MongoDB collections.

4. **Data Integration:** Integration of air quality
   and weather data using MongoDB aggregation
   operations based on date, latitude and longitude.

5. **Data Quality:** Evaluation of completeness,
   consistency, currency and accuracy.

6. **Data Analysis:** Exploratory analysis,
   correlation analysis and comparison of PM10
   concentrations across locations and years.

7. **Data Visualization:** Visual representation
   of pollution distributions and weather trends.

## Key Findings

The average PM10 concentrations reported in the
project were:

| Province | 2024 | 2025 |
|----------|------|------|
| Milan | 40.03 | 39.44 |
| Sondrio | 21.07 | 25.25 |

Values are expressed in µg/m³.

- Milan consistently recorded higher average
  PM10 concentrations than Sondrio.
- Sondrio experienced an approximately 20%
  increase in average PM10 concentrations in 2025.
- Precipitation duration showed a negative
  correlation with PM10 concentrations (-0.24).
- Altitude showed a negative correlation with
  PM10 concentrations (-0.29).
- Low temperatures and limited wind were
  associated with episodes of pollutant accumulation.

These findings describe observed relationships
and do not establish causality.

## Repository Structure

- `Data acquisition/` — Original and processed
  air quality and weather datasets.
- `Data Integration/` — Integrated datasets
  exported from MongoDB.
- `graphs/` — Visualizations and supporting data.
- `New_CODE.ipynb` — Main Python notebook.
- `pm10.csv` — Final cleaned dataset.
- `requirements.txt` — Python dependencies.
- `README.md` — Project documentation.

## Getting Started

Install the required Python libraries:

```bash
pip install -r requirements.txt
```

Open `New_CODE.ipynb` using Jupyter Notebook
or Visual Studio Code.

The repository contains previously integrated
datasets. Repeating the original database
integration requires a MongoDB environment.

## Future Improvements

- Extend the analysis to additional pollutants.
- Include more monitoring stations and longer
  observation periods.
- Develop machine learning models to predict
  future PM10 concentrations.
- Automate the data integration pipeline.

## Acknowledgements

This project was developed collaboratively as
a university group project for the Data Management
course at the University of Milano-Bicocca.

## Project Documentation

- [Project Report](docs/Data_Management_Report.pdf)
- [Project Presentation](docs/Presentation_Margni_Rubini_Villa.pdf)