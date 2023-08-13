# PySpark_HomeSales
**SparkSQL Home Sales Analysis**

**1. Introduction**

The purpose was to outlines the analysis performed on the "home_sales_revised.csv" dataset using Apache Spark's SparkSQL. The primary goal of the analysis is to gain insights into various aspects of home sales data, such as average prices, view ratings, and query runtimes.

**2. Setup and Data Loading**

- The necessary PySpark SQL functions were imported to facilitate data manipulation and analysis.
- The provided "home_sales_revised.csv" dataset was read into a Spark DataFrame.
- A temporary table named "home_sales" was created to enable SparkSQL queries on the data.

**3. Analysis and Results**

*Question 1: Average Price of Four-Bedroom Houses by Year*
The query calculates the average price for a four-bedroom house sold each year and rounds the answer to two decimal places.

*Question 2: Average Price of Homes by Year Built (3 bedrooms, 3 bathrooms)*
The query calculates the average price of homes based on the year they were built, considering homes with three bedrooms and three bathrooms. The result is rounded to two decimal places.

*Question 3: Average Price of Homes by Year (3 bedrooms, 3 bathrooms, 2 floors, >= 2,000 sqft)*
The query calculates the average price of homes based on the year they were built, considering homes with three bedrooms, three bathrooms, two floors, and a minimum area of 2,000 square feet. The result is rounded to two decimal places.

*Question 4: View Ratings for Homes >= $350,000*
The query determines the "view" rating for homes with a cost of $350,000 or more. The runtime for this query was measured and rounded to two decimal places.

*Query Caching*
The "home_sales" temporary table was cached for improved query performance.

*Cached Query*
Using the cached data, a query was executed to filter view ratings with an average price greater than or equal to $350,000. The runtime of the query was measured and compared with the uncached runtime.

*Partitioning and Parquet Table*
The data was partitioned by the "date_built" field and stored in a formatted Parquet table. A temporary table for the Parquet data was created.

*Parquet Query*
A query was executed on the Parquet data to filter view ratings with an average price greater than or equal to $350,000. The runtime was measured and compared to the uncached runtime.

**4. Query Runtimes**

The runtimes for the specified queries were measured and rounded to two decimal places. The comparison between cached and uncached runtimes was also provided where applicable.

**5. Query Uncaching**

The "home_sales" temporary table was uncached to release memory resources.

**6. Conclusion**

In conclusion, this demonstrates the analysis of home sales data using SparkSQL. The average prices of homes were examined based on various criteria, and query runtimes were compared between cached and uncached scenarios. The insights gained from this analysis provide valuable information for understanding the trends and characteristics of home sales.

For any further analysis or detailed insights, additional queries and exploration can be performed on the dataset.
