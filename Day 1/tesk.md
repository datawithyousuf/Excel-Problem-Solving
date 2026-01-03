# Day 01 – Sales Data Analysis

## Dataset
Sales transaction data containing:
- Date
- Product
- Category
- Quantity
- Sales Amount
- Region

---

Task 1: Calculate total sales revenue.
✅ Formula-Based Solution
Formula Used:
=SUM(Sales_Data!H2:H11)
Result Location:
•	File: formulas_solution.xlsx
•	Sheet: formula_work
________________________________________
📊 Pivot Table Method
Pivot Configuration:
•	Rows:None
•	Values: Sum of Sales Amount
•	Filter: None 
Result Location:
•	File: pivot_table_solution.xlsx
•	Sheet: pivot_table_work

________________________________________

Task 2: Find average sales amount per order.
✅ Formula-Based Solution
Formula Used:
=AVERAGE(Sales_Data!H2:H11)
Result Location:
•	File: formulas_solution.xlsx
•	Sheet: formula_work
________________________________________
📊 Pivot Table Method
Pivot Configuration:
•	Rows:None
•	Values: Average of Sales Amount
•	Filter: None 
Result Location:
•	File: pivot_table_solution.xlsx
•	Sheet: pivot_table_work

________________________________________

Task 3: Count total number of orders.
✅ Formula-Based Solution
Formula Used:
=COUNT(Sales_Data!A2:A11)
Result Location:
•	File: formulas_solution.xlsx
•	Sheet: formula_work
________________________________________
📊 Pivot Table Method
Pivot Configuration:
•	Rows:None
•	Values: Count of Order_ID
•	Filter: None 
Result Location:
•	File: pivot_table_solution.xlsx
•	Sheet: pivot_table_work

________________________________________

Task 4: Find total quantity sold per product.
✅ Formula-Based Solution
Formula Used:
I used a two-step formula approach:
1. **Extract unique product names** using the `UNIQUE` function.
   This creates a dynamic list of products without duplicates.
=UNIQUE(Sales_Data!D2:D11)
2.Calculate total quantity for each product using SUMIF.
This sums the Quantity column for each corresponding product.
=SUMIF(Sales_Data!D2:D11,formula_work!B20,Sales_Data!F2:F11)
Result Location:
•	File: formulas_solution.xlsx
•	Sheet: formula_work
________________________________________
📊 Pivot Table Method
Pivot Configuration:
•	Rows: Product
•	Values: Sum of Quality
•	Filter: None 
Result Location:
•	File: pivot_table_solution.xlsx
•	Sheet: pivot_table_work
________________________________________
Task 5: Identify the highest selling product by sales amount.
✅ Formula-Based Solution
Formula Used:
=XLOOKUP(MAX(Sales_Data!H2:H11),Sales_Data!H2:H11,Sales_Data!D2:D11)
Explanation:
•	MAX(Sales_Data!H2:H11) finds the highest sales amount in the dataset.
•	Sales_Data!H2:H11 is the lookup array containing sales values.
•	Sales_Data!D2:D11 is the return array that contains product names.
XLOOKUP matches the highest sales amount and returns the corresponding product name, identifying the highest selling product.

Result Location:
•	File: formulas_solution.xlsx
•	Sheet: formula_work
________________________________________
📊 Pivot Table Method
Pivot Configuration:
•	Rows: Product
•	Values: Max of Sales_Amount
•	Sort: Descending by Max of Sales_Amount
•	Filter: Top 1
Result Location:
•	File: pivot_table_solution.xlsx
•	Sheet: pivot_table_work

________________________________________

Task 6: Calculate total sales by category.
✅ Formula-Based Solution
Formula Used:
I used a two-step formula approach:
1. **Extract unique category names** using the `UNIQUE` function.
   This creates a dynamic list of category without duplicates.
=UNIQUE(Sales_Data!D2:D11)
2.Calculate Sales_Amount for each product using SUMIF.
This sums the Quantity column for each corresponding product.
=SUMIF(Sales_Data!E2:E11,formula_work!B41,Sales_Data!$H$2:$H$11)
Result Location:
•	File: formulas_solution.xlsx
•	Sheet: formula_work
________________________________________
📊 Pivot Table Method
Pivot Configuration:
•	Rows: Category
•	Values: Sumif of Sales_Amount
•	Filter: None 
Result Location:
•	File: pivot_table_solution.xlsx
•	Sheet: pivot_table_work

________________________________________
Task 7: Find total sales by region.
✅ Formula-Based Solution
Formula Used:
I used a two-step formula approach:
1. **Extract unique Region names** using the `UNIQUE` function.
   This creates a dynamic list of region without duplicates.
=UNIQUE(Sales_Data!I2:I11)
2.Calculate Sales_Amount for each region using SUMIF.
This sums the Quantity column for each corresponding product.
=SUMIF(Sales_Data!I2:I11,formula_work!B47,Sales_Data!H2:H11)
Result Location:
•	File: formulas_solution.xlsx
•	Sheet: formula_work
________________________________________
📊 Pivot Table Method
Pivot Configuration:
•	Rows: Region
•	Values: Sumif of Sales_Amount
•	Filter: None 
Result Location:
•	File: pivot_table_solution.xlsx
•	Sheet: pivot_table_work
________________________________________
Task 8: Identify the order with the highest sales amount.
✅ Formula-Based Solution
Formula Used:
=XLOOKUP(MAX(Sales_Data!A2:A11),Sales_Data!A2:A11,Sales_Data!A2:I11)
Result Location:
•	File: formulas_solution.xlsx
•	Sheet: formula_work
________________________________________
📊 Pivot Table Method
Pivot Configuration:
•	Rows: Order_ID
•	Values: SUM of Sales_Amount
•	Sort: Sort Largest To Smallest
•	Filter: Top 1
Result Location:
•	File: pivot_table_solution.xlsx
•	Sheet: pivot_table_work
________________________________________
Task 9: Calculate average unit price per category.
✅ Formula-Based Solution
Formula Used:
I used a two-step formula approach:
1. **Extract unique Category names** using the `UNIQUE` function.
   This creates a dynamic list of catagory without duplicates.
=UNIQUE(Sales_Data!E2:E11)
2.Calculate Average Unit Price for each region using A	VERAGEIF.
This average the Unite_Price column for each corresponding category.
=AVERAGEIF(Sales_Data!E2:E11,formula_work!B59,Sales_Data!$G$2:$G$11)
Result Location:
•	File: formulas_solution.xlsx
•	Sheet: formula_work
________________________________________
📊 Pivot Table Method
Pivot Configuration:
•	Rows: Category
•	Values: Average of Unit_Price
•	Sort: None
•	Filter: None
Result Location:
•	File: pivot_table_solution.xlsx
•	Sheet: pivot_table_work
________________________________________
Task 10: Create a summary table showing:
     - Product
     - Total Quantity
    - Total Sales

✅ Formula-Based Solution
Formula Used:
I used a Thre-step formula approach:
1. **Generate unique product list**
    =UNIQUE(Sales_Data!D2:D11)
This extracts all distinct product names and ensures the summary updates automatically when new data is added.
2. Calculate total quantity sold per product
   =SUMIF(Sales_Data!D2:D11, A2, Sales_Data!F2:F11)
This sums the Quantity column for each product.
3. Calculate total sales per product
  =SUMIF(Sales_Data!D2:D11, A2, Sales_Data!H2:H11)
This sums the Sales Amount for each product.
Result Location:
•	File: formulas_solution.xlsx
•	Sheet: formula_work
________________________________________
📊 Pivot Table Method
Pivot Configuration:
•	Rows: Product
•	Values: Total Quality, Total Sales
•	Sort: None
•	Filter: None
Result Location:
•	File: pivot_table_solution.xlsx
•	Sheet: pivot_table_work
 	________________________________________

