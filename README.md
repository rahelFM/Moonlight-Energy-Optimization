## Moonlight Energy Optimization

# Overview
Moonlight Energy Optimization is a data analysis project focused on exploring and cleaning solar irradiance and weather data from multiple countries (Benin). The goal is to prepare high-quality, insightful datasets that will support energy optimization strategies in each region.

This repository hosts the code, notebooks, and processes used for data profiling, cleaning, and exploratory data analysis (EDA) of Benin dataset. 
## Data Description

The dataset (`benin-malanville.csv.csv') contains the following columns:

* **Timestamp (yyyy-mm-dd hh:mm):** Date and time of each observation.
* **GHI (W/m²):** Global Horizontal Irradiance.
* **DNI (W/m²):** Direct Normal Irradiance.
* **DHI (W/m²):** Diffuse Horizontal Irradiance.
* **ModA (W/m²):** Measurements from module/sensor A.
* **ModB (W/m²):** Measurements from module/sensor B.
* **Tamb (°C):** Ambient Temperature.
* **RH (%):** Relative Humidity.
* **WS (m/s):** Wind Speed.
* **WSgust (m/s):** Maximum Wind Gust Speed.
* **WSstdev (m/s):** Standard Deviation of Wind Speed.
* **WD (°N (to east)):** Wind Direction.
* **WDstdev:** Standard Deviation of Wind Direction.
* **BP (hPa):** Barometric Pressure.
* **Cleaning (1 or 0):** Indicates a cleaning event.
* **Precipitation (mm/min):** Precipitation rate.
* **TModA (°C):** Temperature of Module A.
* **TModB (°C):** Temperature of Module B.
* **Comments:** (Initially found to be entirely missing in this dataset)

## Task 1: Git & Environment Setup

Successfully set up a local Git environment, created a GitHub repository, and linked the local project to the remote repository. Basic Git commands (`add`, `commit`, `push`) were used to manage the project.

## Task 2: Profiling, Cleaning & EDA Outline
* Three ipynb files of EDA were created for the country. benin-eda, serrealeone-eda and toga-eda. 
### 2.1 Data Profiling Summary

* Loaded the  datasets using the `pandas` library.
* Inspected the initial rows and data types using `.head()` and `.info()`.
* Generated descriptive statistics for all columns using `.describe(include='all')`, providing insights into the distribution and range of values.
* Conducted a missing value analysis using `.isnull().sum()` and `.isnull().mean()`, revealing that the 'Comments' column is entirely empty.
* Checked for duplicate rows (result to be included if performed).

### 2.2 Planned Data Cleaning Steps

* Handling Missing Values
* Data Type Conversion
* Outlier Management
* Consistency Checks 
### 2.3 Exploratory Data Analysis (EDA) Plan

The EDA will involved the following:

* **Univariate Analysis:** Examining the distribution of individual features using boxplots. Analyzing the 'Cleaning' and 'Precipitation' columns.
* **Bivariate Analysis:** Analyzing how 'Cleaning' events correlate with other factors. Exploring temporal relationships.
* **Multivariate Analysis:** Exploring of relationships between multiple variables.
* **Time Series Analysis:** Analyzing trends and seasonality in key variables over time.

## Next Steps

The following steps will be undertaken:

* Complete the planned data cleaning steps for all three countries.
* Perform the country comparison analysis as outlined in the EDA plan.
* Document findings and observations in the repository (potentially in a dedicated notebook: `compare_countries.ipynb`).
* (Bonus) Develop a Streamlit application to visualize the insights.
* Prepare for subsequent tasks in the challenge.

## Libraries Used

* pandas
* numpy
* seaborn
* matplotlib
* scipy

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. 


