# Program 12: Analysis of Amazon Prime Dataset

## Aim
To analyze the Amazon Prime dataset using Microsoft Power BI and create visualizations to understand content distribution, release trends, popular genres, country-wise content, and movie or TV show descriptions.

## Software Requirements
- Microsoft Power BI Desktop
- Amazon Prime Titles CSV Dataset

## Objectives
1. Create a donut chart to display the percentage of movies and TV shows.
2. Create an area chart to show content by release year and type.
3. Create a horizontal bar chart to display the Top 10 genres.
4. Create a map to display the total number of shows by country.
5. Create a table to display movie or TV show descriptions.
6. Build an interactive dashboard.

---

## Procedure

### Step 1: Import the Amazon Prime Dataset
1. Open Microsoft Power BI Desktop.
2. Select **Home → Get Data → Text/CSV**.
3. Browse and select the Amazon Prime titles CSV dataset.
4. Preview the data and select **Transform Data**.

### Step 2: Transform and Clean the Data
1. In Power Query Editor, inspect the dataset.
2. Remove blank and null values where necessary.
3. Remove columns that are not required for analysis.
4. Ensure the dataset contains the required fields, such as `Type`, `Title`, `Release Year`, `Genre`, `Country`, and `Description`.
5. Rename columns where necessary, such as renaming the listed genre column to `Genre`.
6. Check the data types of the columns.
7. Select **Close & Apply** to load the cleaned data into Power BI.

---

## i) Create a Donut Chart to Show the Percentage of Movies and TV Shows

### Steps
1. Select the **Donut Chart** visual from the Visualizations pane.
2. Drag the `Type` field to **Legend**.
3. Drag the `Title` field to **Values**.
4. Set the aggregation to **Count**.
5. Ensure that the chart includes the Movie and TV Show categories.
6. Open the Format pane and enable data labels.
7. Configure the labels to display percentages.
8. Add a suitable chart title.

**Chart title:** Percentage of Movies and TV Shows

**Result:** The donut chart displays the percentage distribution of movies and TV shows in the dataset.

---

## ii) Create an Area Chart to Show Content by Release Year and Type

### Steps
1. Select the **Area Chart** visual.
2. Drag the `Release Year` field to the **X-axis**.
3. Drag the `Type` field to **Legend**.
4. Drag the `Title` field to the **Y-axis** and set its aggregation to **Count**.
5. Ensure that the release year is treated as a numerical or categorical year, as appropriate.
6. Use filters to include the required content types.
7. Format the chart and add a suitable title.

**Chart title:** Shows by Release Year and Type

**Result:** The area chart displays the distribution of movies and TV shows across release years.

---

## iii) Create a Horizontal Bar Chart to Show the Top 10 Genres

### Steps
1. Select a **Clustered Bar Chart** from the Visualizations pane.
2. Drag the `Genre` field to the **Y-axis**.
3. Drag the `Title` field to the **X-axis** and set its aggregation to **Count**.
4. Open the Filters pane and select the `Genre` field.
5. Change the filter type to **Top N**.
6. Enter `10` in the Top N field.
7. Under **By value**, add the count of titles.
8. Select **Apply filter**.
9. Sort the chart by title count in descending order.
10. Add data labels and a suitable title.

**Chart title:** Top 10 Genres on Amazon Prime

**Result:** The horizontal bar chart displays the ten genres with the highest content counts.

**Note:** If a title belongs to multiple genres in a single text field, the genre data may need to be split into separate rows to count each genre accurately.

---

## iv) Create a Map to Display Total Shows by Country

### Step 1: Create a Measure

Select **Modeling → New measure** and enter the following DAX formula:

```dax
Count ShowID =
COUNT('amazon_prime_titles'[release_year])
```

This follows the measure provided in the lab instructions. It counts nonblank release-year values rather than show IDs. If the dataset contains a unique, nonblank `show_id` for each title, the following measure is more appropriate for counting shows:

```dax
Total Shows =
DISTINCTCOUNT('amazon_prime_titles'[show_id])
```

### Step 2: Create the Map
1. Select the **Filled Map** visual, if available.
2. Drag the `Country` field to **Location**.
3. Drag the `Total Shows` measure to the appropriate color saturation or values field supported by the selected map visual.
4. If a country contains multiple values in one cell, clean and split the country data into separate rows in Power Query for accurate country-level counts.
5. Format the map and add a suitable title.

**Chart title:** Total Shows by Country

**Result:** The map displays the number of shows associated with each country.

---

## v) Create a Table to Show Movie or TV Show Descriptions

### Steps
1. Select the **Table** visual from the Visualizations pane.
2. Add the `Title` field to the table.
3. Add the `Description` field to the table.
4. Adjust column widths and text formatting so the descriptions are readable.
5. Add a **Slicer** visual to enable searching or filtering by title.
6. Drag the `Title` field into the slicer.
7. Use the slicer to select a movie or TV show and view its description.

**Visual title:** Movie and TV Show Descriptions

**Result:** The table displays titles and their descriptions, with the option to filter by title.

---

## vi) Build an Interactive Dashboard

### Steps
1. Arrange the donut chart, area chart, Top 10 genres bar chart, country map, and description table on the report canvas.
2. Add KPI cards if required to summarize the total number of titles, movies, and TV shows.
3. Add slicers for relevant fields, such as `Type`, `Release Year`, `Country`, and `Genre`.
4. Resize and align the visuals to create a clear layout.
5. Add a dashboard title, such as **Amazon Prime Content Analysis**.
6. Use consistent colors, fonts, and formatting.
7. Test the slicers and visual interactions to ensure that selecting a category filters the relevant visuals.
8. Save the Power BI report as a `.pbix` file.

**Result:** An interactive dashboard is created to explore Amazon Prime content by type, release year, genre, country, and description.

---

## Important Notes
- Ensure that the table and column names used in DAX match the dataset.
- Use **Count of Title** or a distinct count of `show_id` to count content records appropriately.
- The `Country` and `Genre` columns may contain multiple comma-separated values. For accurate country-wise and genre-wise analysis, consider transforming these columns into separate rows.
- Some map visuals may require location categorization or map settings to be enabled in Power BI.
- Use filters and slicers to make the report interactive.

## Conclusion
The Amazon Prime dataset was analyzed using Microsoft Power BI. Donut, area, horizontal bar, map, and table visuals were created to examine the distribution of movies and TV shows, release-year trends, Top 10 genres, country-wise content, and content descriptions. These visualizations were combined into an interactive dashboard for easier exploration and analysis.

