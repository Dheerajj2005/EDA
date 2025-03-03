# Exploratory Data Analysis (EDA) Repository

This repository contains Exploratory Data Analysis (EDA) performed on several datasets. It also includes a guide on how to conduct effective EDA.

## Datasets Analyzed

* **Dataset 1:** [Diwali Sales Analysis]
* **Dataset 2:** [IPL Data Analysis]
* **Dataset 3:** [Titanic Dataset Analysis]
* **Guide on how to do EDA** 

## Purpose

The purpose of this repository is to:

* Demonstrate practical EDA techniques.
* Provide insights into the analyzed datasets.
* Offer a learning resource for those interested in data exploration.

## How to Perform EDA

Here's a general workflow for conducting Exploratory Data Analysis:

1.  **Import Libraries:**
    * Start by importing necessary Python libraries, such as `pandas`, `numpy`, `matplotlib`, and `seaborn`.
    ```python
    import pandas as pd
    import numpy as np
    import matplotlib.pyplot as plt
    import seaborn as sns
    ```

2.  **Load the Dataset:**
    * Load your dataset into a pandas DataFrame.
    ```python
    df = pd.read_csv('your_dataset.csv')
    ```

3.  **Data Inspection:**
    * Examine the dataset's structure, including:
        * Shape (number of rows and columns).
        * Column names and data types.
        * First few rows using `df.head()`.
        * Last few rows using `df.tail()`.
        * Information about the dataset `df.info()`
        * Descriptive statistics `df.describe()`

4.  **Data Cleaning:**
    * Handle missing values:
        * Identify missing values using `df.isnull().sum()`.
        * Decide how to handle them (e.g., imputation, removal).
    * Handle duplicates:
        * Identify duplicate rows `df.duplicated().sum()`
        * Remove duplicate rows `df.drop_duplicates(inplace=True)`
    * Correct data types.
    * Handle outliers.

5.  **Univariate Analysis:**
    * Analyze individual variables:
        * For numerical variables, use histograms, box plots, and descriptive statistics.
        * For categorical variables, use bar charts and value counts.

6.  **Bivariate and Multivariate Analysis:**
    * Explore relationships between variables:
        * Use scatter plots for numerical-numerical relationships.
        * Use box plots or violin plots for numerical-categorical relationships.
        * Use count plots or grouped bar charts for categorical-categorical relationships.
        * Create correlation matrices, and heatmaps.

7.  **Data Visualization:**
    * Use visualizations to communicate your findings effectively.
    * Label your plots clearly.
    * Use appropriate plot types.

8.  **Generate a Profile Report (using ydata-profiling):**
    * Generate an html file with a full report of the dataset.
    ```python
    from ydata_profiling import ProfileReport
    prof = ProfileReport(df)
    prof.to_file(output_file='output.html')
    ```

9.  **Document Your Findings:**
    * Record your observations and insights.
    * Draw conclusions based on your analysis.

## Repository Structure
