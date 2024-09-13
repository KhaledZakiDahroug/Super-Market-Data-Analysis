# Super Market Sales Project


## Table of Contents
1. [Introduction](#introduction)
2. [Column Descriptions](#column-descriptions)
3. [Data Analysis](#data-analysis)
4. [Insights](#insights)
5. [Conclusion](#conclusion)

## Introduction
This dataset contains sales transaction data from a supermarket chain with branches in three major cities: Yangon, Naypyitaw, and Mandalay. The dataset includes information on customer demographics, purchase details, payment methods, and customer satisfaction ratings. Key aspects such as product lines, unit prices, quantities, and total purchase amounts (including tax) are also captured, providing a comprehensive view of sales and customer behavior.

## Column Descriptions

1. **Invoice ID**  
   A unique identifier for each transaction or purchase.

2. **Branch**  
   Indicates the branch location of the supermarket (e.g., Yangon, Naypyitaw, Mandalay).

3. **Yangon, Naypyitaw, Mandalay**  
   These columns may contain geographical or branch-specific data, though further inspection is needed to clarify their exact role.

4. **Customer type**  
   Describes the type of customer (e.g., Member or Normal).

5. **Gender**  
   Gender of the customer (Male or Female).

6. **Product line**  
   The category or type of product purchased (e.g., Health and beauty, Electronics).

7. **Unit price**  
   The price of a single unit of the product.

8. **Quantity**  
   The number of units purchased in the transaction.

9. **Tax 5%**  
   The tax amount applied to the total purchase (calculated as 5%).

10. **Total**  
    The total amount of the purchase, including tax.

11. **Date**  
    The date of the transaction.

12. **Time**  
    The time the transaction took place.

13. **Payment**  
    The payment method used (e.g., Cash, Credit card, E-wallet).

14. **Rating**  
    The customer satisfaction rating, typically on a scale from 1 to 10.
    

# Data Analysis

## Data Wrangling

1. **Loading the Dataset**  
   - The dataset was loaded into a pandas DataFrame for easy manipulation.

2. **Handling Missing Values**  
   - Checked for missing or null values in columns such as `Branch`, `Gender`, `Product line`, etc. If any missing data were found, they were either imputed (e.g., with mean values for numeric columns or mode for categorical columns) or removed.

3. **Correcting Data Types**  
   - Ensured that data types for each column were appropriate, such as converting `Date` and `Time` to `datetime` objects for easier manipulation and calculations.

4. **Removing Duplicates**  
   - Any duplicate records, if found, were removed to ensure each transaction was unique.

5. **Tax and Total Calculation Check**  
   - Verified that the `Tax 5%` column correctly reflected 5% of the purchase `Total` and fixed any discrepancies in these calculations if needed.

6. **Outlier Detection**  
   - Identified and handled potential outliers in columns like `Unit price`, `Quantity`, and `Rating` that could skew analysis results.

7. **Standardizing Categorical Data**  
   - Ensured consistency in categorical columns such as  `Customer type` by correcting any inconsistencies or misspellings.

8. **Datetime Feature Engineering**  
   - Extracted useful features from the `Date` and `Time` columns, such as day of the week or time of day, for deeper analysis of sales patterns.





## Insights

1. *% Customer Type*:
   - *Description*: This chart shows the distribution of customer types, comparing the percentage of normal customers versus members. It helps identify the proportion of different customer categories.

 <p align="center">
  <img src="powerBi/customer_type.png" alt="% Customer by Type"/>
</p>

2. *% Customer by Gender*:
   - *Description*: This visual displays the percentage of customers by gender, highlighting the ratio of male to female customers. It provides insights into the gender demographics of the customer base.


<p align="center">
  <img src="powerBi/customer_gender.png" alt="% Customer by Gender"/>
</p>


3. *% Customer by Shift Type*:
   - *Description*: This chart illustrates the preference of customers for different shift types (first or second shift). It shows which shift is more popular among customers for their purchases.


<p align="center">
  <img src="powerBi/customer_shift.png" alt="% Customer by shift"/>
</p>


4. *Preferred Payment Methods for Customers*:
   - *Description*: This chart compares different payment methods and shows which method is preferred by customers. The stacked format reveals preferences segmented by customer type.


<p align="center">
  <img src="powerBi/payment_method.png" alt="% Payment_Method"/>
</p>


5. *Distribution of Customer by Cities*:
   - *Description*: This visual breaks down the number of customers by city and customer type (normal or member). It helps understand customer distribution across various cities.


<p align="center">
  <img src="powerBi/customer_by_city.png" alt=" Dist_by_Citites"/>
</p>


6. *Distribution of Product Line by Customers*:
   - *Description*: This tree map categorizes product lines and shows the number of invoices for each product line. It highlights which product lines are most popular based on customer purchases.


<p align="center">
  <img src="powerBi/customer_by_city.png" alt=" Dist_by_Citites"/>
</p>


7. *Peak and Low Selling Hours by Product Line*:
   - *Description*: This table lists each product line along with its peak and low selling hours. It identifies the times of day when products are sold the most and least.


<p align="center">
  <img src="powerBi/peak_selling_hours.png" alt="Peak_Hours"/>
</p>


8. *Rating for Products*:
   - *Description*: This chart displays the count of products based on their rating categories (Good, Fair, Excellent, Very Good). It provides an overview of product ratings and their distribution.


<p align="center">
  <img src="powerBi/rating_of_products.png" alt="Rating_Of_Prouct"/>
</p>


9. *Distribution of Products by Quantity Sold*:
   - *Description*: This visual compares the total quantity sold for each product line. It shows which product lines have higher or lower sales volumes.


<p align="center">
  <img src="powerBi/dist_product_by_qty.png" alt=" Dist_Product_By_QtySold"/>
</p>


10. *% Sales for Each City*:
    - *Description*: This chart represents the percentage of total sales generated by each city. It provides insights into the sales contribution of different cities.


<p align="center">
  <img src="powerBi/sale_for_each_city.png" alt=" Sales_for_Each_City"/>
</p>


11. *Distribution of Sales by Product Line Across Shift Types*:
    - *Description*: This chart compares sales performance for different product lines across various shifts. It shows which product lines achieve higher sales during each shift type.


<p align="center">
  <img src="powerBi/product_line_across_shift.png" alt="Dist_Product_Across_Shift_Type"/>
</p>


12. *Average Sales by Hour (10 AM - 9 PM)*:
    - *Description*: This line chart tracks average sales throughout the day from 10 AM to 9 PM. It provides a view of sales trends by hour.


<p align="center">
  <img src="powerBi/avg_sales_by_hour.png" alt="Avg_Sales_Per_Hour"/>
</p>


13. *Average Sales Comparison: Weekends vs Weekdays*:
    - *Description*: This chart compares average sales on weekends versus weekdays. It helps assess the impact of day type on sales performance.


<p align="center">
  <img src="powerBi/sales_comparison.png" alt=" WeekDay_VS_WeekEnd"/>
</p>


14. *Sales Trend Over 3 Months*:
    - *Description*: This line chart illustrates the sales trend over the past three months. It provides insights into how sales have fluctuated month by month.


<p align="center">
  <img src="powerBi/total_sales_over_3_months.png" alt=" Sales_Over_3_Months"/>
</p>


15. *Sales Distribution by Days of Week*:
    - *Description*: This chart shows sales distribution across different days of the week. It helps identify which days generate higher or lower sales.


<p align="center">
  <img src="powerBi/sales_dist_by_days_of_week.png" alt=" Sales_By_Day"/>
</p>

## Conclusion

