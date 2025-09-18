🏠 Airbnb Price Prediction (Regression Project)

📌 Problem Statement
The objective of this project is to predict the log-transformed price of Airbnb listings using features such as property type, room type, location, and review ratings.
This is a supervised regression task, where the target variable is continuous (log_price).

📊 Dataset
Source: Airbnb dataset (Kaggle).
Size: ~71111 rows and 30 columns
Target Variable: log_price (logarithm of listing price).

🛠️ Steps Taken

1. Data Cleaning

Checked dataset shape and previewed features.
Selected relevant columns related to Airbnb pricing.
Handled missing values:
Filled bathrooms, bedrooms, and beds with most frequent value.
Filled neighbourhood with most common value (Williamsburg).
Filled review scores with mean rating.

2. Feature Engineering

Encoded categorical variables using Label Encoding.
Ensured all features were numeric.
Computed correlations with the target variable.

3. Exploratory Data Analysis (EDA)

Plotted:

Top 10 property types by maximum price.
Average price based on review scores.
Room type distribution.
Histogram of log prices.
Listings count by city.
Correlation heatmap.

Key insight: property type, city, and room type had strong influence on price.

4. Model Building

Split dataset: 80% train / 20% test.
Baseline model: Linear Regression.
Validated regression assumptions:
Linearity, normality, homoscedasticity, independence of errors.

5. Model Comparison

Linear Regression
Ridge Regression (L2 regularization)
Lasso Regression (L1 regularization)
Random Forest Regressor

6. Hyperparameter Tuning

Used GridSearchCV to tune Random Forest parameters:
Number of trees (n_estimators)
Maximum depth (max_depth)
Minimum samples per split and leaf

7. Final Model

Best Model: Random Forest Regressor
Achieved highest R² score and lowest RMSE compared to other models.
Extracted feature importance, showing property type, city, and reviews were the most impactful features.

📈 Results
Model	              R² Score      	RMSE
Linear Regression	  ~0.5061	        ~0.4564
Ridge Regression	  ~0.5061         ~0.4564
Lasso Regression	  ~0.5037         ~0.4575
Random Forest	      ~0.6024	        ~0.4095

🔑 Key Insights

Property type and city are major determinants of price.
Review ratings also influence price positively.

Random Forest outperformed linear models, capturing non-linear relationships.
