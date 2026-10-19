# Experiment No. 10: Analysis of GDP Dataset

## 1. Aim

To analyze and visualize GDP data using Tableau by creating symbol maps, bar charts, pie charts, comparative charts, and circle views for selected countries and years.

## 2. Software Requirements

- Tableau Desktop or Tableau Public
- GDP dataset containing country names, latitude, longitude, and GDP values for multiple years
- Windows operating system

## 3. Objectives

- Visualize countries using latitude and longitude on a symbol map.
- Compare Belgium's GDP between 2006 and 2026 using a bar chart.
- Visualize GDP values for India, Nepal, Romania, South Asia, and Singapore for 2010 using a pie chart.
- Compare GDP values for Bhutan and Costa Rica from 2016 to 2018.
- Create a circle view to compare GDP values for Mexico, Algeria, Fiji, and Estonia from 2004 to 2006.
- Apply filters, colors, labels, and formatting to improve visualization.
- Understand the use of Measure Names and Measure Values in Tableau.

## 4. Introduction

Gross Domestic Product (GDP) is an economic indicator that represents the monetary value of goods and services produced within a country during a specified period.

Data visualization tools such as Tableau help analyze GDP data across countries and years. Maps show geographical distributions, bar charts compare values, pie charts display proportions, and circle views provide a visual comparison of multiple categories.

In this experiment, a GDP dataset is used to create different visualizations by selecting countries and years and comparing their GDP values.

## 5. Dataset Requirements

The GDP dataset should contain fields similar to the following:

| Field | Description |
|---|---|
| Country | Name of the country or geographical region |
| Latitude | Geographical latitude |
| Longitude | Geographical longitude |
| Measure Names | Tableau-generated field representing the names of measures |
| Measure Values | Tableau-generated field representing the values of measures |
| Year fields | GDP values for different years, such as 2004, 2005, 2006, and 2010 |

**Note:** The exact structure depends on the supplied dataset. Some datasets store years as separate columns, while others store years as rows. Follow the instructions below according to the structure of your file.

# 6. Procedure

## Step 1: Import the GDP Dataset

1. Open Tableau Desktop or Tableau Public.
2. Under **Connect**, select the appropriate data source, such as Microsoft Excel or Text File.
3. Browse to the GDP dataset.
4. Select the file and open it.
5. Verify that the dataset is displayed correctly.
6. Check that the Country, Latitude, Longitude, and yearly GDP fields are available.
7. If Tableau displays incorrect field types, correct them using the data type icons in the Data pane.
8. Confirm that latitude and longitude are numeric fields.
9. Verify that GDP values are numeric.
10. Open a worksheet to begin creating visualizations.

**Expected result:** The GDP dataset is loaded into Tableau and is ready for analysis.

# Question 1: Create a Symbol Map Using Latitude, Longitude, and Country

## Objective

To visualize the geographical locations of countries using latitude and longitude, with country names and GDP values displayed on the map.

### Step 1: Create a New Worksheet

1. Open a new worksheet.
2. Locate the Latitude and Longitude fields in the Data pane.
3. If the dataset contains latitude and longitude columns, ensure they are recognized as numeric fields.
4. If Tableau has generated geographic fields automatically, verify that they correspond to the correct geographical locations.

### Step 2: Place Latitude and Longitude

1. Drag **Latitude** to the **Rows** shelf.
2. Drag **Longitude** to the **Columns** shelf.
3. Tableau should generate a map using the coordinate fields.
4. If necessary, select the **Map** view or use the appropriate geographic settings.

### Step 3: Configure the Marks Card

1. Locate the **Marks** card.
2. Select **Circle** or **Shape** as the mark type, if required.
3. Drag **Country** to **Color**.
4. Drag **Country** to **Label** to display country names.
5. Drag a GDP measure for a selected year to **Label** or **Tooltip**.
6. If the GDP value is added to Label, ensure that the text remains readable.
7. Adjust the mark size if necessary.

### Step 4: Format the Symbol Map

1. Select the Marks card and choose an appropriate color palette.
2. Adjust the size of the symbols.
3. Open **Map → Map Layers** if additional map formatting is needed.
4. Configure the background map and geographical details.
5. Use tooltips to display the country name and selected GDP value.
6. Rename the worksheet:

   `GDP Symbol Map`

**Expected result:** A symbol map displaying country locations using latitude and longitude, with country names and selected GDP values.

# Question 2: Create a Bar Chart to Compare Belgium's GDP from 2006 to 2026

## Objective

To compare Belgium's GDP values across the years 2006 to 2026 using a bar chart.

### Step 1: Filter the Required Years

1. Open a new worksheet.
2. Locate **Measure Names** in the Data pane.
3. Drag Measure Names to the **Filters** shelf.
4. In the filter dialog, select the GDP measures corresponding to the years 2006 through 2026.
5. Click **OK**.

**Important:** Select all 21 years, from 2006 through 2026 inclusive, if all are present in the dataset.

### Step 2: Filter the Country

1. Locate the Country field.
2. Drag Country to the **Filters** shelf.
3. Select `Belgium`.
4. Click **OK**.
5. Verify that the worksheet is restricted to Belgium.

### Step 3: Configure the Bar Chart

1. Drag **Measure Names** to the **Columns** shelf.
2. Drag **Measure Values** to the **Rows** shelf.
3. In the Measure Values card, retain only the GDP measures for the years 2006 through 2026.
4. Ensure that the chart uses the appropriate aggregation for the GDP fields.
5. On the Marks card, select **Bar** if Tableau does not select it automatically.

### Step 4: Format the Bar Chart

1. Turn on mark labels if required.
2. Format the GDP axis.
3. Add a descriptive title:

   `Belgium GDP Comparison (2006–2026)`

4. Adjust the bar colors.
5. Sort the year categories chronologically if necessary.
6. Resize the chart to display all years clearly.

**Expected result:** A bar chart comparing Belgium's GDP values for the selected years from 2006 through 2026.

# Question 3: Create a Pie Chart Showing GDP for Selected Countries in 2010

## Objective

To visualize the GDP values for India, Nepal, Romania, South Asia, and Singapore for the year 2010 using a pie chart.

### Step 1: Filter the Countries

1. Open a new worksheet.
2. Drag **Country** to the **Filters** shelf.
3. Select the following entries:
   - India
   - Nepal
   - Romania
   - South Asia
   - Singapore
4. Click **OK**.

### Step 2: Filter the Year

1. Drag **Measure Names** to the **Filters** shelf.
2. Select the measure corresponding to the year `2010`.
3. Click **OK**.
4. Verify that the worksheet contains only the selected countries and the 2010 GDP measure.

### Step 3: Select the Pie Chart

1. Locate the **Marks** card.
2. Open the mark-type dropdown.
3. Select **Pie** instead of Automatic.
4. Drag **Country** to **Color**.
5. Drag the 2010 GDP measure or the appropriate Measure Values field to **Angle**.
6. If you use Measure Values, ensure that only the 2010 GDP measure is included in the calculation.
7. Drag the GDP measure to **Label** if you want to display the values on the pie slices.

### Step 4: Display GDP Values and Percentages

1. Select the Marks card.
2. Click **Label**.
3. Enable **Show mark labels**.
4. Format the labels for readability.
5. If percentage contribution is required, use the appropriate table calculation for percent of total.
6. Verify that the chart contains five country or region categories, provided all are present in the dataset.

### Step 5: Format the Pie Chart

1. Choose different colors for the selected countries.
2. Adjust the size of the pie.
3. Add the title:

   `GDP Distribution of Selected Countries and Region (2010)`

4. Review the labels and tooltip values.

**Expected result:** A pie chart comparing the 2010 GDP values of India, Nepal, Romania, South Asia, and Singapore.

**Note:** South Asia is a geographical region rather than an individual country. Retain it as a separate category if it appears in the supplied dataset, as specified in the lab instructions.

# Question 4: Compare the GDP of Bhutan and Costa Rica

## Objective

To compare the GDP values of Bhutan and Costa Rica for the years 2016, 2017, and 2018.

### Step 1: Filter the Countries

1. Open a new worksheet.
2. Drag **Country** to the Filters shelf.
3. Select:
   - Bhutan
   - Costa Rica
4. Click **OK**.

### Step 2: Filter the Years

1. Drag **Measure Names** to the Filters shelf.
2. Select the GDP measures corresponding to:
   - 2016
   - 2017
   - 2018
3. Click **OK**.

### Step 3: Configure the Comparison Chart

1. Drag **Measure Names** to the **Columns** shelf.
2. Drag **Measure Values** to the **Rows** shelf.
3. Remove any measures that do not correspond to the selected years.
4. On the Marks card, select **Bar** or use the visualization type specified by your lab.
5. Drag **Country** to **Color**.

### Step 4: Format the Chart

1. Choose distinct colors for Bhutan and Costa Rica.
2. Add the title:

   `GDP Comparison: Bhutan vs Costa Rica (2016–2018)`

3. Enable labels if required.
4. Ensure that the year categories appear in chronological order.
5. Review the tooltip values for each country and year.

**Expected result:** A comparative chart displaying the GDP values of Bhutan and Costa Rica for 2016, 2017, and 2018.

# Question 5: Create a Scatter Plot or Circle View for Mexico, Algeria, Fiji, and Estonia from 2004 to 2006

## Objective

To visualize and compare GDP values for Mexico, Algeria, Fiji, and Estonia for the years 2004, 2005, and 2006 using a circle view.

### Step 1: Filter the Countries

1. Open a new worksheet.
2. Drag **Country** to the Filters shelf.
3. Select:
   - Mexico
   - Algeria
   - Fiji
   - Estonia
4. Click **OK**.

### Step 2: Filter the Years

1. Drag **Measure Names** to the Filters shelf.
2. Select the GDP measures for:
   - 2004
   - 2005
   - 2006
3. Click **OK**.

### Step 3: Configure the Circle View

1. Drag **Measure Names** to the **Columns** shelf.
2. Drag **Measure Values** to the **Rows** shelf.
3. Verify that only the GDP measures for 2004, 2005, and 2006 are included.
4. On the Marks card, select **Circle**.
5. Drag **Country** to **Color**.
6. Drag **Country** to **Label** if country names need to be displayed.
7. Drag Measure Values to **Size** if the circle sizes should represent GDP values.

### Step 4: Format the Circle View

1. Select an appropriate color palette.
2. Adjust circle sizes to avoid excessive overlap.
3. Add the title:

   `GDP Comparison of Selected Countries (2004–2006)`

4. Enable labels where useful.
5. Use tooltips to display the country, year, and GDP value.
6. Review the view to ensure that the selected countries and years are represented.

**Expected result:** A circle view comparing GDP values for Mexico, Algeria, Fiji, and Estonia over the years 2004, 2005, and 2006.

# 7. Formatting and Presentation

After completing all five visualizations, apply consistent formatting to improve readability.

1. Use meaningful worksheet titles.
2. Select appropriate color palettes.
3. Use readable font sizes for labels.
4. Format GDP values consistently.
5. Ensure that the years are displayed in chronological order.
6. Use tooltips to show additional information without overcrowding the charts.
7. Avoid unnecessary visual elements.
8. Verify that each visualization includes only the intended countries and years.

# 8. Summary of Visualizations

| Question | Visualization | Data Selection | Purpose |
|---|---|---|---|
| 1 | Symbol Map | Countries, latitude, longitude, selected GDP measure | Display geographical locations and GDP values |
| 2 | Bar Chart | Belgium, 2006–2026 | Compare Belgium's GDP across years |
| 3 | Pie Chart | India, Nepal, Romania, South Asia, Singapore; 2010 | Compare selected GDP values |
| 4 | Comparative Bar Chart | Bhutan and Costa Rica; 2016–2018 | Compare GDP between two countries |
| 5 | Circle View | Mexico, Algeria, Fiji, Estonia; 2004–2006 | Compare GDP values using circles |

# 9. Viva Questions and Answers

**1. What is GDP?**

GDP stands for Gross Domestic Product. It represents the monetary value of goods and services produced within a country during a specified period.

**2. What is Tableau?**

Tableau is a data visualization and business intelligence tool used to analyze data and create interactive charts, maps, and dashboards.

**3. What is a symbol map?**

A symbol map represents geographical locations using marks such as circles or symbols, often displaying additional information through color, size, and labels.

**4. What are latitude and longitude?**

Latitude identifies a location's position north or south of the Equator, while longitude identifies its position east or west of the Prime Meridian.

**5. What is the purpose of a bar chart?**

A bar chart compares numerical values across categories.

**6. What is a pie chart?**

A pie chart represents the relative contributions of categories as slices of a circle.

**7. What is the Marks card in Tableau?**

The Marks card controls visual properties such as mark type, color, size, label, detail, and tooltip.

**8. What is Measure Names?**

Measure Names is a Tableau-generated field containing the names of measures in the data source.

**9. What is Measure Values?**

Measure Values is a Tableau-generated field that contains the values of multiple measures, allowing them to be displayed together in a visualization.

**10. Why are filters used in Tableau?**

Filters restrict the data displayed in a worksheet to the required categories, countries, values, or years.

**11. What is a circle view?**

A circle view represents data using circles. Circle size, color, and position can be used to compare categories and numerical values.

**12. How can countries be compared across different years?**

Filter the required countries and years, then use Measure Names and Measure Values to display the selected GDP measures in a chart.

**13. Why is color useful in data visualization?**

Color distinguishes categories and helps users identify patterns and differences.

**14. What is the difference between a symbol map and a filled map?**

A symbol map displays marks at geographical locations, while a filled map colors geographical areas according to a measure or category.

**15. Why should GDP values be formatted consistently?**

Consistent formatting makes comparisons easier and reduces the risk of misinterpreting values.

# 10. Result

The GDP dataset was imported into Tableau and analyzed using five visualizations. A symbol map was created using latitude, longitude, and country names. A bar chart compared Belgium's GDP from 2006 to 2026. A pie chart represented the GDP values of India, Nepal, Romania, South Asia, and Singapore for 2010. A comparative chart displayed the GDP values of Bhutan and Costa Rica from 2016 to 2018. Finally, a circle view was created to compare Mexico, Algeria, Fiji, and Estonia from 2004 to 2006.

# 11. Conclusion

This experiment demonstrates how Tableau can be used to explore and compare GDP data across countries and years. Symbol maps provide geographical context, bar charts support year-wise comparison, pie charts show relative contributions, and circle views help visualize multiple categories. Filters, colors, labels, and tooltips improve the clarity and interpretability of the resulting visualizations.

**Author:** Iqra Farheen
