# BDAT1002
# Brewery Data Analysis Project
BDAT 1002 - Group Assignment Documentation and Code

## Overview

This repository contains the code and analysis for the Brewery Data Analysis project, covering data extraction, preliminary analysis in Hive, and more detailed processing and analysis using PySpark.

## 1. Data Extraction and Initial Analysis

The dataset was obtained from [Brewery Operations and Market Analysis Dataset](https://www.kaggle.com/) and extracted using wget and unzip commands on the VM machine. It was then imported into a Hive database for preliminary analysis.

## 2. Preliminary Hive Query

A Hive query was executed to perform initial testing and data checking:

```sql
SELECT Beer_Style, SKU, SUM(Total_Sales) AS Total_Sales
FROM brewery_data
GROUP BY Beer_Style, SKU
ORDER BY Total_Sales DESC
LIMIT 10;
```

## 3. Data Processing and Analysis with PySpark

### 3.1 Counting Rows

A Spark operation was performed to count rows, ensuring data availability and checking for potential errors.

### 3.2 Distribution of Losses

A complex Spark query was executed to visualize the distribution of losses across batches and styles.

## 4. Data Transformation

A new column representing the ratio of total sales to volume was created, showcasing Spark's ability for data transformation.

## 5. Error Mitigation and Visualization Optimization

Challenges were encountered during data analysis, leading to the strategic decision to limit the dataset to the first 1000 rows for smoother demonstration. The analysis involved Spark and Pandas, with screenshots capturing errors and steps taken for mitigation.

## 6. Visualisation Results

Various visualizations were generated using Seaborn, showcasing insights into quality scores, fermentation time, bitterness distribution, and sales performance across different locations.

## Conclusion

The project involved a mix of Hive and PySpark, highlighting both challenges and solutions. Screenshots provide visual documentation of specific steps and errors encountered. The combination of local installation and subset sampling allowed for effective troubleshooting and visualization, demonstrating the power and flexibility of PySpark in handling large datasets.
