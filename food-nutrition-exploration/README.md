# Branded Food Nutrition Data Exploration
This project explores a large food‑nutrition dataset by performing heavy preprocessing, feature creation, and light exploratory analysis. The goal was to clean and enrich the raw data, then use a separate small website to generate interactive visualizations and reports.

## Datasets
This project uses the USDA Branded Food Products Database [Data set]. Retrieved from [https://fdc.nal.usda.gov/fdc-datasets/FoodData_Central_branded_food_csv_2024-04-18.zip].  

1. Primary Branded Food Dataset
**Source:** branded_food

**Description:** Contains branded foods and private-label products information for a wide range of foods.

**Key fields:** brand name, brand owner, ingredients, branded food category.

2. Nutrition Dataset
**Source:** food_nutrient

**Description:** Contains detailed nutrient information for a wide range of foods from primary dataset.

**Key fields:** food brand id, nutrient id, amount

3. Nutrient Dataset
**Source:**  nutrient

**Description:** Contains all the nutrients considered in the nutritional information dataset.

**Key fields:** id, name

How They Were Used Together
Main datasets were cleaned and standardized during preprocessing

Joined/merged on food brand id, nutrition id, nutrient id

Combined dataset was used for exploration and visualization

## Project Structure
01-data-preprocessing.ipynb   → heavy cleaning, Dask processing, feature engineering  
02-data-exploration.ipynb     → light exploration, sanity checks, summary insights  
(report visuals hosted separately)

## Key Steps
1. Data Preprocessing (Dask)
Loaded a large nutrition dataset using Dask for parallelized processing

Cleaned missing or inconsistent values

Standardized units and column formats

Engineered new carb to fiber ratios feature

Exported a refined dataset for exploration and visualization

2. Light Exploration
Verified distributions and ranges

Identified outliers and unusual food nutrition information

Prepared summary tables for the reporting website

## Visualizations & Reports
The final visualizations were presented through a custom dashboard website built outside this notebook environment.

They include:

Top best options in terms of brands carb-to-fiber ratio categories

Category‑level comparisons

Interactive filtering

## Tools & Technologies

Python

Dask for scalable preprocessing

Pandas for final adjustments

Numpy for efficient numerical operations

Jupyter Notebooks and website-based external tools

Flask to build a lightweight backend for the dashboard, serving processed data and powering interactive visualizations.

Elasticsearch (Docker) to provide fast, flexible search and filtering across the nutrition datasets for real‑time dashboard queries.

jQuery, Chart.js, DataTables.js for visualizations and filtering
