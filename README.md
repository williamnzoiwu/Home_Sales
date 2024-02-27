# Home_Sales
## Big Data Module 22 Challenge.
This script contains an iPython notebook utilizing Spark to visualize home sales data.

The code first imports the PySpark SQL functions and uses Spark to read a csv file containing home sales data. It then creates a temporary table view of the dataframe called home_sales. It then uses Spark SQL to display the following information from the table:

The average price for a four-bedroom house sold for each year.

The average price of a home for each year the home was built, that has three bedrooms and three bathrooms.

The average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet.

The average price of a home per "view" rating having an average home price greater than or equal to $350,000, also displaying the runtime for this query.

After the previous data is retrieved, the temporary table home_sales is cached. Next, using the cached data, the last query is ran again, once again displaying the runtime to compare it to the uncached runtime. The code then partitions by the "date_built" field on the formatted parquet home sales data and creates a temporary table for the parquet data. The last query is then ran one more time using the parquet table to compare the runtime to the cached runtime. Lastly, the home_sales temporary table is uncached.
