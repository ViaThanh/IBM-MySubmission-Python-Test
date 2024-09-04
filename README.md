# IBM Data Science Capstone Project - SpaceX

## Summary
This report evaluates machine learning models for predicting the landing success of SpaceX's Falcon 9 rocket. The process involves:
- Data preprocessing, model training, and hyperparameter tuning.
- Analyzing data from APIs and web sources using EDA, visualizations, and SQL.
- Integrating insights into an interactive dashboard.
- Identifying the best-performing model, which is the Decision Tree, and evaluating it using key metrics.

## Introduction
The commercial space age has arrived, led by companies like Virgin Galactic, Rocket Lab, Blue Origin, and SpaceX. SpaceX has revolutionized space travel by making it more affordable through the use of reusable rockets. This project aims to develop a model to predict the landing success of SpaceX's Falcon 9 first stage. Accurate predictions can inform cost estimates and optimize mission planning.

## Methodology

### Tools: Jupyter Notebook 

### Data Collection & Data Wrangling
**Data Collection:**  
Data was sourced from the SpaceX API and additional web scraping.

**Data Wrangling:**  
Initial data cleaning and feature engineering were performed to prepare the data for analysis.

### EDA with Visualization
1. **Scatterplot for Flight Number and Payload:** Higher flight numbers and payloads are often associated with successful landings.
2. **Scatterplot for Flight Number and Launch Site:** This plot shows how different launch sites handle various flight numbers.
3. **Scatterplot for Payload Mass and Launch Site:** Observes mass differences across sites.
4. **Bar Plot for Success Rate by Orbit Type:** Displays success patterns for different orbits.
5. **Scatterplot for Flight Number and Orbit Type:** Examines trends related to orbits and payload mass.
6. **Line Plot for Yearly Launch Success Trend:** Shows success trends over time.

### EDA with SQL
SQL queries were written and executed to address specific tasks:
- Displaying unique launch site names.
- Showing 5 records of launch sites starting with 'CCA'.
- Displaying the total payload mass carried by NASA (CRS) boosters.
- Displaying the average payload mass for booster version F9 v1.1.
- Listing the date of the first successful ground pad landing.

### Maps with Folium
Interactive visual analytics were performed using Folium, including:
- **Map Initialization:** Centered on NASA Johnson Space Center.
- **Circles and Markers:** A blue circle and marker were added at the NASA Johnson Space Center's coordinates with popup labels.
- **Mouse Position:** A feature was added to display coordinates when hovering over the map.
- **Proximity Analysis:** Lines were drawn to show distances between launch sites and points of interest using `folium.PolyLine`.

### Dashboard with Plotly Dash
Plots and interactions were integrated into a dashboard:
- A dropdown list for selecting Launch Sites.
- A pie chart displaying the total count of successful launches for all sites.
- A slider to choose the payload range.
- A scatter chart illustrating the correlation between payload and launch success.
![Dashboard](https://github.com/ViaThanh/Project_IBM_SpaceX_DS/blob/a88234dc40c156f3962a86c8a963a2b8413fb3b2/Dash_Dashboard.png)

### Predictive Analytics
- **Model:** Various classification algorithms, including Logistic Regression, SVM, Decision Tree Classifier, and KNN, were employed.
- **Grid Search:** Used to identify the optimal settings for each model.
- **Training and Testing:** The dataset was split into training and testing sets to evaluate model performance.
- **Performance Metrics:** Accuracy, precision, recall, F1-score, and confusion matrix were used to assess and compare model effectiveness.

**Final Model:**  
The Decision Tree model, which achieved the best performance metrics, was selected as the final predictive model for Falcon 9 landing success.

## Conclusions
- As the Flight Number increases, the likelihood of successful landings also rises.
- Certain orbits, such as ES-L1, GEO, HEO, and SSO, have a 100% success rate.
- Since 2013, the success rate has consistently increased, indicating a strong positive trend.
- Launch sites near the equator, railways, highways, coastlines, and remote areas are ideal due to ease of transportation, safety, and minimal environmental impact.
- KSC LC-39A has the highest number of successful launches.
- The payload range of 2k-5.5k has the highest launch success rate.
- The Decision Tree model was identified as the best-performing model with a score of 0.875.

This project successfully developed a predictive model for Falcon 9's first stage landing success, supported by thorough data analysis and visualization. The provided files, plots, and interactive dashboards offer stakeholders an intuitive tool to explore data and insights. Future efforts will focus on refining the model and enhancing the dashboard's features.
