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

## Visualization

Price distribution histogram, log-scale price distribution, price by property type boxplot, correlation heatmap, top 15 feature importance bar chart.

## Project structure
Melbourne_Housing/
├── data/
│   └── melb_data.csv
├── notebooks/
│   └── melbourn_housing.ipynb
|   └── melbourn_housing (group_notebook).ipynb
├── tasks/
|   └── task.md
|   └── task_medium.md
└── README.md

## Tech Stack
Python, pandas, numpy, scikit-learn (RandomForestRegressor, SimpleImputer, OneHotEncoder, ColumnTransformer), matplotlib.

