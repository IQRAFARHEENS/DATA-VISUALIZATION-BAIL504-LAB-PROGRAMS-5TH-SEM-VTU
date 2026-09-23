# Program 4: Dashboard Design and Storytelling Using Tableau

**Dashboard Components, Worksheet Containers, Action Filters & Tableau Storytelling**

**Dataset used:** `GDP by Country per Year_data.xlsx`

---

## 📌 Aim

To design an interactive dashboard and create a meaningful data story using Tableau Public by working with dashboard components, worksheet containers, action filters, and Tableau storytelling techniques.

---

## 📚 Program Overview

This program demonstrates:

- Creating worksheets for data visualization
- Combining worksheets into a dashboard
- Using dashboard components and containers
- Creating interactive Action Filters
- Understanding different types of Tableau actions
- Creating a Tableau Story
- Using story points and captions
- Applying the Tailoring-In storytelling technique
- Adding text to highlight important observations

---

## 🎥 Screen Recording & Materials

The complete screen recording and supporting materials for Program 4 are available in the Google Drive folder.

👉 [View Program 4 Screen Recording & Materials](PASTE_GOOGLE_DRIVE_LINK_HERE)

---

## 🗂️ Dataset Used

**Dataset:** `GDP by Country per Year_data.xlsx`

The dataset contains country-wise GDP Growth information across different years.

### Important Fields

| Field | Description |
|---|---|
| Country | Name of the country |
| Year | Year of observation |
| GDP Growth | GDP growth value for the country and year |

---

## 🔌 1. Connecting to the Data Source

1. Open **Tableau Public**.
2. Select **Microsoft Excel** from the Connect section.
3. Browse to the dataset location.
4. Select `GDP by Country per Year_data.xlsx`.
5. Click **Open**.
6. Tableau loads the available fields.

---

## 🗺️ 2. Creating the GDP Growth Map

A geographical map is created to visualize GDP Growth across countries.

### Steps

1. Create a new worksheet.
2. Rename it **GDP Growth Map – 2016**.
3. Drag **Country** to the view.
4. Drag **GDP Growth** to **Color**.
5. Drag **Year** to **Filters**.
6. Select **2016**.

### Result

The map displays GDP Growth across different countries for the year 2016.

---

## 📈 3. Creating the GDP Growth Trend

A line chart is created to display GDP Growth over time.

### Steps

1. Create a new worksheet.
2. Rename it **GDP Growth Trend**.
3. Drag **Year** to **Columns**.
4. Drag **GDP Growth** to **Rows**.
5. Drag **Country** to **Color**.
6. Select **Line** from the Marks card.

### Result

The visualization displays the GDP Growth trend of different countries over time.

---

## 🖥️ 4. Creating the Dashboard

The map and line chart are combined into an interactive dashboard.

### Steps

1. Create a **New Dashboard**.
2. Rename it **GDP Growth Dashboard**.
3. Add the following worksheets:
   - GDP Growth Map – 2016
   - GDP Growth Trend
4. Arrange the worksheets using dashboard containers.
5. Enable **Show Dashboard Title**.
6. Set the dashboard title to **GDP Growth Dashboard**.

---

## 📦 5. Using Dashboard Containers

Dashboard containers help organize and align worksheets and other dashboard objects.

### Horizontal Container

Places dashboard objects from left to right.

### Vertical Container

Places dashboard objects from top to bottom.

Containers are used to maintain proper alignment and organization of dashboard components.

---

## 🔄 6. Creating an Action Filter

An Action Filter is created to make the dashboard interactive.

### Configuration

**Action Name:** `Country Selection Filter`

**Source Sheet:** `GDP Growth Trend`

**Target Sheet:** `GDP Growth Map – 2016`

**Action:** Filter

**Field Mapping:**

`Country → Country`

**Clearing the Selection:** Show all values

### Interaction

Selecting a country from the GDP Growth Trend interacts with the GDP Growth Map.

For example:

**Select India → Map responds to the selected country**

---

## 🧩 7. Types of Tableau Actions

Tableau provides different types of actions:

1. **Filter Action** – Filters another worksheet based on user interaction.
2. **Highlight Action** – Highlights related marks.
3. **URL Action** – Opens a specified web page.
4. **Go to Sheet Action** – Navigates to another worksheet, dashboard, or story.
5. **Parameter Action** – Changes a parameter value through interaction.
6. **Set Action** – Changes the members of a Tableau set.

---

## 📖 8. Creating a Tableau Story

A Tableau Story is created using multiple story points to communicate a data narrative.

### Story Name

**GDP Growth Story**

The **Tailoring-In** storytelling approach is used.

### Story Flow

```text
Global View
     ↓
Specific Country
     ↓
Detailed Country Trend
````

---

## 🌍 9. Story Point 1 – Global View

The first story point provides an overall view of GDP Growth.

**Worksheet:** `GDP Growth Map – 2016`

**Caption:**
`Global GDP Growth by Country – 2016`

---

## 🇮🇳 10. Story Point 2 – India Selected

The second story point focuses on India.

### Steps

1. Duplicate the first story point.
2. Select **India** on the map.
3. Click **Update** to save the selected state.

**Caption:**
`India – Selected Country`

---

## 📈 11. Story Point 3 – India GDP Growth Trend

A detailed trend for India is created.

**Worksheet:** `India GDP Growth Trend`

### Steps

1. Duplicate the GDP Growth Trend worksheet.
2. Rename it **India GDP Growth Trend**.
3. Apply a **Country** filter.
4. Select **India**.
5. Add the worksheet to the third story point.

**Caption:**
`India GDP Growth Trend (2000–2020)`

---

## 📝 12. Adding Text to the Story

Text boxes can be used to highlight important observations.

Example observation:

> India's GDP Growth shows significant variation between 2000 and 2020, including a sharp decline in 2020.

---

## 🔗 13. Final Story Flow

The final Tableau Story follows the Tailoring-In approach:

```text
Global GDP Growth by Country – 2016
                 ↓
          India – Selected Country
                 ↓
       India GDP Growth Trend
              (2000–2020)
```

The story progresses from:

**Global → Specific → Detailed**

---

## 📸 14. Screenshots

The following screenshots can be included to document the major stages of the program:

```text
screenshots/
│
├── 01-gdp-growth-map-2016.png
├── 02-gdp-growth-trend.png
├── 03-dashboard.png
├── 04-action-filter.png
├── 05-action-filter-india.png
├── 06-story-global-view.png
├── 07-story-india-selected.png
└── 08-story-india-trend.png
```

---

## 📁 Repository Structure

```text
Program-04-Dashboard-Creation/
│
├── README.md
├── GDP by Country per Year_data.xlsx
├── Program4_Tableau_Dashboard.twbx
│
└── screenshots/
    ├── 01-gdp-growth-map-2016.png
    ├── 02-gdp-growth-trend.png
    ├── 03-dashboard.png
    ├── 04-action-filter.png
    ├── 05-action-filter-india.png
    ├── 06-story-global-view.png
    ├── 07-story-india-selected.png
    └── 08-story-india-trend.png
```

---

## 🎯 Learning Outcomes

After completing this program, the learner should be able to:

* Create multiple worksheets in Tableau
* Create geographical visualizations
* Create time-series line charts
* Combine worksheets into a dashboard
* Use dashboard containers
* Create Action Filters
* Understand different Tableau actions
* Create interactive dashboards
* Create Tableau Stories
* Create and navigate story points
* Add captions and text boxes
* Apply the Tailoring-In storytelling technique
* Present data as a meaningful visual narrative

---

## ✅ Result

The GDP dataset was successfully connected to Tableau Public.

The following visualizations were created:

* **GDP Growth Map – 2016**
* **GDP Growth Trend**
* **India GDP Growth Trend**

An interactive dashboard named **GDP Growth Dashboard** was successfully created by combining the map and line chart.

A **Country Selection Filter** was implemented to enable interaction between the GDP Growth Trend and GDP Growth Map.

A Tableau Story named **GDP Growth Story** was created using three story points:

1. Global GDP Growth by Country – 2016
2. India – Selected Country
3. India GDP Growth Trend (2000–2020)

The story follows the **Tailoring-In** approach, progressing from a global view to a specific country and finally to its detailed historical trend.

---

## 🏁 Conclusion

This program provided practical experience in creating interactive Tableau dashboards and data-driven stories.

The program demonstrated the use of worksheets, dashboard components, containers, Action Filters, interactive visualizations, and Tableau storytelling techniques to communicate data effectively.

---


## 👩‍💻 Author

**Iqra Farheen**


This version will look much more like your **Program 3 README**: clean headings → short explanation → steps → result → conclusion, instead of the current very long 500-line document.
