# Melbourne Housing - data cleanin & visualisation
Project involving the cleaning of a “dirty” dataset of Melbourne Housing.

Link: https://www.kaggle.com/datasets/dansbecker/melbourne-housing-snapshot

## About dataset
The dataset includes 21 columns and 13,580 rows with information about Melbourne housing properties including address, type, suburb, price, rooms, bedrooms, bathrooms, car spaces, land size, building area, year built, distance from CBD, region name, council area, and sale details.

## What was done
Cleaned data: removed invalid year_built, building_area < 15m², filled missing values. Result: 12,211 clean rows

Created visualizations: price histogram, log-scale price, boxplot by type, correlation matrix, feature importance chart

Built 6 new features: age, sale_year, sale_month, has_year_built, has_building_area, suburb_freq

Trained 3 models: DummyRegressor (baseline), LinearRegression, RandomForest (best: MAE $169k, R² 1.0)

## Conclusions
The Random Forest model predicts house price with MAE of 169,000$. Key findings: location is most important (20.9%), followed by property size (27%). Houses cost significantly more than units, and farther properties are cheaper. The model works well but may overfit to training data. Adding external features like school ratings or crime data could improve accuracy. The cleaned dataset and feature engineering provide a good foundation for price prediction.

## Future Improvements
The model could be improved by adding external features like school ratings, crime data, and public transport information. Since the dataset is from 2017, collecting more recent data would help reflect current market conditions. Advanced models like XGBoost or GradientBoosting might provide better predictions than RandomForest. Better handling of expensive properties over $3 million would prevent outliers from distorting results. Finally, using cross-validation instead of a single train-test split would give more robust evaluation of model performance.

## Visualization

Price distribution histogram, log-scale price distribution, price by property type boxplot, correlation heatmap, top 15 feature importance bar chart.

## Project structure
Melbourne_Housing/

├── data/

│     └── melb_data.csv

├── notebooks/

│     └── melbourn_housing.ipynb

|     └── melbourn_housing (group_notebook).ipynb

├── tasks/

|     └── task.md

|     └── task_medium.md

└── README.md

## Tech Stack
Python, pandas, numpy, scikit-learn (RandomForestRegressor, SimpleImputer, OneHotEncoder, ColumnTransformer), matplotlib.

