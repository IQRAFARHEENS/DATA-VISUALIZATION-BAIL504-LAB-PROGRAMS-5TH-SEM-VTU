Program 6: Power BI Data Transformation and Visualization
Power Query Editor, Data Cleaning, Top 10 States by Total Sales & Total Sales by Category
📌 Aim
To perform data transformation using Power Query Editor and create interactive visualizations in Power BI Desktop, including a map showing the Top 10 States by Total Sales and a column chart showing Total Sales by Category.
📚 Program Overview
This program demonstrates:
- Importing an Excel dataset into Power BI Desktop
- Opening Power Query Editor
- Checking the Orders table and its fields
- Removing the unnecessary Product Name column
- Removing bottom rows
- Renaming Sales to Total Sales
- Applying transformations using Close & Apply
- Enabling Map and Filled Map visuals
- Creating a map showing the Top 10 States by Total Sales
- Applying a Top N filter
- Adding Total Sales to Bubble size and Tooltips
- Creating a clustered column chart for Total Sales by Category
- Arranging and verifying report visuals
- Saving the report as a .pbix file
🎥 Screen Recording & Materials
The screen recording and supporting materials can be accessed through the Google Drive folder.

👉 View Screen Recording & Materials
🗂️ Dataset Used
Dataset: Excel workbook containing the Orders table.

The dataset includes sales, product, customer, order, and geographical information used to create the report.
Important Fields
Field	Description
Category	Product category
Sub-Category	Product sub-category
Sales / Total Sales	Sales value used for analysis
Quantity	Quantity of products
Discount	Discount value
Profit	Profit value
City	City associated with an order
State	State used for the map
Country	Country associated with an order
Region	Geographical region
Customer information	Information about customers
Order information	Information about orders
Product information	Information about products


🔌 1. Import the Data
Step 1 — Open Power BI Desktop
1. Open Power BI Desktop.
2. From the Home tab, click Get Data.
3. Select Excel workbook.
4. Browse to your dataset.
5. Select the required Excel file.
6. Click Open.
🔄 2. Open Power Query Editor
Step 2 — Open Power Query Editor
After selecting the Excel file:
1. Select the required table/sheet.
2. Click Transform Data.
This opens Power Query Editor.

Power Query is used to clean and transform the dataset before creating visualizations.
📋 3. Check the Orders Table
Step 3 — Check the Orders table
On the left side, make sure the query is:

Orders

The data contains fields such as:
- Category
- Sub-Category
- Sales
- Quantity
- Discount
- Profit
- City
- State
- Country
- Region
- Customer information
- Order information
- Product information
🧹 4. Remove the Unnecessary Column
Step 4 — Remove Product Name
The Product Name column is not required for this program.
1. Locate Product Name.
2. Right-click the column.
3. Select Remove.
Alternatively, use:

Home → Remove Columns

After this, you should see an applied step called:

Removed Columns

The formula bar will show something similar to:
Table.RemoveColumns(...)
✂️ 5. Remove Bottom Rows
Step 5 — Remove Bottom Rows
Now remove the unwanted rows from the bottom of the dataset.
1. Go to the Home tab.
2. Click Remove Rows.
3. Select Remove Bottom Rows.
4. A dialog box called Remove Bottom Rows appears.
5. Enter the number of rows specified by your lab instructions.
6. Click OK.
Power Query will create an applied step:

Removed Bottom Rows
Note: Use the number of rows specified in your Program 6 lab instructions.

✏️ 6. Rename Sales to Total Sales
Step 6 — Rename Sales to Total Sales
Your original column is:

Sales

Rename it to:

Total Sales

Steps:
1. Find the Sales column.
2. Right-click it.
3. Select Rename.
4. Enter:
Total Sales
5. Press Enter.
You should now see Total Sales instead of Sales.

Power Query creates the applied step:

Renamed Columns
✅ 7. Apply the Transformations
Step 7 — Close Power Query
Once all transformations are complete:
1. Click Home.
2. Click Close & Apply.
Power BI will load the transformed data into the report.

Wait for the data to finish loading.
⚙️ 8. Enable Map Visuals
Because Power BI initially showed the message:
"Map and filled map visuals are disabled."

the visuals were enabled through Power BI settings.

If this has already been done, you do not need to repeat it.

For reference:
1. Go to File.
2. Select Options and settings.
3. Click Options.
4. Select Security under Global settings.
5. Find Map and Filled Map visuals.
6. Enable Use Map and Filled Map visuals.
7. Click OK.
If Power BI asks you to restart, restart Power BI Desktop.
🗺️ 9. Create the Top 10 States Map
Step 8 — Create a Map Visual
Go to the Report view.
1. Click an empty area of the report canvas.
2. In the Visualizations pane, select the Map visual.
A blank map appears.
Step 9 — Add State to Location
From the Data pane:
1. Find the State field.
2. Drag State into Location.
Power BI will identify the states geographically. Your map will begin displaying state locations.
🔎 10. Create the Top 10 Filter
Step 10 — Add State Filter
Select the map.

In the Filters pane:
1. Under Filters on this visual, locate State.
2. Change the Filter type to Top N.
Step 11 — Set Top 10
Under Show items:
- Select Top
- Enter 10
So it becomes:

Top 10
Step 12 — Filter by Total Sales
Under By value:
1. Drag Total Sales into the field.
2. Make sure it appears as Sum of Total Sales.
Your filter should now essentially read:

Top 10 States by Sum of Total Sales

Click Apply filter if the button is available.

The map should now show only the top 10 states according to total sales.
🔵 11. Add Total Sales to Bubble Size
Step 13 — Add Total Sales to Bubble Size
With the map selected:
1. Find Bubble size in the Visualizations pane.
2. Drag Total Sales into Bubble size.
3. Make sure it shows Sum of Total Sales.
Now the bubble size represents the amount of sales.
- Larger bubble → higher total sales
- Smaller bubble → lower total sales
💬 12. Add Total Sales to Tooltips
Step 14 — Add Tooltip
Still with the map selected:
1. Find Tooltips.
2. Drag Total Sales into Tooltips.
3. It should appear as Sum of Total Sales.
Now when you hover over a state, Power BI can display the sales value.
🏷️ 13. Format the Map Title
Step 15 — Give the Map a Title
Select the map.

Go to:

Format visual → General → Title
1. Turn Title ON.
2. Set the title to:
Top 10 States by Total Sales

Your map should now have:
- State → Location
- Total Sales → Bubble size
- Total Sales → Tooltips
- Top N = 10
- Top N based on Sum of Total Sales
📊 14. Create Total Sales by Category
Step 16 — Insert a Column Chart
Click an empty area beside the map.

From Visualizations, select:

Clustered column chart

This creates the second visual.
Step 17 — Add Category to X-axis
From the Data pane:
1. Find Category.
2. Drag it into X-axis.
The categories should appear:
- Technology
- Furniture
- Office Supplies
Step 18 — Add Total Sales to Y-axis
From the Data pane:
1. Find Total Sales.
2. Drag it into Y-axis.
Power BI should automatically use:

Sum of Total Sales

You should now see three columns representing the total sales for each category.
📝 15. Format the Column Chart
Step 19 — Add Chart Title
Select the column chart.

Go to:

Format visual → General → Title
1. Turn the title On.
2. Enter:
Total Sales by Category

Your final chart should clearly show Technology | Furniture | Office Supplies with their corresponding total sales.
🖥️ 16. Arrange the Final Report
Step 20 — Arrange Both Visuals
Place the two visuals side by side.

Left side
- Top 10 States by Total Sales
- Map
Right side
- Total Sales by Category
- Column chart
Your final report should look approximately like this:
┌───────────────────────────┬──────────────────────────────┐
│ Top 10 States by          │ Total Sales by Category      │
│ Total Sales               │                              │
│                           │       █                     │
│        Map                │       █     █               │
│     with different-       │       █     █     █         │
│     size bubbles          │     Technology              │
│                           │     Furniture               │
│                           │     Office Supplies         │
└───────────────────────────┴──────────────────────────────┘
✔️ 17. Verify the Map
Before considering the program complete, check the map.
Requirement	Status
State in Location	✅
Top N filter	✅
Top N = 10	✅
By value = Sum of Total Sales	✅
Total Sales in Bubble size	✅
Total Sales in Tooltips	✅
Map title	✅


✔️ 18. Verify the Column Chart
Check the second visual.
Requirement	Status
Clustered column chart	✅
Category on X-axis	✅
Total Sales on Y-axis	✅
Aggregation = Sum	✅
Three categories visible	✅
Chart title	✅


💾 19. Save the Power BI File
Step 21 — Save the Report
Go to:

File → Save As

Save the file as a Power BI file:
Program-06.pbix
Or use the filename required by your lab.

Make sure the .pbix extension is present.
📸 20. Screenshots
The following screenshots can be included to document the major stages of the program:
screenshots/
├── 01-import-dataset.png
├── 02-power-query-editor.png
├── 03-remove-product-name.png
├── 04-remove-bottom-rows.png
├── 05-rename-sales-total-sales.png
├── 06-map-top-10-states.png
├── 07-top-n-filter.png
├── 08-map-bubble-size-tooltips.png
├── 09-total-sales-by-category.png
└── 10-final-report.png
📁 Repository Structure
The Program 6 folder can be organized as follows:
Program-06-Power-BI-Data-Transformation-and-Visualization/
│
├── README.md
├── Program-06.pbix
├── Orders.xlsx
└── screenshots/
    ├── 01-import-dataset.png
    ├── 02-power-query-editor.png
    ├── 03-remove-product-name.png
    ├── 04-remove-bottom-rows.png
    ├── 05-rename-sales-total-sales.png
    ├── 06-map-top-10-states.png
    ├── 07-top-n-filter.png
    ├── 08-map-bubble-size-tooltips.png
    ├── 09-total-sales-by-category.png
    └── 10-final-report.png
Use your actual dataset filename in place of Orders.xlsx if it is different.
🎯 Learning Outcomes
After completing this program, the learner should be able to:
- Import Excel data into Power BI Desktop
- Use Power Query Editor to transform data
- Remove unnecessary columns and bottom rows
- Rename columns
- Apply transformations using Close & Apply
- Enable map visuals
- Create a geographical map
- Apply a Top N filter
- Use sales values to control bubble size and tooltips
- Create a clustered column chart
- Arrange multiple visuals in a report
- Verify and save a Power BI report
✅ Result
After completing the program, the Power BI report contains two visualizations:
1. Top 10 States by Total Sales
A geographical map displaying the top 10 states based on Sum of Total Sales, with bubble size representing total sales and tooltips displaying sales information.
2. Total Sales by Category
A clustered column chart comparing Sum of Total Sales across:
- Technology
- Furniture
- Office Supplies
The report was arranged with the map on the left and the column chart on the right, and saved as Program-06.pbix.
🏁 Conclusion
This program provided practical experience in transforming data using Power Query Editor and creating visualizations in Power BI Desktop. It demonstrated how to remove unnecessary data, rename fields, apply transformations, create a Top 10 States map, compare sales by category, and organize multiple visuals into a clear report.
👩‍💻 Author
Iqra Farheen
