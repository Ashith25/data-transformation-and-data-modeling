# data-transformation-and-data-modeling
## Import Data:
 1) Import “List of Orders.csv” into Power BI.

* created a blank report in power bi - home-get data- text /csv -select list of  order -load .
   
2) Open “List of Orders” in Power Query Editor by clicking on ‘Transform’.
 * select data (list of orders) in power Bi - tranform data
      
3) Import “order Details.csv” and “Sales target.csv” into Power Query Editor.
  * Home new source-text/csv- select file ( order details )-ok
  *  Home new source-text/csv- select file ( sales target )-ok
## Data Transformation:
1) Restrict the "List of Orders" table to only the first 500 rows.
  * Select data in home tab select keep rows under reduce row and select keep top rows give the commend first 500 rows then click ok.
2) Ensure the “Order Date” column in the “List of Orders” table is set to data type 'Date'.
 * Set order date column data type to ' date'.
3) Change the data type of “Amount” and “Target” columns to ‘Fixed Decimal Number’.
 * Set data type amount and target colums to 'fixed decimal' by using filter.
4) Format	the	"CustomerName"	column	into	proper	case,	ensuring consistent capitalization for each word.
* Transform - formate - capitalised each word.
5) Merge the "State" and "City" columns to create a new column named "Location" in the format ‘City, State’.
* Rearranged the state and city column to city and state and created a new column named 'loaction' by mearging the city and state column.
6) Create a new custom column named "Profit Margin" as the percentage of "Profit" divided by "Amount".
* Created a column "profit margin" by the use of custom column and provided the formula 'Profit / Amount'.
7) Add a new conditional column named "Profit Status" based on the values in the "Profit" column. The conditions are as follows: if the profit is less than 0, the label should be "Loss"; if the profit equals 0, the label should be "Break-Even"; and if the profit is greater than 0, the label should be "Profit".
* Created a new column named 'profit status' by the use of conditional column , "syntex =if (profit) < 0 then loss ,else if (profit) < = 0 Break-even, else 0".
## Merging Data (Joins):
1) Merge the "List of Orders" and "Order Details" tables into a new single table named "Orders Data" based on the "Order ID" relationship.
* Merged the "List of Orders" and "Order Details" tables into a new single table named "Orders Data" based on the "Order ID" relationship Home – Merge Queries – Merge Queries as New.
 ## Handling Missing Data & Duplicate Data:
1) Identify missing values in the data and determine a strategy to address them.

   a) Check for duplicate rows and define a strategy to handle duplicates.
* Duplicate rows was removed by right clicking the order id column and selecting the remove duplicate option.
 ## Sorting and Filtering Data:
1) In the ‘Orders Data’ table, utilize sorting and filtering techniques on columns like Order Date, State or Category to analyze data based on specific criteria:
   
a) Sort the orders by Order Date in descending order to analyze recent trends.
 * Sorted the ordr date in descinding order by using the filter option  and sorting it in descinding order.
   
b) Filter the orders to focus only on a specific state (e.g., Tamil Nadu) for regional analysis.
 * Filtered the data to give out specif state by using the filter option and selecting only the ' Tamil Nadu' state data. 
 ## Grouping and Aggregating Data:
1) Duplicate the “Order Details” table and calculate the count of each Order ID, average profit by Category or total amount by Sub-Category.
   
* Duplicate “ Order details” table – Group by Order ID – Operation given as count rows – Ok Duplicate “Order details” table - Group by Sub category – Operation given as Sum and Column given as amount – ok

2) Duplicate the “Sales Target” table and aggregate the total target amount by Month of Order Date.

* Duplicate “Sale target” table – Group by – Month of order date – operation given as sum - and column given as “Target”.
## Data Modeling:
1) Establish a relationship between the “List of Orders” and “Order Details” tables using the ‘Order ID’ column.
* In power Bi loading page go to options and setting - options- current file - data load - unselect the autodetect option and press ok . Then in 'manage relationship' option select the tables and select order id as common item and provide cardinality as 'many to one'.
  
2) Build a relationship between the “Order Details” and “Sales Target” tables based on the ‘Category’ column. Click "Manage relationships" and ensure this relationship is active.
* To ensure the relationship go to 'manage relationship' option and delet
the excisting deletials and add new relation by selecting the 'order detials'and 'sales Target' data and select catagory column as common.
