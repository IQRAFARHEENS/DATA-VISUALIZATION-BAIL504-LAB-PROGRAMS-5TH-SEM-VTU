# Program 7: Creating Reports & Visualizations

## Different Types of Charts and Formatting Charts with Titles and Colors

### 1. Aim

To create reports and visualizations using Microsoft Power BI by importing an HR dataset, transforming data using Power Query Editor, creating different types of charts, and formatting visuals with titles, colors, labels, and slicers.

### 2. Software Requirements

- Microsoft Power BI Desktop
- HR dataset in CSV or Excel format
- Windows operating system

### 3. Objectives

- Import and transform an HR dataset.
- Create calculated columns using Power Query Editor.
- Create and format a KPI visual.
- Create pie, stacked column, matrix, stacked bar, and doughnut charts.
- Format visual titles, colors, labels, borders, and backgrounds.
- Sort age-band categories in the correct order.
- Add slicers for interactive filtering.
- Build a clear and meaningful Power BI report.

### 4. Procedure

## Step 1: Import the Dataset

1. Open Microsoft Power BI Desktop.
2. Click **Home → Get Data**.
3. Select the appropriate source, such as **Text/CSV** or **Excel workbook**.
4. Browse to the HR dataset and select it.
5. Click **Load** or **Transform Data**, depending on the option available.
6. If you choose **Transform Data**, the dataset opens in Power Query Editor.

## Step 2: Open Power Query Editor

1. Select **Home → Transform Data**.
2. Verify that the correct HR table is selected.
3. Examine the column names and data types.
4. Check for missing values, incorrect column names, and unnecessary columns.
5. Ensure that the dataset contains the fields required for the report, such as Attrition, Age, Age Band, Gender, Department, Job Role, and other available HR attributes.

## Step 3: Use the First Row as Headers

1. In Power Query Editor, select the dataset.
2. Open the **Home** or **Transform** tab.
3. Select **Use First Row as Headers**.
4. Verify that the first row now contains the column names.
5. Check that the headers are meaningful and correctly assigned.

## Step 4: Create the Attrition Count Column

The Attrition Count column can be used to count employees who have left the organization.

1. In Power Query Editor, select **Add Column → Custom Column**.
2. Enter the column name:

   `Attrition Count`

3. Enter the following formula:

```powerquery
if [Attrition] = "Yes" then 1 else 0
```

4. Click **OK**.
5. The new column contains `1` for employees whose Attrition value is Yes and `0` for other employees.
6. Select the new column.
7. From the data type menu, choose **Whole Number**.
8. Verify that the column contains numeric values.

**Note:** If you need to count all employee records instead of employees who left, create a separate column named `Employee Count` using the custom column formula `1`. Set its data type to Whole Number and summarize it using Sum. Use the appropriate count column according to the purpose of the visual.

## Step 5: Apply the Changes

1. Verify the column names, formulas, and data types.
2. Check that the Attrition Count column was created correctly.
3. Click **Home → Close & Apply**.
4. Wait for Power BI to load the transformed data into the report.

## Step 6: Create a KPI Visual — Overall Employees

1. In the Report view, select a blank area of the report canvas.
2. From the Visualizations pane, select a **Card** visual or the KPI-style visual specified in your lab instructions.
3. Drag the employee-count field into the visual's data field.
4. If using the Employee Count column containing 1 for each row, set its aggregation to **Sum**.
5. If using a unique employee identifier, use an appropriate distinct count where necessary.
6. Select the visual and open the **Format visual** pane.
7. Expand the **Title** section and switch it on.
8. Enter the title:

   `Overall Employees`

9. Set the title alignment to Center.
10. Choose a suitable title color.
11. Turn the visual background off if required by the lab instructions.
12. Turn the border on.
13. Set the corner radius to 20, if the selected visual supports this setting.
14. Turn the category label off if required.
15. Change the callout value font color to improve readability.
16. Resize and position the visual appropriately.

**Expected result:** A card displaying the overall employee count with the title *Overall Employees*.

## Step 7: Create a Pie Chart

1. Click a blank area of the report canvas.
2. Select **Pie Chart** from the Visualizations pane.
3. Drag a suitable categorical field, such as Gender or Department, into the Legend field.
4. Drag an appropriate measure, such as Employee Count, into the Values field.
5. If using a column containing 1 for every employee, ensure that the aggregation is Sum.
6. Select the pie chart.
7. Open **Format visual**.
8. Expand **Title** and turn it on.
9. Enter a suitable title, such as:

   `Employee Distribution by Gender`

10. Select appropriate colors for the categories.
11. Enable data labels if required.
12. Adjust label text size and color for readability.
13. Resize the visual and position it on the report canvas.

**Expected result:** A pie chart showing the distribution of employees across the selected categories.

## Step 8: Create a Stacked Column Chart

1. Select a blank area of the report canvas.
2. Choose **Stacked Column Chart** from the Visualizations pane.
3. Drag a suitable category, such as Department, into the X-axis field.
4. Drag a measure, such as Employee Count or Attrition Count, into the Y-axis field.
5. To compare groups, drag an additional categorical field into the Legend field.
6. Select the visual and open **Format visual**.
7. Turn on the title and enter a meaningful title, such as:

   `Employee Count by Department`

8. Adjust the title alignment, font size, and color.
9. Set the column colors according to the categories displayed.
10. Format the X-axis and Y-axis titles and labels.
11. Enable data labels if appropriate.
12. Adjust the visual size and placement.

**Expected result:** A stacked column chart comparing values across categories using vertical columns.

## Step 9: Sort Age-Band Categories

Age-band categories sometimes appear in alphabetical order instead of their intended numerical order. A numeric sort column can correct this.

1. Open **Transform Data** to return to Power Query Editor, or create the sort column using the appropriate method in Power BI.
2. Identify the age-band column, such as `CP_age_band`, if that is the column name in your dataset.
3. Create a numeric sort column that represents the intended order of the age bands.
4. Assign a number to each age band in ascending age order.
5. Ensure that the sort column has the Whole Number data type.
6. Click **Close & Apply** if you made the changes in Power Query Editor.
7. In Power BI Data or Table view, select the age-band column.
8. Open **Column tools → Sort by column**.
9. Select the numeric sort column.
10. Return to the report and verify that the age bands appear in the correct order.

**Important:** The numeric sort values must correspond consistently to the actual age-band categories in your dataset. Do not use alphabetical sorting when it produces the wrong age sequence.

## Step 10: Create a Matrix Visual

1. Select a blank area of the report canvas.
2. Choose **Matrix** from the Visualizations pane.
3. Drag a categorical field into **Rows**.
4. Drag another categorical field into **Columns**.
5. Drag a numeric measure, such as Employee Count or Attrition Count, into **Values**.
6. Select the matrix and open **Format visual**.
7. Expand **Row headers** and format the font, text size, and color.
8. Expand **Column headers** and format the font, text size, and color.
9. Expand **Values** and adjust the text size and display settings.
10. Expand **Grand total** or the relevant totals section and format it as required.
11. Check that row totals, column totals, and grand totals are displayed correctly where applicable.
12. Adjust column widths and row heights to improve readability.

**Expected result:** A matrix showing summarized values across rows and columns, with appropriate headers and totals.

## Step 11: Create a Stacked Bar Chart

1. Select a blank area of the report canvas.
2. Choose **Stacked Bar Chart** from the Visualizations pane.
3. Drag a category, such as Department or Job Role, into the Y-axis field.
4. Drag an appropriate measure into the X-axis field.
5. Add a categorical field to the Legend field if you want to divide each bar into segments.
6. Select the chart and open **Format visual**.
7. Turn on the title.
8. Enter a suitable title, such as:

   `Employee Count by Job Role`

9. Format the title alignment, font, and color.
10. Select suitable colors for the stacked categories.
11. Format axis labels and data labels as required.
12. Resize and position the chart.

**Expected result:** A horizontal stacked bar chart comparing values across categories.

## Step 12: Create a Doughnut Chart

1. Select a blank area of the report canvas.
2. Choose **Doughnut Chart** from the Visualizations pane.
3. Drag a categorical field into the Legend field.
4. Drag an appropriate measure into the Values field.
5. Select the visual and open **Format visual**.
6. Turn on the title.
7. Enter a suitable title, such as:

   `Employee Distribution by Department`

8. Choose suitable segment colors.
9. Enable data labels if required.
10. Format label text, size, and color.
11. Adjust the visual size and position.

**Expected result:** A doughnut chart showing category proportions around a blank center.

## Step 13: Add Slicers

1. Select a blank area of the report canvas.
2. Choose **Slicer** from the Visualizations pane.
3. Drag a categorical field, such as Department, Gender, or Job Role, into the slicer's Field area.
4. Resize and position the slicer.
5. Repeat the process to create additional slicers if required.
6. Select each slicer and open **Format visual**.
7. Format the slicer title, text, background, and border where applicable.
8. Select a value in a slicer.
9. Verify that the other visuals respond to the selected filter.
10. If a visual does not respond as expected, check **Format → Edit interactions** and confirm the intended filter interaction.

**Expected result:** Interactive slicers that allow users to filter the report by selected HR attributes.

## Step 14: Format the Charts Consistently

Apply consistent formatting across the report:

1. Use meaningful and descriptive chart titles.
2. Keep title alignment consistent.
3. Choose colors that distinguish categories clearly.
4. Maintain readable font sizes.
5. Format axis labels and data labels appropriately.
6. Use borders and backgrounds only where they improve readability.
7. Avoid excessive colors and unnecessary visual elements.
8. Align visuals neatly on the report canvas.
9. Use **Format Painter** where supported to copy formatting from one visual to another.
10. Review the report to ensure that all charts are easy to understand.

## Step 15: Save the Power BI Report

1. Review all the visuals and slicers.
2. Verify that the counts and aggregations are appropriate.
3. Check that the age bands appear in the correct order.
4. Ensure that chart titles and colors are consistent.
5. Click **File → Save As**.
6. Enter the report filename:

   `Program-07.pbix`

7. Select the required location and click **Save**.

### 5. Common Types of Charts in Data Visualization

| Chart Type | Purpose |
|---|---|
| Bar Chart | Compares values using horizontal bars. |
| Column Chart | Compares values using vertical columns. |
| Stacked Bar Chart | Compares categories using horizontal bars divided into segments. |
| Stacked Column Chart | Compares categories using vertical columns divided into segments. |
| Clustered Bar Chart | Compares multiple series using grouped horizontal bars. |
| Clustered Column Chart | Compares multiple series using grouped vertical columns. |
| Line Chart | Displays trends or changes over time. |
| Area Chart | Displays trends with the area below the line filled. |
| Stacked Area Chart | Shows cumulative values across categories or time. |
| Pie Chart | Shows proportions of a whole using slices. |
| Doughnut Chart | Shows proportions of a whole using segments around a blank center. |
| Treemap | Displays hierarchical data using nested rectangles. |
| Scatter Chart | Displays relationships between numerical variables. |
| Waterfall Chart | Shows how positive and negative values contribute to a final total. |
| Funnel Chart | Displays values across sequential stages. |
| Gauge Chart | Displays a value in relation to a target or range. |
| Matrix | Displays summarized data across rows and columns. |
| Card / KPI | Highlights an important number or indicator. |

### 6. Important Power BI Formulas

**Formula 1: Count employees who left the organization**

Create a Custom Column in Power Query Editor:

```powerquery
if [Attrition] = "Yes" then 1 else 0
```

Set the column's data type to Whole Number and summarize it using Sum.

**Formula 2: Count all employee records**

Create a Custom Column named `Employee Count`:

```powerquery
1
```

Set the column's data type to Whole Number and summarize it using Sum.

**Note:** These are Power Query M formulas for a Custom Column. They are not DAX measures.

### 7. Viva Questions and Answers

**1. What is data visualization?**

Data visualization is the graphical representation of data using charts, graphs, tables, and other visual elements.

**2. What is Microsoft Power BI?**

Microsoft Power BI is a business intelligence tool used to connect, transform, analyze, and visualize data.

**3. What is Power Query Editor?**

Power Query Editor is used to import, clean, transform, and prepare data before loading it into Power BI.

**4. Why do we use the Use First Row as Headers option?**

It converts the first row of the dataset into column names.

**5. What is a custom column?**

A custom column is a new column created using a formula or expression in Power Query Editor.

**6. Why is the Whole Number data type used for Attrition Count?**

It stores the numeric values 0 and 1, which can be summed to calculate the number of employees who left.

**7. What is a KPI or card visual?**

A KPI or card-style visual highlights an important measure, such as total employees or attrition count.

**8. What is a pie chart?**

A pie chart represents the proportions of categories as slices of a circle.

**9. What is a stacked column chart?**

It compares categories using vertical columns divided into segments representing different groups.

**10. What is a matrix visual?**

A matrix displays data across rows and columns and can show grouped values, subtotals, and grand totals.

**11. What is a stacked bar chart?**

It compares categories using horizontal bars divided into segments.

**12. What is a doughnut chart?**

A doughnut chart displays parts of a whole using segments arranged around a blank center.

**13. What is a slicer?**

A slicer is an interactive report visual that filters other visuals using selected values.

**14. What is Format Painter?**

Format Painter copies formatting from one visual to another where supported.

**15. Why do we use a sort column for age bands?**

A numeric sort column ensures that age-band categories appear in the intended logical order instead of an alphabetical order.

**16. Why are titles and colors important?**

They improve readability, distinguish categories, and help users understand the information presented by each visual.

**17. What is a `.pbix` file?**

A `.pbix` file is a Power BI Desktop report file containing report content and associated model/data information.

### 8. Result

The HR dataset was imported and transformed using Power Query Editor. An Attrition Count column was created and assigned the Whole Number data type. KPI, pie, stacked column, matrix, stacked bar, and doughnut visuals were created and formatted with titles, colors, and other display settings. Slicers were added to support interactive filtering, and the report was saved as `Program-07.pbix`.

### 9. Conclusion

This program demonstrates the workflow for creating a Power BI report, from importing and preparing HR data to building and formatting multiple visualizations. It also covers category sorting, consistent formatting, and interactive slicers. These techniques help present HR information in a clear, organized, and meaningful way.

**Author:** Iqra Farheen
