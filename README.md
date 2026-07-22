# SpaceX Falcon 9 First Stage Landing Prediction
**IBM Applied Data Science Capstone Project**

## Project Overview
SpaceX advertises Falcon 9 rocket launches at a cost of $62 million, which is significantly lower than competitors whose costs often exceed $165 million. A primary driver of this cost reduction is SpaceX's ability to successfully land and reuse the first stage of the Falcon 9 rocket. 

The goal of this project is to predict whether the first stage of the Falcon 9 rocket will land successfully. By accurately predicting these outcomes, alternate commercial entities can better estimate launch costs and bid effectively against SpaceX for satellite deployments.

## Methodologies
This project follows a complete end-to-end data science lifecycle:
1. **Data Collection:** Extracted historical launch records utilizing the SpaceX REST API and implemented web scraping using `BeautifulSoup` to gather supplementary data from Wikipedia.
2. **Data Wrangling:** Cleaned and formatted the raw data, handled missing values, and engineered new features to prepare the dataset for analysis and machine learning.
3. **Exploratory Data Analysis (EDA):** Loaded the data into a Db2 database to execute SQL queries. Utilized `Matplotlib` and `Seaborn` to visualize data distributions and uncover relationships between variables (e.g., payload mass, launch site, and success rates).
4. **Interactive Visual Analytics:** * Built interactive maps using `Folium` to analyze the geographical layout of launch sites and their proximity to coastlines and highways.
    * Developed a dynamic, interactive dashboard using `Plotly Dash` to allow users to filter launch success rates by site and payload mass.
5. **Predictive Modeling:** Standardized the dataset and trained multiple classification models, including Logistic Regression, Support Vector Machines (SVM), K-Nearest Neighbors (KNN), and Decision Trees. Hyperparameters were optimized using `GridSearchCV`.

## Key Results
* **Geographical Insights:** Launch success varies by location, with KSC LC-39A emerging as the most reliable launch facility.
* **Payload Impact:** Successful landings are more frequent across all orbit types for payloads under 6,000 kg. Heavier payloads show a mix of successes and failures.
* **Machine Learning Performance:** The **Decision Tree** algorithm achieved the highest predictive accuracy at **88.88%** on the test data, outperforming Logistic Regression, SVM, and KNN (which all scored 83.33%). 

## Repository Contents
This repository contains the Jupyter Notebooks documenting each phase of the project:
* `1. jupyter-labs-spacex-data-collection-api.ipynb`: Data extraction via SpaceX API.
* `2. jupyter-labs-webscraping.ipynb`: Data extraction via web scraping Wikipedia.
* `3. labs-jupyter-spacex-Data wrangling.ipynb`: Data cleaning and feature engineering.
* `4. jupyter-labs-eda-sql-coursera_sqllite.ipynb`: Exploratory data analysis using SQL.
* `5. jupyter-labs-eda-dataviz.ipynb`: Exploratory data analysis using Python visualization libraries.
* `6. lab_jupyter_launch_site_location.ipynb`: Interactive geographical analysis using Folium.
* `7. SpaceX_Machine_Learning_Prediction_Part_5.jupyterlite.ipynb`: Machine learning model development and evaluation.
