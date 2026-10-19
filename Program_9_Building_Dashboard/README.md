# Experiment No. 9: Building Dashboard in Power BI

## Analysis of Revenue in a Sales Dataset

## 1. Aim

To analyze revenue data using Microsoft Power BI by creating a filled map, line chart, age bins, doughnut chart, butterfly chart, calculated measures, profitability classification, and an interactive dashboard.

## 2. Software Requirements

- Microsoft Power BI Desktop
- Sales dataset containing revenue, state, month, age, region, gender, and product category fields
- Windows operating system

## 3. Objectives

- Import and transform the sales dataset.
- Create a filled map to identify states with the highest revenue.
- Create a line chart to analyze monthly revenue trends.
- Create age bins of size 10 and analyze revenue by age group.
- Create a doughnut chart to display revenue distribution by region.
- Create a butterfly chart to compare male and female revenue by product category.
- Calculate average revenue per state.
- Classify states as profitable or non-profitable.
- Create KPI cards and slicers.
- Combine all visualizations into an interactive dashboard.

## 4. Introduction

A dashboard is a visual representation of important information and key performance indicators. It combines multiple charts, maps, tables, and cards into a single report page to help users understand data and make informed decisions.

Microsoft Power BI provides a variety of visualizations and data analysis features. In this experiment, a sales dataset is used to analyze revenue based on geographical location, month, age, region, gender, product category, and state profitability.

The experiment includes data transformation, calculated measures, calculated columns, visual formatting, and dashboard design.

## 5. Dataset Requirements

The sales dataset should contain the following fields, where available:

| Field | Purpose |
|---|---|
| State | Identifies the state associated with each record. |
| Revenue | Represents revenue generated from sales. |
| Month | Used to analyze monthly revenue trends. |
| Age | Used to create age groups. |
| Region | Used to compare revenue across regions. |
| Gender | Used to compare male and female revenue. |
| ProductCategory | Identifies the product category. |
| Country | Used for geographical filtering through a slicer. |

**Note:** The actual column names in your dataset may differ. Use the corresponding fields from your imported table. The DAX formulas below assume that the table is named `SalesTable`.

# 6. Procedure

## Step 1: Import the Sales Dataset

1. Open Microsoft Power BI Desktop.
2. Navigate to the **Home** tab.
3. Click **Get Data**.
4. Select the appropriate data source, such as **Text/CSV** or **Excel workbook**.
5. Browse to the sales dataset.
6. Select the file and click **Open**.
7. Preview the data.
8. Click **Transform Data** to open Power Query Editor.
9. Verify that the expected columns are present.

## Step 2: Clean and Transform the Dataset

1. In Power Query Editor, inspect the imported table.
2. Check the column names and data types.
3. Identify unnecessary columns.
4. Locate the last column containing only null values, as specified in the lab instructions.
5. Right-click that column and select **Remove**.
6. Check whether any other columns contain unnecessary data.
7. Ensure that the `Revenue` column has a suitable numeric data type, such as Decimal Number or Fixed Decimal Number.
8. Ensure that `Age` is a Whole Number.
9. Ensure that `State`, `Region`, `Gender`, `ProductCategory`, and `Country` have suitable text data types.
10. Verify the `Month` field and confirm that it can be used for monthly analysis.
11. Check for blank values and obvious data-quality issues.
12. Click **Home → Close & Apply**.
13. Wait for Power BI to load the transformed data.

**Expected result:** The sales dataset is loaded into Power BI with unnecessary columns removed and suitable data types assigned.

## Question 1: Create a Filled Map to Identify the State with the Highest Revenue

### Objective

To create a choropleth-style filled map that uses color intensity to show revenue across states.

### Step 1: Add a Filled Map

1. Open Report view.
2. Select a blank area of the report canvas.
3. In the Visualizations pane, select **Filled Map**, if available.
4. If the visual is not immediately visible, locate it in the visualization options.
5. Resize the map to provide enough space for state labels and tooltips.

### Step 2: Configure the Map

1. Drag the `State` field into **Location**.
2. Drag the `Revenue` field into **Color saturation**, **Values**, or the equivalent field well available in your version of Power BI.
3. Ensure that Revenue is summarized using **Sum**.
4. If the map displays the wrong locations, select the State column and assign the appropriate geographical data category under **Column tools → Data category**, where available.
5. If states have the same names in different countries, add Country information where the visual supports it to help disambiguate the locations.

### Step 3: Format the Map

1. Select the map.
2. Open the **Format visual** pane.
3. Configure the title.
4. Enter the title:

   `Revenue by State`

5. Select an appropriate color gradient.
6. Use lighter shades for lower revenue and darker shades for higher revenue, where supported.
7. Enable tooltips to show state names and revenue values.
8. Adjust the map zoom and visual size.

### Step 4: Identify the Highest-Revenue State

1. Hover over individual states to inspect their revenue values.
2. Compare the displayed values.
3. Identify the state with the highest revenue.
4. If the map is difficult to interpret, create a supporting bar chart with State on the axis and Sum of Revenue as the value, then sort it in descending order.

**Expected result:** A filled map showing revenue distribution by state. The highest-revenue state can be identified by comparing the revenue values.

**Note:** Power BI map features and field wells can vary by version. If Filled Map is unavailable, use an approved filled-map visual or another supported map visual that can represent state-level revenue.

## Question 2: Create a Line Chart to Show Revenue by Month

### Objective

To analyze how revenue changes throughout the months of the year.

### Step 1: Add a Line Chart

1. Select a blank area of the report canvas.
2. Choose **Line Chart** from the Visualizations pane.
3. Resize the visual.

### Step 2: Configure the Chart

1. Drag the `Month` field into the **X-axis**.
2. Drag the `Revenue` field into the **Y-axis** or **Values** field well.
3. Ensure that Revenue is summarized using **Sum**.
4. If the dataset contains a Date field, use the appropriate date field or month level from the date hierarchy.

### Step 3: Arrange the Months Correctly

If the month names appear alphabetically instead of chronologically:

1. Create or identify a numeric month-order field, where January = 1, February = 2, and so on through December = 12.
2. Select the Month column.
3. Choose **Column tools → Sort by column**.
4. Select the numeric month-order field.
5. Return to the report and verify the month sequence.

If the dataset contains multiple years, use a Year-Month field or a suitable date hierarchy to prevent the same month across different years from being combined unintentionally.

### Step 4: Format the Chart

1. Select the line chart.
2. Open **Format visual**.
3. Turn on the title.
4. Enter:

   `Monthly Revenue Trend`

5. Set the title alignment and font size.
6. Choose a suitable line color.
7. Format the X-axis and Y-axis titles.
8. Enable data labels if they improve readability.
9. Configure markers if required.
10. Adjust the visual size and placement.

**Expected result:** A line chart displaying revenue changes across months.

## Question 3: Create Age Bins of Size 10 and Show Revenue

### Objective

To group employee or customer ages into intervals of 10 and analyze revenue for each age group.

### Step 1: Create Age Bins

1. Open the Data or Table view.
2. Locate the `Age` field.
3. Right-click the Age field.
4. Select **New group**, if this option is available for the field.
5. In the grouping dialog, select **Bin**.
6. Set the bin size to:

   `10`

7. Confirm the operation.
8. Verify that a new grouped field, such as `Age (bins)`, has been created.

**If the New Group option is unavailable:** Create a calculated column using DAX, or use Power Query to construct age ranges. The DAX alternative is provided below.

### Alternative: Create Age Groups Using DAX

Select **Modeling → New column** and enter:

```dax
AgeBin =
VAR LowerAge =
    INT(SalesTable[Age] / 10) * 10
RETURN
    FORMAT(LowerAge, "0")
        & "–"
        & FORMAT(LowerAge + 9, "0")
```

This creates labels such as `20–29`, `30–39`, and `40–49`.

**Important:** This alternative creates text labels, not a native numeric bin. If you use it, create a corresponding numeric lower-bound column and sort the labels by that column so that the age groups appear in ascending order.

### Step 2: Create a Stacked Column Chart

1. Return to Report view.
2. Select **Stacked Column Chart** from the Visualizations pane.
3. Drag `Age (bins)` or the new `AgeBin` field into the **X-axis**.
4. Drag `Revenue` into the **Y-axis** or **Values** field well.
5. Ensure Revenue is summarized using Sum.

### Step 3: Format the Chart

1. Select the chart.
2. Open **Format visual**.
3. Turn on the title.
4. Enter:

   `Revenue by Age Group`

5. Format the title, axis labels, and colors.
6. Enable data labels if necessary.
7. Confirm that the age groups are displayed in the intended order.

**Expected result:** A stacked column chart showing revenue for each age group.

## Question 4: Create a Doughnut Chart Showing Revenue Percentage by Region

### Objective

To show each region's contribution to total revenue using a doughnut chart.

### Step 1: Create a Revenue Measure

Select **Modeling → New measure** and enter:

```dax
TotalRevenue =
SUM(SalesTable[Revenue])
```

Press Enter to create the measure.

### Step 2: Add a Doughnut Chart

1. Return to Report view.
2. Select a blank area of the canvas.
3. Choose **Doughnut Chart** from the Visualizations pane.
4. Drag `Region` into the **Legend** field.
5. Drag `TotalRevenue` into the **Values** field.

### Step 3: Display Revenue Percentages

1. Select the doughnut chart.
2. Open **Format visual**.
3. Expand **Detail labels** or **Data labels**, depending on the Power BI version.
4. Enable the labels.
5. Select the option for **Percent of total**, where available.
6. If the visual does not offer this option, create the percentage measure below.
7. Format the labels so that the percentages are readable.
8. Turn on the title and enter:

   `Revenue Contribution by Region`

9. Choose distinct colors for the regions.

### Optional: Create a Revenue Percentage Measure

```dax
RevenuePercentage =
DIVIDE(
    [TotalRevenue],
    CALCULATE(
        [TotalRevenue],
        REMOVEFILTERS(SalesTable[Region])
    ),
    0
)
```

Format the measure as a percentage using **Measure tools → Format → Percentage**.

Add this measure to a tooltip or another suitable visual if you want to display the calculated percentage explicitly.

### Understanding the Zero-Access Note

The lab instructions mention creating a "zero access" effect. This term is not a standard doughnut-chart setting in Power BI, and the supplied instructions do not specify a calculated-field formula for it. The documented steps describe changing detail-label positioning and displaying percentages.

A doughnut chart already has a blank center. Use its available label settings to display the revenue contribution clearly. Do not assume that a label-position setting creates a separate zero-value calculation.

**Expected result:** A doughnut chart showing the percentage contribution of each region to total revenue.

## Question 5: Create a Butterfly Chart to Compare Female and Male Revenue by Product Category

### Objective

To compare female and male revenue across product categories using bars arranged in opposite directions.

### Step 1: Create the Total Revenue Measure

Select **Modeling → New measure** and enter:

```dax
TotalRevenue =
SUM(SalesTable[Revenue])
```

If this measure already exists from Question 4, reuse it instead of creating another measure with the same name.

### Method 1: Compare Revenue Using a Stacked Column Chart

This method provides a straightforward comparison of male and female revenue, although it is not a true butterfly chart.

1. Select **Stacked Column Chart**.
2. Drag `ProductCategory` into the X-axis.
3. Drag `TotalRevenue` into the Y-axis or Values field well.
4. Drag `Gender` into the Legend field.
5. Format the title as:

   `Revenue by Product Category and Gender`

6. Choose different colors for Female and Male.
7. Enable data labels if necessary.

**Expected result:** A stacked column chart comparing revenue by gender across product categories.

### Method 2: Create a Butterfly Chart Using Two Bar Charts

A butterfly chart, also called a population-pyramid-style chart, places two horizontal bar series on opposite sides of a shared category axis.

#### Step 1: Create a Female Revenue Measure

```dax
FemaleRevenue =
CALCULATE(
    [TotalRevenue],
    SalesTable[Gender] = "Female"
)
```

#### Step 2: Create a Male Revenue Measure

```dax
MaleRevenue =
CALCULATE(
    [TotalRevenue],
    SalesTable[Gender] = "Male"
)
```

These formulas assume that the Gender column contains the text values `Female` and `Male`. If the dataset uses different labels, replace them accordingly.

#### Step 3: Create the Female Bar Chart

1. Add a **Clustered Bar Chart**.
2. Drag `ProductCategory` into the Y-axis.
3. Drag `FemaleRevenue` into the X-axis or Values field well.
4. Format the chart title as:

   `Female Revenue`

5. Choose a distinct color for the bars.

#### Step 4: Create the Male Bar Chart

1. Add another **Clustered Bar Chart**.
2. Drag `ProductCategory` into the Y-axis.
3. Drag `MaleRevenue` into the X-axis or Values field well.
4. Format the chart title as:

   `Male Revenue`

5. Choose a different color for the bars.

#### Step 5: Arrange the Charts

1. Place the two bar charts side by side.
2. Keep the product categories in the same order.
3. Use the same vertical size for both charts.
4. Align the category labels so that corresponding categories can be compared.
5. Use consistent axis scales if you want the bar lengths to be directly comparable.
6. Remove unnecessary borders and visual clutter.

**Important:** Two side-by-side bar charts are a comparison layout, not automatically a true butterfly chart. To create the classic butterfly effect, one series must extend left and the other right from a shared center line. Power BI's standard bar chart may not support this directly. Use a suitable custom butterfly visual or a carefully configured diverging-bar approach if your lab requires the true mirrored design.

**Expected result:** A comparison of female and male revenue by product category, using either the stacked column method or the mirrored bar-chart method.

## Question 6: Calculate Average Revenue per State and Display Profitable and Non-Profitable States

### Objective

To calculate revenue by state and classify each state according to a specified threshold.

### Step 1: Create the Total Revenue Measure

If it does not already exist, select **Modeling → New measure** and enter:

```dax
TotalRevenue =
SUM(SalesTable[Revenue])
```

### Step 2: Create the Average Revenue per State Measure

Select **Modeling → New measure** and enter:

```dax
AverageRevenuePerState =
AVERAGEX(
    VALUES(SalesTable[State]),
    CALCULATE(
        SUM(SalesTable[Revenue])
    )
)
```

This measure calculates revenue for each distinct state and averages those state-level revenue totals within the current filter context.

### Step 3: Display the Average Revenue by State

1. Return to Report view.
2. Add a **Table** visual.
3. Drag `State` into the table.
4. Drag `TotalRevenue` into the table.
5. Verify that revenue is summarized by state.
6. Use the `AverageRevenuePerState` measure in a Card or another suitable visual to show the average across the states in the current filter context.

**Important:** The average measure above is a measure, not a calculated column. A measure cannot generally be referenced in a calculated column in the same way as a row-level column. Use the following calculated-column method to classify individual states.

### Step 4: Create a State Revenue Calculated Column

Select **Modeling → New column** and enter:

```dax
StateRevenue =
CALCULATE(
    SUM(SalesTable[Revenue]),
    ALLEXCEPT(
        SalesTable,
        SalesTable[State]
    )
)
```

This column repeats the total revenue for each state across that state's rows. It is useful for a row-level classification based on state revenue.

### Step 5: Create the Profitability Status Column

Select **Modeling → New column** and enter:

```dax
ProfitabilityStatus =
IF(
    SalesTable[StateRevenue] > 1000,
    "Profitable",
    "Non-Profitable"
)
```

This uses 1,000 as the classification threshold specified in the lab instructions.

**Important:** This classifies states by total revenue relative to 1,000. Revenue alone does not establish actual profitability because profit normally requires costs or expenses. For this experiment, follow the lab's requested revenue threshold and label.

### Step 6: Display the Results in a Table

1. Add a **Table** visual to the report canvas.
2. Drag `State` into the table.
3. Drag `StateRevenue` into the table.
4. Drag `ProfitabilityStatus` into the table.
5. Format the column headers and values.
6. Sort by State or StateRevenue as required.
7. Verify that each state is classified according to the specified threshold.

**Expected result:** A table showing states, their total revenue, and their classification as Profitable or Non-Profitable according to the threshold of 1,000.

## Extra Task 1: Display Total Revenue Using a Card

A Card visual highlights a single important metric, such as total revenue, average revenue, or the number of customers.

### Steps

1. Select a blank area of the report canvas.
2. Choose **Card** from the Visualizations pane.
3. Drag `TotalRevenue` into the Card's data field.
4. Confirm that the measure displays the total revenue.
5. Open **Format visual**.
6. Turn on the title.
7. Enter:

   `Total Revenue`

8. Format the title, callout value, and display units.
9. Resize and position the card near the top of the dashboard.

**Expected result:** A card displaying the total revenue in the current filter context.

## Extra Task 2: Add a Country Slicer

A slicer allows users to filter multiple visuals by selecting a field value.

### Steps

1. Select a blank area of the report canvas.
2. Choose **Slicer** from the Visualizations pane.
3. Drag `Country` into the slicer's Field area.
4. Format the slicer title.
5. Enter:

   `Filter by Country`

6. Resize and position the slicer.
7. Select a country from the slicer.
8. Verify that the relevant visuals update.
9. If a visual does not respond, open **Format → Edit interactions** and review its interaction settings.

**Expected result:** An interactive country slicer that filters connected visuals.

## Question 7: Build the Final Dashboard

### Objective

To combine the visualizations, measures, table, KPI card, and slicer into a single, organized Power BI report page.

### Step 1: Plan the Dashboard Layout

Before arranging the visuals, decide which information should receive the most attention.

A recommended layout is:

- **Top row:** Dashboard title and Total Revenue card.
- **Left section:** Country slicer and other relevant filters.
- **Center or upper section:** Filled map showing revenue by state.
- **Middle section:** Line chart showing monthly revenue.
- **Lower section:** Revenue by age group and revenue contribution by region.
- **Right or lower section:** Gender comparison chart and state profitability table.

The exact arrangement depends on the screen size and the dimensions of the visuals.

### Step 2: Add a Dashboard Title

1. Open Report view.
2. Select **Insert → Text box**.
3. Enter the title:

   `SALES REVENUE ANALYSIS DASHBOARD`

4. Format the title using a readable font size and suitable alignment.
5. Place it at the top of the report page.

### Step 3: Add the Total Revenue KPI Card

1. Add or move the Total Revenue Card to the top row.
2. Resize it so that the value is easy to read.
3. Keep the title short and meaningful.
4. Format the card consistently with the other visuals.
5. Verify that the value updates when applicable filters are selected.

### Step 4: Position the Filled Map

1. Move the Revenue by State filled map to the main analysis area.
2. Give it enough space to display the geographical information clearly.
3. Ensure the color gradient is understandable.
4. Keep the map title visible.
5. Check the state-level revenue values through tooltips.

### Step 5: Position the Monthly Revenue Line Chart

1. Place the Monthly Revenue Trend chart next to or below the map.
2. Ensure the month axis is chronological.
3. Make the line and labels readable.
4. Avoid overcrowding the chart with unnecessary labels.

### Step 6: Position the Age-Bin Chart

1. Place the Revenue by Age Group chart in the lower section.
2. Ensure that the age bins are in ascending order.
3. Keep the column colors consistent with the overall dashboard theme.
4. Verify that the revenue values are correct.

### Step 7: Position the Regional Doughnut Chart

1. Move the Revenue Contribution by Region doughnut chart into the lower section.
2. Ensure that the legend identifies each region.
3. Show percentage labels where available.
4. Use colors that make each region distinguishable.

### Step 8: Add the Gender Revenue Comparison

1. Position the gender comparison chart beside the age or regional visual.
2. Use clearly distinguishable colors for female and male revenue.
3. Keep product categories aligned if using two separate bar charts.
4. Add an informative title.
5. Ensure that the chart does not become too small to interpret.

### Step 9: Add the State Profitability Table

1. Position the StateRevenue and ProfitabilityStatus table in the lower or right section.
2. Ensure the State, StateRevenue, and ProfitabilityStatus columns are visible.
3. Format the table headers.
4. Adjust column widths to avoid truncating state names or profitability labels.
5. Confirm that the classification uses the threshold specified in the lab.

### Step 10: Add and Format the Country Slicer

1. Place the Country slicer on the left side or in a dedicated filter area.
2. Give it a clear title.
3. Ensure that the selected value is visible.
4. Avoid allowing the slicer to overlap any charts.
5. Test the slicer after arranging the dashboard.

### Step 11: Apply Consistent Formatting

1. Use a consistent theme and color palette across the report.
2. Apply readable titles and axis labels.
3. Keep the spacing between visuals consistent.
4. Align the edges of cards and charts.
5. Use borders or backgrounds only when they improve readability.
6. Avoid excessive visual effects and unnecessary gridlines.
7. Ensure that each chart has a meaningful title.
8. Use consistent number formats for revenue.
9. Use appropriate display units such as thousands or millions when needed.
10. Keep the report page uncluttered.

### Step 12: Configure Visual Interactions

1. Select the Country slicer.
2. Open **Format → Edit interactions** if available in your Power BI version.
3. Inspect how the slicer affects each visual.
4. Ensure that it filters the appropriate charts and table.
5. Check the interaction between the map and other charts if cross-filtering is required.
6. Adjust interactions only when needed.
7. Exit Edit interactions mode when finished.

**Note:** Visual interactions depend on the fields, relationships, and configuration in the data model. Not every visual will necessarily filter every other visual in the same way.

### Step 13: Test the Completed Dashboard

1. Select a country in the slicer.
2. Observe the Total Revenue card.
3. Check the revenue map and monthly trend.
4. Inspect the age-bin and regional charts.
5. Verify the gender comparison.
6. Review the state profitability table.
7. Clear the slicer selection and confirm that the report returns to the unfiltered view.
8. Check for blank visuals, incorrect totals, missing labels, or overlapping elements.

### Step 14: Save the Dashboard

1. Click **File → Save As**.
2. Enter the filename:

   `Program-09.pbix`

3. Choose the required folder.
4. Click **Save**.
5. Reopen the file if necessary to confirm that the report has been saved successfully.

**Expected result:** An interactive Power BI report page containing a filled map, monthly revenue line chart, age-bin chart, regional doughnut chart, gender comparison, state profitability table, Total Revenue card, and Country slicer.

## 7. Important DAX Formulas

### 1. Total Revenue

```dax
TotalRevenue =
SUM(SalesTable[Revenue])
```

### 2. Average Revenue per State

```dax
AverageRevenuePerState =
AVERAGEX(
    VALUES(SalesTable[State]),
    CALCULATE(
        SUM(SalesTable[Revenue])
    )
)
```

### 3. State Revenue Calculated Column

```dax
StateRevenue =
CALCULATE(
    SUM(SalesTable[Revenue]),
    ALLEXCEPT(
        SalesTable,
        SalesTable[State]
    )
)
```

### 4. Profitability Status

```dax
ProfitabilityStatus =
IF(
    SalesTable[StateRevenue] > 1000,
    "Profitable",
    "Non-Profitable"
)
```

### 5. Female Revenue

```dax
FemaleRevenue =
CALCULATE(
    [TotalRevenue],
    SalesTable[Gender] = "Female"
)
```

### 6. Male Revenue

```dax
MaleRevenue =
CALCULATE(
    [TotalRevenue],
    SalesTable[Gender] = "Male"
)
```

### 7. Revenue Percentage by Region

```dax
RevenuePercentage =
DIVIDE(
    [TotalRevenue],
    CALCULATE(
        [TotalRevenue],
        REMOVEFILTERS(SalesTable[Region])
    ),
    0
)
```

**Important:** Replace `SalesTable` and field names with the exact names used in your Power BI data model. Measures and calculated columns serve different purposes; create each formula using the correct Modeling option.

## 8. Summary of Visualizations

| Visualization | Purpose |
|---|---|
| Filled Map | Identifies geographical revenue distribution by state. |
| Line Chart | Displays monthly revenue trends. |
| Stacked Column Chart | Compares revenue across age groups. |
| Doughnut Chart | Displays the percentage contribution of regions to revenue. |
| Butterfly Chart | Compares female and male revenue by product category. |
| Table | Displays state revenue and profitability classification. |
| Card | Highlights total revenue. |
| Slicer | Filters the report by country. |

## 9. Viva Questions and Answers

**1. What is a dashboard in Power BI?**

A dashboard is a visual summary of important metrics and information. In Power BI Desktop, multiple visuals are typically arranged on a report page to create a dashboard-style report.

**2. What is a filled map?**

A filled map displays geographical areas using different colors to represent a measure, such as revenue.

**3. Why is a line chart used?**

A line chart displays changes and trends in values across an ordered dimension, such as months.

**4. What is binning?**

Binning groups continuous numeric values into intervals. For example, an age bin size of 10 groups ages into intervals of ten years.

**5. What is a doughnut chart?**

A doughnut chart displays the relative contributions of categories using segments arranged around a central blank area.

**6. What is a butterfly chart?**

A butterfly chart compares two series using bars extending in opposite directions from a shared center, making comparisons between groups easier.

**7. What is a DAX measure?**

A DAX measure is a calculation evaluated according to the current filter context. For example, TotalRevenue calculates the sum of revenue.

**8. What is a calculated column?**

A calculated column computes a value for each row in a table using a DAX expression.

**9. What is the difference between a measure and a calculated column?**

A calculated column is evaluated row by row and stored in the data model, while a measure is evaluated when a visual queries it and responds to the current filter context.

**10. What does SUM do in DAX?**

SUM adds the numeric values in a specified column.

**11. What does AVERAGEX do in DAX?**

AVERAGEX evaluates an expression for each row of a table and returns the average of the resulting values.

**12. What does REMOVEFILTERS do?**

REMOVEFILTERS removes filters from the specified table or column within a calculation.

**13. What is a Card visual?**

A Card visual highlights a single important value, such as total revenue.

**14. What is a slicer?**

A slicer is an interactive visual that lets users filter other connected visuals by selecting values.

**15. Why is dashboard formatting important?**

Formatting improves readability, consistency, and the presentation of analytical results.

**16. How can we identify the state with the highest revenue?**

Compare state-level revenue values on the filled map, or use a supporting bar chart sorted in descending order by revenue.

**17. What is profitability classification in this experiment?**

It is the classification of states as Profitable or Non-Profitable according to the revenue threshold specified in the lab instructions.

## 10. Result

The sales dataset was imported and transformed using Power Query Editor. A filled map was created to analyze revenue by state, a line chart was created to examine monthly revenue, and age bins of size 10 were used to analyze revenue by age group. A doughnut chart displayed regional revenue contribution, and a gender comparison visual was created for product categories. DAX calculations were used to calculate total revenue, average revenue per state, and state revenue classifications. A Card visual and Country slicer were added, and the visualizations were arranged and formatted into a dashboard-style Power BI report.

## 11. Conclusion

This experiment demonstrates how Microsoft Power BI can be used to analyze sales revenue through geographical, temporal, demographic, regional, and gender-based visualizations. It also demonstrates the use of DAX measures, calculated columns, age binning, slicers, and visual formatting. Combining these components into a well-organized report helps users explore sales performance and interpret revenue patterns effectively.

**Author:** Iqra Farheen
