# Program 6: Power BI Data Transformation and Visualization

**Tools Used:** Power BI Desktop, Power Query Editor

## 📌 Aim

To perform data transformation using Power Query Editor and create interactive visualizations in Power BI Desktop, including a map showing the Top 10 States by Total Sales and a column chart showing Total Sales by Category.

## 📊 Program Overview

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
- Saving the report as a Power BI file (`.pbix`)

## 🛠️ Software Requirements

- Power BI Desktop
- Microsoft Excel dataset
- Windows operating system

## 📂 Dataset

The program uses an Excel dataset containing order information.

**Expected table:** `Orders`

The dataset includes fields used for the analysis, such as State, Category, Sales, and Product Name.

> Note: Use the actual dataset filename supplied for your lab. The dataset must contain the required columns for the steps below.

## 📝 Procedure

### Step 1: Import the Excel Dataset

1. Open Power BI Desktop.
2. Select **Get Data** from the Home ribbon.
3. Choose **Excel Workbook**.
4. Browse to the Excel dataset and select it.
5. In the Navigator window, select the `Orders` table or worksheet.
6. Click **Transform Data** to open Power Query Editor.

### Step 2: Open Power Query Editor

1. Verify that the `Orders` table is displayed.
2. Examine the available columns and their data.
3. Identify the columns required for the report.
4. Confirm that fields such as State, Category, and Sales are available.

### Step 3: Remove the Product Name Column

1. Locate the **Product Name** column.
2. Select the column.
3. Right-click and choose **Remove**, or use the Remove Columns option on the ribbon.
4. Verify that the Product Name column has been removed.

### Step 4: Remove Bottom Rows

1. Open the **Home** tab in Power Query Editor.
2. Select **Remove Rows**.
3. Choose **Remove Bottom Rows**.
4. Enter the number of rows specified in your lab instructions.
5. Click **OK** and verify the resulting data.

### Step 5: Rename Sales to Total Sales

1. Locate the **Sales** column.
2. Double-click the column heading or right-click and select **Rename**.
3. Change the column name to `Total Sales`.
4. Press **Enter** to apply the change.

### Step 6: Apply the Transformations

1. Review the changes made in Power Query Editor.
2. Confirm that the unwanted column has been removed.
3. Verify the removal of bottom rows.
4. Check that the Sales column is now named Total Sales.
5. Click **Close & Apply**.
6. Wait for Power BI Desktop to load the transformed data.

### Step 7: Enable Map Visuals

1. Open Power BI Desktop.
2. Navigate to **File → Options and settings → Options**.
3. Locate the security settings for map visuals.
4. Enable the required Map and Filled Map options if they are available in your Power BI version.
5. Apply the settings and restart Power BI Desktop if prompted.

*Note: Map visual availability and security settings can vary by Power BI version and organizational policy.*

### Step 8: Create a Map of the Top 10 States by Total Sales

1. Open the Report view.
2. Select the **Map** visual from the Visualizations pane.
3. Drag the **State** field into the Location field well.
4. Drag **Total Sales** into the appropriate field well to represent sales.
5. Verify that the locations are recognized correctly.
6. Resize the map visual as required.

### Step 9: Apply a Top N Filter

1. Select the map visual.
2. Open the Filters pane.
3. Locate the **State** field under the visual-level filters.
4. Change the filter type to **Top N**.
5. Set the number of items to **10**.
6. Drag **Total Sales** into the *By value* field.
7. Click **Apply filter**.
8. Verify that the visual displays the top 10 states by Total Sales.

### Step 10: Configure Bubble Size and Tooltips

1. Select the map visual.
2. Locate the field wells for the map.
3. Add **Total Sales** to the Bubble size or Size field, if available for the selected map visual.
4. Add **Total Sales** to the Tooltips field.
5. Hover over the map bubbles to verify that the sales information appears.
6. Adjust the visual size and placement for better readability.

*Note: Available field wells depend on the map visual selected and the Power BI version.*

### Step 11: Create a Clustered Column Chart

1. Click an empty area of the report canvas.
2. Select the **Clustered Column Chart** visual.
3. Drag **Category** to the X-axis field.
4. Drag **Total Sales** to the Y-axis field.
5. Check that the chart displays total sales for each category.
6. Resize the chart and position it beside or below the map.

### Step 12: Format and Arrange the Visuals

1. Select the map visual and open the Format visual pane.
2. Add a suitable title, such as **Top 10 States by Total Sales**.
3. Select the clustered column chart.
4. Add a suitable title, such as **Total Sales by Category**.
5. Adjust the size, alignment, labels, and other formatting options as needed.
6. Ensure that both visuals are clearly visible.
7. Verify that the map and chart display the intended data.

### Step 13: Save the Power BI Report

1. Select **File → Save As**.
2. Choose the required folder.
3. Save the report as `Program-06.pbix`.
4. Verify that the file has been saved successfully.

## 📸 Screenshots

Add your actual screenshots in the following sections after uploading them to this repository.

### 1. Excel Dataset

*Insert a screenshot showing the original Excel dataset.*

### 2. Power Query Editor

*Insert a screenshot showing the Orders table and the applied transformations.*

### 3. Transformed Dataset

*Insert a screenshot showing the renamed Total Sales column and the cleaned data.*

### 4. Top 10 States by Total Sales

*Insert a screenshot of the map visual with the Top N filter applied.*

### 5. Total Sales by Category

*Insert a screenshot of the clustered column chart.*

### 6. Final Power BI Dashboard

*Insert a screenshot showing the completed report with both visuals.*

## 📈 Expected Result

The Power BI report should contain:

- A transformed Orders dataset.
- A map displaying the top 10 states by Total Sales.
- A clustered column chart showing Total Sales by Category.
- Tooltips that provide sales information when hovering over the map.
- A saved Power BI report named `Program-06.pbix`.

## 🎯 Learning Outcomes

After completing this program, students will be able to:

- Import Excel data into Power BI Desktop.
- Use Power Query Editor for data cleaning and transformation.
- Remove unnecessary columns and rows.
- Rename columns for better clarity.
- Apply Top N filters to visualizations.
- Create map-based visualizations.
- Build clustered column charts.
- Format and arrange visuals in a report.
- Save a Power BI report in `.pbix` format.

## ❓ Viva Voce Questions

**1. What is Power BI?**

Power BI is a business intelligence tool used to connect, transform, analyze, and visualize data.

**2. What is Power Query Editor?**

Power Query Editor is used to clean and transform data before loading it into Power BI.

**3. What is the purpose of removing unnecessary columns?**

Removing unnecessary columns simplifies the dataset and keeps only the information required for analysis.

**4. What does Close & Apply do?**

Close & Apply applies the transformations and loads the resulting data into Power BI Desktop.

**5. What is a Top N filter?**

A Top N filter displays a specified number of items based on a selected measure, such as the 10 states with the highest Total Sales.

**6. What is a map visual used for?**

A map visual represents data geographically using locations such as states or cities.

**7. What are tooltips in Power BI?**

Tooltips display additional information when a user hovers over a data point in a visual.

**8. What is a clustered column chart?**

A clustered column chart compares values across categories using vertical bars.

**9. What is a `.pbix` file?**

A `.pbix` file is a Power BI Desktop report file that stores report content and associated data/model information.

**10. Why do we use data transformation?**

Data transformation improves data quality, consistency, and suitability for analysis.

## 🎥 Screen Recording

[View the Program 6 screen recording on Google Drive](https://drive.google.com/drive/u/0/folders/12hpdL3JAwwcT_IWrmvS4nX5lsYFgjd0s)

## 📁 Repository Structure

```text
DATA-VISUALIZATION-BAIL504-LAB-PROGRAMS-5TH-SEM-VTU/
│
├── Program-01-Tableau-Basics/
├── Program-02-Connecting-Data-Sources/
├── Program-03-Creating-a-View/
├── Program-04-Dashboard-Creation/
├── Program-05-Introducing-Power-BI/
│
└── Program-06-Power-BI-Data-Transformation-and-Visualization/
    └── README.md
```

## ✅ Result

The Orders dataset was transformed using Power Query Editor, and Power BI visuals were created to represent the Top 10 States by Total Sales and Total Sales by Category. The report was saved as `Program-06.pbix`.

## 🏁 Conclusion

This program demonstrates how Power Query Editor can be used to prepare data for analysis and how Power BI visuals can communicate sales information effectively. The map and clustered column chart provide complementary views of sales across states and product categories.

---

**Author:** Iqra Farheen

**Repository:** Data Visualization Lab Programs – 5th Semester VTU
