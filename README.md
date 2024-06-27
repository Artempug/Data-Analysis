# Data-Analysis
Outlier detection.

The lab session focused on handling and analyzing a dataset using Python, with a particular emphasis on data cleaning, statistical analysis, and visualization. Here’s a breakdown of the steps and key learnings:

Loading and Exploring Data
Importing Libraries:

The lab made use of essential libraries such as pandas for data manipulation, numpy for numerical operations, matplotlib.pyplot and seaborn for data visualization, and sklearn.ensemble.IsolationForest for anomaly detection.
Reading the Dataset:

The dataset was loaded from a CSV file named store.csv using pandas.read_csv(). The initial loading process encountered a DtypeWarning indicating mixed data types in one of the columns, suggesting the need for specifying data types or setting low_memory=False.
Data Inspection:

The dataset contained 80,475 rows and 8 columns, including details like DEALS_CARD_CODE, Month, TotalSpent, AvgCheck, VisitsPerMonth, UniqueProductsPerMonth, and UniqueCategoriesPerMonth.
An initial data inspection using df.info() revealed that the TotalSpent column was incorrectly read as an object due to the presence of non-numeric values.
Data Cleaning and Transformation
Handling Data Types:

An attempt was made to convert the TotalSpent column to a numeric type, which resulted in a ValueError because of invalid entries (e.g., 'f'). This required further cleaning to ensure consistent data types.
Data Conversion:

After cleaning, the TotalSpent column was successfully converted to float64, with one missing value identified.
Descriptive Statistics:

Descriptive statistics provided insights into the data distribution, including means, standard deviations, and min/max values for the numeric columns.
Data Visualization and Outlier Detection
Visualization:

A strip plot of TotalSpent using seaborn highlighted the data distribution, revealing potential outliers.
A boxplot further visualized the spread and outliers in TotalSpent.
Outlier Detection:

The Interquartile Range (IQR) method was employed to identify outliers in the TotalSpent column. Outliers outside the lower and upper bounds were replaced with the median value of TotalSpent.
A custom Hempel filter function was introduced to handle outliers based on Median Absolute Deviation (MAD), marking extreme values as NaNs.
Data Analysis
Final Data Inspection:
The cleaned dataset, with outliers handled, contained 80,475 entries with 65,965 non-null entries for TotalSpent, indicating the removal or modification of outliers.
Overall, this lab provided a comprehensive overview of data handling techniques, including reading, cleaning, visualizing, and analyzing a real-world dataset to ensure data integrity and prepare it for further analysis.
