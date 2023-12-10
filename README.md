# Diamond Price Prediction

## Project Overview
### Introduction

The **Diamond Price Prediction** project is an end-to-end model designed to predict the price of diamonds using regression analysis. The primary objective is to leverage various features such as carat, cut quality, color, clarity, dimensions, and more to accurately estimate the price of a given diamond.

The project employs a variety of regression models for optimal prediction accuracy, including Linear Regression, Lasso Regression for feature selection, Ridge Regression to prevent multicollinearity, and ElasticNet Regression, which combines feature selection and coefficient shrinkage. The effectiveness of these models is rigorously evaluated using industry-standard metrics:

## Why Diamond Price Prediction Matters
- **Industry Relevance:** In the ever-growing diamond industry, predicting prices accurately is crucial for various stakeholders, including jewelers, investors, and consumers.

- **Business Insights:** The project provides valuable insights into the factors influencing diamond prices, offering a deeper understanding of market trends.

### Data Overview :

**The dataset** The goal is to predict `price` of given diamond (Regression Analysis).

There are 10 independent variables (including `id`):

* `id` : unique identifier of each diamond
* `carat` : Carat (ct.) refers to the unique unit of weight measurement used exclusively to weigh gemstones and diamonds.
* `cut` : Quality of Diamond Cut
* `color` : Color of Diamond
* `clarity` : Diamond clarity is a measure of the purity and rarity of the stone, graded by the visibility of these characteristics under 10-power magnification.
* `depth` : The depth of diamond is its height (in millimeters) measured from the culet (bottom tip) to the table (flat, top surface)
* `table` : A diamond's table is the facet which can be seen when the stone is viewed face up.
* `x` : Diamond X dimension
* `y` : Diamond Y dimension
* `x` : Diamond Z dimension

Target variable:
* `price`: Price of the given Diamond.

## Pipelines

### Training Pipeline
The **training pipeline** automates the entire model development process

- **Data Ingestion:** Reads data from the source, initiating the process.
- **Data Transformation:** Conducts Exploratory Data Analysis (EDA), Feature Engineering (FE), and Feature Selection (FS).
- **Model Training:** Utilizes the prepared data for model training.
- **Hyperparameter Tuning:** Optimizes model performance for accurate predictions.
- **Model Evaluation:** Rigorous assessment of the model using industry-standard metrics.

The architecture follows a sequential flow:

**Data Ingestion → Data Transformation (FE, FS) → Model Training → Hyperparameter Tuning → Model Evaluation**

### Prediction Pipeline
The **prediction pipeline** efficiently serves queries and receives predictions through API.

## Error Handling and Logging
### Exception Handling:
The project incorporates a custom exception (CustomException) for graceful error handling. This tailored exception captures crucial details like script name and line number, enhancing error reporting for effective debugging.

### Logging Mechanism:
A robust logging setup is implemented, generating unique log files with timestamps. This logging mechanism provides insights into project execution, aiding transparency and facilitating issue identification during development, training, and deployment.

## Metrics Used
The model is evaluated using the following metrics:

- **R2 Score:** Measures the proportion of the response variable's variance captured by the model.
- **Mean Absolute Error (MAE):** Quantifies the average absolute differences between predicted and actual values.
- **Mean Squared Error (MSE):** Evaluates the average squared differences between predicted and actual values.

## Installation
To install the necessary dependencies, run:
```bash
pip install -r requirements.txt
```

## How to Run the model:
In order to run the model, use following command:
```bash
python run application.py
```

## Conclusion

In conclusion, after training models on diamond data to predict diamond prices, the Linear Regression, Lasso, and Ridge models exhibit similar and promising performance, with low Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and high R2 scores around 93.7%. However, the Elasticnet model shows inferior performance with higher RMSE, MAE, and a lower R2 score of 85.6%. 
