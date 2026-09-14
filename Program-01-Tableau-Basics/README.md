# Program 1: Getting Started with Tableau
### Tableau Workspace, Terminologies & Basic Functionalities

**Dataset used:** `vgsales.csv` 

---

## 📌 Aim

To get familiar with the Tableau Workspace, understand core Tableau terminologies, and practice basic functionalities such as building charts, sorting, filtering, creating animated views, and creating dashboards using the `vgsales.csv` dataset.

---

# 🎥 1. Program Materials & Screen Recordings

All the materials related to this program, including the **screen recordings, reference materials, and supporting files**, are available in the Google Drive folder below.

👉 **[View Program 1 – All Materials & Screen Recordings](https://drive.google.com/drive/u/0/folders/1XpWuH_b8BPnV07sqv0gq0rjyFSUe7hXE)**

The folder contains the resources used to demonstrate the complete execution of this program.

---

# 🗂️ 2. Tableau Workspace — Key Components

Before starting, identify the following components in Tableau:

| # | Component | Description |
|---|-----------|-------------|
| 1 | **Start Page** | Used to connect to data sources and access Tableau workbooks. |
| 2 | **Data Pane** | Lists dimensions, measures, calculated fields, parameters, and sets. |
| 3 | **Analytics Pane** | Provides options such as reference lines, trend lines, forecasts, totals, and box plots. |
| 4 | **Workbook Name** | Displays the name of the current Tableau workbook. |
| 5 | **View Cards / Marks Card** | Used to control the appearance and formatting of marks. |
| 6 | **Toolbar** | Provides quick access to commands such as Undo, Redo, Save, Swap, and other functions. |
| 7 | **Worksheet / View** | The main area where visualizations are created. |
| 8 | **Go to Data Source** | Takes you back to the data source page. |
| 9 | **Worksheet Tabs** | Used to switch between worksheets, dashboards, and stories. |
| 10 | **New Worksheet / Dashboard / Story** | Used to create new Tableau views. |
| 11 | **Status Bar** | Displays information about the current view and selected marks. |

---

# 🧩 3. Tableau Terminologies

## 3.1 Dimensions

**Dimensions** are qualitative or descriptive fields used to categorize and group data.

Examples from `vgsales.csv`:

- `Platform`
- `Genre`
- `Publisher`

For example, `Genre` can be used to group video game sales into categories such as Action, Sports, Shooter, and Role-Playing.

---

## 3.2 Measures

**Measures** are quantitative fields that can be aggregated or used for calculations.

Examples from `vgsales.csv`:

- `Global_Sales`
- `NA_Sales`
- `EU_Sales`
- `JP_Sales`
- `Other_Sales`
- `Year`

For example, `Global_Sales` can be aggregated using `SUM` to calculate total global sales.

> **Note:** `Year` is technically treated as a measure based on the dataset, but it can also be used as a discrete field for grouping and time-based analysis.

---

## 3.3 Rows and Columns Shelves

The **Rows** and **Columns** shelves determine the basic structure of a visualization.

For example:

```text
Columns → Genre
Rows → Global_Sales
````

This creates a visualization showing global sales for each genre.

---

## 3.4 Marks

The **Marks card** controls how data appears in the visualization.

It can be used to control:

* Color
* Size
* Label
* Shape
* Detail
* Tooltip

For example, `Genre` can be placed on **Color** to display each genre using a different color.

---

## 3.5 Filters

**Filters** restrict the data displayed in a visualization.

For example:

```text
Year → Filters
```

can be used to display only selected years, such as 2000–2016.

---

## 3.6 Pages Shelf

The **Pages shelf** can be used to divide a visualization into separate views based on a field and can provide an animation/playback experience.

For example:

```text
Year → Pages
```

can be used to observe how sales change year by year.

---

# 🚀 4. Connecting to the Data Source

## Step 1: Open Tableau

1. Open **Tableau**.
2. On the **Start Page**, locate the **Connect** section.

---

## Step 2: Connect to the CSV File

Under **Connect**, select:

```text
To a File → Text File
```

---

## Step 3: Select the Dataset

Browse to the location where `vgsales.csv` is stored.

Select:

```text
vgsales.csv
```

Click **Open**.

---

## Step 4: Verify the Data Preview

Tableau displays a preview of the dataset.

Check:

* Column names
* Data types
* Dimensions
* Measures

If necessary, rename columns or modify their data types.

---

## Step 5: Open the Worksheet

Click **Sheet 1** at the bottom of Tableau.

This opens the worksheet where the first visualization will be created.

**Screenshot:** `03-vgsales-data-preview.png`

---

# 📊 5. Exploring Dimensions and Measures

In the **Data Pane**, identify the available dimensions and measures.

### Dimensions

```text
Platform
Genre
Publisher
```

### Measures

```text
Year
NA_Sales
EU_Sales
JP_Sales
Other_Sales
Global_Sales
```

The Data Pane is used throughout the program to drag fields onto shelves and the Marks card.

---

# 📈 6. Creating a Basic Visualization

## Bar Chart — Global Sales by Genre

The first visualization displays global video game sales by genre.

### Steps

1. Open **Sheet 1**.
2. Drag `Genre` to the **Columns** shelf.
3. Drag `Global_Sales` to the **Rows** shelf.
4. Tableau generates a bar chart.

The basic configuration is:

```text
Columns → Genre
Rows → SUM(Global_Sales)
```

If necessary:

1. Right-click `Global_Sales`.
2. Select **Measure**.
3. Select **Sum**.

Rename the worksheet:

```text
Global Sales by Genre
```

**Screenshot:** `04-global-sales-by-genre-initial.png`

---

# 🔽 7. Sorting the Visualization

The bar chart can be sorted to display genres according to their global sales.

### Steps

1. Select the `Global_Sales` axis or use the sort option.
2. Select **Sort Descending**.
3. Tableau rearranges the genres according to their sales values.

The resulting chart displays higher-sales genres before lower-sales genres.

**Screenshots:**

```text
05-global-sales-by-genre-sorted.png
06-sort-genre-by-global-sales.png
```

---

# 🔎 8. Filtering the Visualization

A filter can be applied to restrict the visualization to a particular range of years.

### Steps

1. Drag `Year` to the **Filters** shelf.
2. Select **Range of Years**.
3. Enter the required range.

Example:

```text
2000 → 2016
```

4. Click **OK**.

The visualization now represents the selected year range.

**Screenshot:** `07-year-filter-dialog.png`

The resulting filtered visualization can be saved as:

```text
08-global-sales-by-genre-filtered.png
```

---

# ▶️ 9. Creating a Dynamic View Using the Pages Shelf

The `Pages` shelf can be used to observe how the visualization changes over time.

### Steps

1. Drag `Year` to the **Pages** shelf.
2. Tableau displays a playback control.
3. Click **Play**.
4. Observe the changes in global sales by genre year by year.

The Pages shelf therefore provides a dynamic way to examine changes over time.

---

# 📉 10. Creating Global Sales Trend by Year

A second worksheet is created to visualize the trend in global sales over time.

## Step 1: Create a New Worksheet

Click the **New Worksheet** icon.

Rename the worksheet:

```text
Global Sales Trend by Year
```

---

## Step 2: Add Year to Columns

Drag:

```text
Year → Columns
```

This places the years along the horizontal axis.

---

## Step 3: Add Global Sales to Rows

Drag:

```text
Global_Sales → Rows
```

The basic configuration becomes:

```text
Columns → Year
Rows → SUM(Global_Sales)
```

---

## Step 4: Convert to a Line Chart

1. Open **Show Me**.
2. Select **Line Chart**.

The visualization now displays the trend in global sales over time.

---

## Step 5: Add Genre to Color

1. Locate `Genre`.
2. Drag `Genre` to the **Color** option on the Marks card.

Tableau creates separate colored lines for the different genres.

This allows the sales trends of different genres to be compared over time.

**Screenshot:** `09-global-sales-trend-by-year.png`

---

# 🖥️ 11. Creating the Dashboard

The two worksheets can be combined into a single dashboard.

### Worksheets used

```text
Global Sales by Genre
Global Sales Trend by Year
```

---

## Step 1: Create a New Dashboard

Click the **New Dashboard** icon/tab.

---

## Step 2: Set Dashboard Size

Under **Size**, select:

```text
Automatic
```

This allows the dashboard to adjust to the available screen size.

---

## Step 3: Add the Worksheets

From the **Sheets** section on the left, drag:

```text
Global Sales by Genre
```

and

```text
Global Sales Trend by Year
```

onto the dashboard.

---

## Step 4: Arrange the Visualizations

Arrange the visualizations neatly using the dashboard layout options.

The charts can be:

* Placed side by side
* Stacked vertically
* Arranged using horizontal/vertical containers

---

## Step 5: Add a Dashboard Title

Optionally add a **Text** object.

Example:

```text
Video Game Sales Dashboard
```

---

## Step 6: Apply Dashboard Filtering

A bar from the `Global Sales by Genre` chart can be selected to filter or highlight the corresponding information in the trend visualization.

This allows the dashboard to provide an interactive analysis experience.

**Screenshot:** `10-program-1-dashboard.png`

---

# 💾 12. Saving the Tableau Workbook

After completing the visualizations and dashboard:

1. Go to **File → Save As**.
2. Save the workbook in the project folder.
3. Use the packaged workbook format if you want the data source bundled with the workbook.

Recommended filename:

```text
Program1_Tableau_Basics.twbx
```

The `.twbx` format packages the Tableau workbook and supporting data together.

---

# 📸 13. Screenshots

The screenshots document the major stages of the program.

Recommended structure:

```text
screenshots/
│
├── 01-tableau-start-page.png
├── 02-select-vgsales-dataset.png
├── 03-vgsales-data-preview.png
├── 04-global-sales-by-genre-initial.png
├── 05-global-sales-by-genre-sorted.png
├── 06-sort-genre-by-global-sales.png
├── 07-year-filter-dialog.png
├── 08-global-sales-by-genre-filtered.png
├── 09-global-sales-trend-by-year.png
└── 10-program-1-dashboard.png
```

Each screenshot represents an important stage of the implementation.

---

# 🎥 14. Screen Recording & Supporting Materials

The complete **screen recordings, reference materials, and supporting resources** for Program 1 are available in the Google Drive folder.

👉 **[View All Program 1 Materials & Screen Recordings](https://drive.google.com/drive/u/0/folders/1XpWuH_b8BPnV07sqv0gq0rjyFSUe7hXE)**

The recordings provide a practical demonstration of:

* Connecting `vgsales.csv` to Tableau
* Exploring dimensions and measures
* Creating the bar chart
* Sorting the visualization
* Applying the Year filter
* Using the Pages shelf
* Creating the yearly sales trend
* Applying Genre to Color
* Creating the dashboard

---

# 📁 15. Repository Structure

The Program 1 folder can be organized as follows:

```text
Program-01-Getting-Started-with-Tableau/
│
├── README.md
│
├── vgsales.csv
│
├── Program1_Tableau_Basics.twbx
│
└── screenshots/
    │
    ├── 01-tableau-start-page.png
    ├── 02-select-vgsales-dataset.png
    ├── 03-vgsales-data-preview.png
    ├── 04-global-sales-by-genre-initial.png
    ├── 05-global-sales-by-genre-sorted.png
    ├── 06-sort-genre-by-global-sales.png
    ├── 07-year-filter-dialog.png
    ├── 08-global-sales-by-genre-filtered.png
    ├── 09-global-sales-trend-by-year.png
    └── 10-program-1-dashboard.png
```

---

# 🎯 16. Learning Outcomes

After completing this program, the learner should be able to:

* Identify the major components of the Tableau workspace.
* Connect a CSV data source to Tableau.
* Understand **Dimensions** and **Measures**.
* Use the **Rows** and **Columns** shelves.
* Understand and use the **Marks card**.
* Create a **bar chart** using Tableau.
* Sort a visualization in descending order.
* Apply a **Year filter**.
* Use the **Pages shelf** to create a dynamic view.
* Create a **line chart** for yearly sales trends.
* Use `Genre` on **Color** to compare multiple trends.
* Combine multiple worksheets into a **Dashboard**.
* Configure the dashboard size using **Automatic**.
* Save a Tableau workbook in packaged workbook format.

---

# ✅ 17. Result

The `vgsales.csv` dataset was successfully connected to Tableau.


