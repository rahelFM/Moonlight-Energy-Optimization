## Moonlight Energy Optimization

# Overview
Moonlight Energy Optimization is a data analysis project focused on exploring and cleaning solar irradiance and weather data from multiple countries (Benin, Sierra Leone, and Togo). The goal is to prepare high-quality, insightful datasets that will support energy optimization strategies in each region.

This repository hosts the code, notebooks, and processes used for data profiling, cleaning, and exploratory data analysis (EDA). 
## The ipynb EDA  files are in another branch and not merged on main branch, named as, benin-eda, sierraleon-eda and togo-eda. 
## Data Description

The dataset (`sierraleone-bumbuna.csv`,'benin-malanville.csv','togo-dapaong_qc.csv') contains the following columns:

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
* Three ipynb files of EDA were created for the country. benin-eda, serrealeone-eda and toga-eda. The files are in another branch and not merged on main branch. 
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


   ## # Task 3
## # Solar Irradiance Data Analysis

The project compare_countries.ipynb, analyzes solar irradiance data for three West African countries: **Benin**, **Togo**, and **Sierra Leone**. The goal is to compare and evaluate solar energy potential using key irradiance metrics:

- **GHI**: Global Horizontal Irradiance  
- **DNI**: Direct Normal Irradiance  
- **DHI**: Diffuse Horizontal Irradiance

## 📁 Project Structure
We compute:

Mean, median, and standard deviation for each irradiance metric

One-Way ANOVA and Kruskal-Wallis tests to assess country-level differences

Example Output:
Country	GHI_mean	DNI_mean	DHI_mean
Togo	230.56	151.26	116.44
Benin	240.56	167.19	115.36
Sierra Leone	139.54	67.17	93.90

ANOVA and Kruskal-Wallis p-values:

GHI differences between countries are statistically significant (p-value = 0.0).

📌 Key Insights
Togo shows the highest DHI and DNI values.

Benin has the highest GHI on average.

Sierra Leone consistently shows lower irradiance across all metrics.


## Libraries Used

* pandas
* numpy
* seaborn
* matplotlib
* scipy

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. 



