## E-Commerce Sales Data Analysis across Python-SQL-Tableau

This is a personal side project focused on building an integrated data pipeline between **Python**, **SQL**, and **Tableau**. It demonstrates how to perform exploratory data analysis (EDA) in a Jupyter environment and export the results for high-performance visualization in Tableau.

<ins>Key Features</ins>
- **Integration**: Works seamlessly across Python, SQL (via the Hyper Kernel), and Tableau.
- **Interactive**: Includes `pygwalker`, allowing for a Tableau-like drag-and-drop experience directly inside JupyterLab.

### **1. Dataframe to Tableau extract file (.hyper)**
*df_ETL_to_tableau.ipynb*  (run on python)  
- Extract: Fetch dataset with `kagglehub` and read as `pd.DataFrame`
- Transform: Handle missing data and generate visualizations with `matplotlib` or `seaborn`
- Load: Export cleaned dataframe to Tableau extract file (.hyper format) via `pantab.frame_to_hyper` for Tableau integration.

The cleaned data will be saved as 
- `ecommerce_cleaned.hyper`, which you can immediately open in Tableau for dashboarding
- `cleaned_amazon_sales.csv`


### **2. Read table(s) from Tableau extract file (.hyper) and query data with SQL**
*read_df_frim_tableau.ipynb*  (run on python)
- Read table(s) from .hyper file as dataframe with `pantab.frame_from_hyper`
- Visualize data with Tableau-like interactive UI via PyGWalker `pyg.walk`
- Execute SQL queries against the .hyper extract via `pantab.frame_from_hyper_query`


### **3. SQL integration with Tableau's Hyper API**  
*tableau_hypersql_interface.ipynb*  (run on hyper kernel)
- Mounting .hyper file to SQL
- Native SQL Execution: Utilized full SQL syntax (PostgreSQL-compatible) to to query data and also export query data to csv

The query results are saved as `highest_value_categories_results.csv`


### Requirements
To run this notebook, you will need:
- Python 3.x
- The libraries listed in `requirements.txt`

### Instructions
1. Install prerequisites:  
   ```python
   pip install -r requirements.txt
   ```
2. **Setup the Hyper Kernel:** Run this command in your terminal or your Jupyter Notebook/Lab cell to ensure the packages are installed into your active environment and register the kernel for the Jupyter Launcher.  
    ```python
    python -m hyper_kernel.install
    ```
