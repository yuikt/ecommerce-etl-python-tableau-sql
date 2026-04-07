# E-Commerce Sales Data Analysis & Tableau Integration

This is a personal side project focused on building an integrated data pipeline between **Python**, **SQL**, and **Tableau**. It demonstrates how to perform exploratory data analysis (EDA) in a Jupyter environment and export the results for high-performance visualization in Tableau.

## Overview
1.  **Data Acquisition**: Using `kagglehub` to fetch the ecommerce public dataset of orders made at Olist Store.
2.  **Data Cleaning and EDA**: Handling missing values using Pandas.
3.  **Visualization**: Generating statistical plots with Seaborn and Matplotlib to understand category performance.
4.  **Tableau Integration**: Exporting the cleaned DataFrame directly into a `.hyper` file format (Tableau's high-performance data engine) using the `pantab` library.

## Key Features
- **Integration**: Works seamlessly across Python, SQL (via the Hyper Kernel), and Tableau.
- **Performance**: Uses Tableau's Hyper API for faster data loading compared to traditional CSV exports.
- **Interactive**: Includes `pygwalker`, allowing for a Tableau-like drag-and-drop experience directly inside JupyterLab.

## Requirements
To run this notebook, you will need:
- Python 3.x
- The libraries listed in `requirements.txt`

## Instructions
1. Install prerequisites:  
   ```python
   pip install -r requirements.txt
   ```
2. **Setup the Hyper Kernel:** Run this command in your terminal or your Jupyter Notebook/Lab cell to ensure the packages are installed into your active environment and register the kernel for the Jupyter Launcher.  
    ```python
    python -m hyper_kernel.install
    ```
3. Run the notebook `ecommerce_DF-TableauExtract.ipynb`.
4. The cleaned data will be saved as `ecommerce_cleaned.hyper`, which you can immediately open in Tableau for dashboarding.
