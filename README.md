Project Overview
The goal of this project is to predict whether the Falcon 9 first stage will land successfully. Landing the first stage significantly reduces the cost of space travel (SpaceX saves millions per launch by reusing boosters). By predicting the landing outcome, we can estimate the cost of a launch and compare it against other providers.

What I Did (The Process)
This project followed a full data science workflow:

1. Data Collection & Wrangling
API Integration: Pulled real-time launch data from the SpaceX API.

Web Scraping: Scraped Wikipedia tables using BeautifulSoup to gather historical launch data.

Data Cleaning: Handled missing values (especially in the 'Payload Mass' column) and created a binary Class column (1 for successful landing, 0 for failure).

2. Exploratory Data Analysis (EDA)
SQL Queries: Used SQL to perform complex queries on launch sites, success rates, and total payload mass.

Visualization: Used Matplotlib and Seaborn to discover patterns between Orbit types, Payload mass, and Launch Sites.

3. Interactive Maps & Dashboards
Folium Maps: Created interactive maps to visualize launch site locations and proximity to coastlines/highways.

Plotly Dash: Built a functional web dashboard with:

Dropdown menus to filter by site.

Range sliders to filter by Payload weight.

Pie and Scatter charts that update dynamically.

4. Machine Learning Classification
Pre-processing: Standardized data using StandardScaler.

Modeling: Trained and tuned four models:

Logistic Regression

Support Vector Machine (SVM)

Decision Tree

K-Nearest Neighbors (KNN)

Optimization: Used GridSearchCV to find the best hyperparameters for each model.

Key Results
Best Performing Model: All models performed similarly on the test set with an accuracy of approximately 87%.

Insight: Decision Tree models showed a slight tendency toward overfitting compared to the more stable Logistic Regression.
