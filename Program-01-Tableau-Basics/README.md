# Program 1: Getting Started with Tableau
### Tableau Workspace, Terminologies & Basic Functionalities

**Dataset used:** `vgsales.csv` (Video Game Sales dataset)

---

## 📌 Aim

To get familiar with the Tableau Workspace, understand core Tableau terminologies, and practice basic functionalities such as building charts, sorting, filtering, and creating dashboards using the `vgsales.csv` dataset.

---

## 🗂️ 1. Tableau Workspace — Key Components

Before starting, take a moment to identify these on your screen once Tableau is open:

| # | Component | Description |
|---|-----------|-------------|
| 1 | **Start Page** | Toggle between the active sheet and the Desktop Start Page. |
| 2 | **Data Pane** | Lists dimensions and measures from your data source; also shows calculated fields, parameters, and sets. |
| 3 | **Analytics Pane** | Lets you add reference lines, forecasts, trend lines, totals, and box plots. |
| 4 | **Workbook Name** | Displays the file name of the current workbook. |
| 5 | **View Cards** | Used to modify/format the worksheet (Marks card, shelves, etc.). |
| 6 | **Toolbar Icons** | Quick access to common features (Undo, Redo, Save, Swap, etc.). |
| 7 | **Worksheet/View** | The main canvas where visualizations are built. |
| 8 | **Go to Data Source** | Returns you to the data source specification page. |
| 9 | **Worksheet Tabs** | Click to switch between worksheets, dashboards, or stories. |
| 10 | **New Worksheet/Dashboard/Story Tabs** | Buttons to create a new worksheet, dashboard, or story. |
| 11 | **Status Bar** | Shows information about the fields and marks used in the current view. |

---

## 🧩 2. Tableau Terminologies

| Term | Meaning | Example (from `vgsales.csv`) |
|------|---------|-------------------------------|
| **Dimensions** | Qualitative, descriptive fields | `Platform`, `Genre`, `Publisher` |
| **Measures** | Quantitative fields used for aggregation/calculation | `Global_Sales`, `NA_Sales`, `Year` |
| **Rows/Columns Shelf** | Where you drag fields to define the structure of the viz | — |
| **Marks** | Controls appearance of data points (shape, size, color, label) | Bar, Circle, etc. |
| **Filters** | Used to restrict the data shown in the view | Filter by `Year` |
| **Pages Shelf** | Used to animate/segment views by category over a field | Animate by `Year` |

---

## 🚀 3. Step-by-Step Procedure

### Step 1: Connect to the Data Source

1. Open **Tableau Desktop.{Reference 1-tableau-start-page.png}**
2. On the **Start Page**, under **Connect**, click **To a File → Text File**.
3. Browse to the location of `vgsales.csv` and click **Open**.**{Reference 2-Select-vgsales-dataset.png}**
4. Tableau will show a **data preview**. Verify the column names and data types; rename columns if needed.**{Reference 3-vgsales-data-preview.png}**
5. Click the **Sheet 1** tab at the bottom of the screen to move to your first worksheet.

> 💡 **Tip:** Check that fields like `Global_Sales`, `NA_Sales`, `EU_Sales`, `JP_Sales` are recognized as **Measures**, and fields like `Platform`, `Genre`, `Publisher` are recognized as **Dimensions**. Tableau usually does this automatically based on data type.

---

### Step 2: Explore Dimensions and Measures

1. In the **Data Pane** (left side), scroll through the **Dimensions** section (blue fields) — you should see `Name`, `Platform`, `Genre`, `Publisher`.
2. Scroll through the **Measures** section (green fields) — you should see `Year`, `NA_Sales`, `EU_Sales`, `JP_Sales`, `Other_Sales`, `Global_Sales`.
3. Note: `Year` is technically a measure but is often treated as a discrete dimension (blue) when used for grouping — you'll see this in Step 5.

---

### Step 3: Build a Basic Visualization — Bar Chart of Global Sales by Genre

1. On **Sheet 1**, drag **Genre** from the Data Pane onto the **Columns** shelf.
2. Drag **Global_Sales** onto the **Rows** shelf.
3. Tableau will automatically generate a **bar chart**.
4. If the values don't look aggregated correctly:
   - Right-click **Global_Sales** (in the Rows shelf or Data Pane) → **Measure** → select **Sum**.
5. Rename the sheet tab (bottom) to **"Global Sales by Genre"** for clarity.**{Reference 4-global-sales-by-genre-initial.png and 8-global-sales-by-genre-filtered.png }**

---

### Step 4: Sort the Bar Chart

1. Click on the **Global_Sales axis** (or the small sort icon that appears on the toolbar/axis).
2. Choose **Sort Descending** so genres with the highest sales appear first.
3. Observe how Action/Sports genres typically top the chart. **{Reference 5-global-sales-by-genre-sorted.png and 6-sort-genre-by-global-sales.png}**

---

### Step 5: Apply a Filter

1. Drag **Year** onto the **Filters** shelf.
2. In the dialog box that appears, choose **Range of Years** (or select individual years).
3. Set the range, e.g., **2000 to 2016**, and click **OK**.
4. The bar chart will now only reflect data from the selected year range. **{Reference 7-year-filter-dialog.png)**

**Optional — Create a Dynamic Animated View:**
1. Drag **Year** onto the **Pages** shelf as well.
2. A playback control will appear on the right side of the screen.
3. Click the **Play** button to animate how `Global_Sales by Genre` changes year by year.

---

### Step 6: Create a Second Worksheet — Global Sales Trend by Year

1. Click the **New Worksheet** icon at the bottom of the screen.
2. Rename this sheet **"Global Sales Trend by Year"**.
3. Drag **Year** onto the **Columns** shelf.
4. Drag **Global_Sales** onto the **Rows** shelf.
5. Tableau may show a bar chart by default — click the **Show Me** panel (top-right) and select the **Line Chart** icon to convert it into a line chart.
6. Drag **Genre** onto the **Marks card** (specifically onto the **Color** button in the Marks card).
7. This will split the single trend line into multiple colored lines — one per genre — letting you compare trends across genres over the years.
**{Reference 9-global-sales-trend-by-year.png}**
---

### Step 7: Build the Dashboard

1. Click the **New Dashboard** tab/icon at the bottom of the screen.
2. On the left, under **Size**, change it from a fixed size to **Automatic** (this lets the dashboard scale to fit the browser/screen).
3. From the **Sheets list** on the left panel, drag:
   - **"Global Sales by Genre"** (bar chart) onto the dashboard canvas.
   - **"Global Sales Trend by Year"** (line chart) onto the dashboard canvas.
4. Arrange the two charts side by side or stacked, using the **layout containers** (horizontal/vertical) to keep them neatly aligned.
5. Resize each worksheet within the dashboard by dragging its borders.
6. (Optional) Add a **Text object** as a title, e.g., "Video Game Sales Dashboard," using **Objects → Text** from the left panel.
7. (Optional) Use dashboard **filter actions**: click a bar in the "Global Sales by Genre" chart → use the filter icon that appears → this can dynamically filter the line chart to highlight the selected genre's trend.
**{Reference 10-program-1-dashboard.png}**
---

### Step 8: Save Your Work

1. Go to **File → Save As**.
2. Name the workbook, e.g., `Program1_Tableau_Basics.twbx` (use the **Packaged Workbook** format `.twbx` so the data is bundled with the file — important when uploading to GitHub, since `.twb` alone won't include the data source).
3. Save it inside your project folder before committing to Git.

---

## 📁 4. Suggested Repository Structure

```
Program1-Tableau-Basics/
│
├── README.md                     ← this file
├── vgsales.csv                   ← dataset used
├── Program1_Tableau_Basics.twbx  ← packaged Tableau workbook
└── screenshots/
├── 1-tableau-start-page.png
├── 2-select-vgsales-dataset.png
├── 3-vgsales-data-preview.png
├── 4-global-sales-by-genre-initial.png
├── 5-global-sales-by-genre-sorted.png
├── 6-sort-genre-by-global-sales.png
├── 7-year-filter-dialog.png
├── 8-global-sales-by-genre-filtered.png
├── 9-global-sales-trend-by-year.png
└── 10-program-1-dashboard.png
```

---

## ✅ 5. Expected Outcomes

By completing this program, you should be able to:
- Identify and use all major components of the Tableau workspace.
- Distinguish between **Dimensions** and **Measures**.
- Build a basic **bar chart** and a **line chart**.
- Apply **sorting** and **filters** to refine a view.
- Use the **Pages shelf** to animate a view over time.
- Combine multiple worksheets into a single **Dashboard**.

---

