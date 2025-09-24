# Airbnb Data Cleaning with Pandas

This project focuses on the comprehensive cleaning and preprocessing of the Airbnb Open Data for New York City using the Pandas library in Python. The primary goal is to transform the raw, messy dataset into a clean, structured, and reliable format that is suitable for exploratory data analysis (EDA), visualization, and building machine learning models.

The entire process is documented in the `Data_Cleaning_Handson.ipynb` Jupyter Notebook.

## Dataset

  * **Source:** `Airbnb_Open_Data.csv`
  * **Description:** This dataset contains listing information for Airbnb properties, including details about the host, location, price, reviews, and availability.

## Project Workflow & Cleaning Steps

The data cleaning process was systematically performed in the following stages:

1.  **Initial Data Assessment**

      * Loaded the dataset into a Pandas DataFrame.
      * Performed an initial investigation using `info()`, `describe()`, `shape`, and `head()` to understand its structure, data types, and identify preliminary issues like null values and incorrect data formats.

2.  **Data Type Correction (Type Casting)**

      * The `price` and `service fee` columns were identified as `object` type due to the presence of '$' symbols. These were removed, and the columns were converted to a numeric (`float64`) data type.
      * The `last review` column was converted from `object` to the `datetime` format to enable proper time-series analysis.

3.  **Handling Missing Values**

      * The `license` column was dropped entirely as it contained approximately 99.9% missing values and was not informative.
      * Missing values in `reviews per month` were filled with `0`, assuming that no data implies zero reviews for that month.
      * Null entries in `last review` and `house_rules` were replaced with descriptive strings ('No Review' and 'Not Given', respectively).
      * After targeted imputation, the `dropna()` method was used to remove any remaining rows with null values, ensuring a complete dataset.

4.  **Standardizing Column Names**

      * Column names were standardized to a consistent `snake_case` format for better readability and easier access (e.g., 'host name' was changed to `host_name`).

5.  **Removing Duplicates**

      * The dataset was checked for duplicate records.
      * A total of 523 duplicate rows were identified and removed to ensure data integrity.

## Final Outcome

After completing all the cleaning steps, the dataset is now robust, consistent, and ready for further analysis. This clean dataset can be reliably used for feature engineering, data visualization, and as an input for predictive modeling tasks.

## Tools and Libraries Used

  * **Python**
  * **Pandas**
  * **Jupyter Notebook**

## How to Use

1.  Clone this repository to your local machine.
2.  Make sure you have Python and Jupyter Notebook installed.
3.  Install the required library:
    ```bash
    pip install pandas
    ```
4.  Place the `Airbnb_Open_Data.csv` file in the same directory as the notebook.
5.  Open and run the `Data_Cleaning_Handson.ipynb` notebook to see the step-by-step cleaning process.

-----

## Author

  * **Naveen Kumar K**

### Connect with Me 

  * **LinkedIn:** [linkedin.com/in/naveen840/](https://www.linkedin.com/in/naveen840/)
  * **GitHub:** [github.com/NaveenKumar1822](https://github.com/NaveenKumar1822)
