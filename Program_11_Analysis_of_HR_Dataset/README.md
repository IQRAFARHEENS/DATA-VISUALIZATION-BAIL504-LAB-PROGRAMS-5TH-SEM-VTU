# Program 11: Analysis of HR Dataset

## Aim
To analyze an HR dataset using Microsoft Power BI and create visualizations to understand employee count, attrition, age distribution, job satisfaction, education-wise attrition, and gender-wise attrition rates.

## Software Requirements
- Microsoft Power BI Desktop
- HR Dataset (Excel or CSV format)

## Objectives
1. Create KPI cards to display employee count, attrition count, attrition rate, active employees, and average age.
2. Create a lollipop chart to show attrition rate by gender.
3. Create a pie chart to show department-wise attrition percentage.
4. Create a bar chart to display employee count by age group.
5. Create a highlight table to show job satisfaction ratings for each job role based on employee count.
6. Create a horizontal bar chart to display education-field-wise attrition count.
7. Create multiple donut charts to show attrition rate by gender across different age groups.

---

## Procedure

### i) Create KPI Cards

KPI cards are used to display important HR metrics, such as employee count, attrition count, attrition rate, active employees, and average age.

#### Step 1: Create Employee Count Measure

```dax
Employee Count = COUNT('HR'[EmployeeNumber])
```

1. Open Power BI Desktop and load the HR dataset.
2. Select **Modeling → New measure**.
3. Enter the above DAX formula.
4. Add a Card visual and drag the `Employee Count` measure into it.

#### Step 2: Create Attrition Count Measure

```dax
Attrition Count =
COUNTROWS(
    FILTER('HR', 'HR'[Attrition] = "Yes")
)
```

1. Create a new measure using the above formula.
2. Add another Card visual.
3. Drag the `Attrition Count` measure into the card.

#### Step 3: Create Attrition Rate Measure

```dax
Attrition Rate =
DIVIDE([Attrition Count], [Employee Count], 0) * 100
```

1. Create a new measure.
2. Add a Card visual.
3. Drag the `Attrition Rate` measure into the card.
4. Format the value appropriately.

#### Step 4: Create Active Employees Measure

```dax
Active Employees =
[Employee Count] - [Attrition Count]
```

1. Create a new measure using the formula.
2. Add a Card visual.
3. Drag the `Active Employees` measure into it.

#### Step 5: Create Average Age Measure

```dax
Average Age = AVERAGE('HR'[Age])
```

1. Create a new measure.
2. Add a Card visual.
3. Drag the `Average Age` measure into it.
4. Format the value as required.

**Result:** KPI cards display employee count, attrition count, attrition rate, active employees, and average age.

### ii) Create a Lollipop Chart for Attrition Rate by Gender

Power BI does not provide a native lollipop chart in its standard visualizations. It can be simulated using a combination chart or an appropriate custom visual.

1. Select a **Line and Stacked Column Chart** or another suitable combination visual.
2. Drag the `Gender` field to the X-axis.
3. Add the attrition count or attrition rate measure to the appropriate value field.
4. Format the chart to resemble a lollipop chart.
5. Add data labels and a suitable title.

**Chart title:** Attrition Rate by Gender

**Result:** The visualization compares attrition across gender categories.

### iii) Create a Pie Chart for Department-Wise Attrition Percentage

1. Select the **Pie Chart** visual from the Visualizations pane.
2. Drag the `Department` field to **Legend**.
3. Drag the `Attrition Count` measure to **Values**.
4. Select the chart and open the **Format visual** pane.
5. Enable data labels.
6. Set the label style to percentage, if supported by the Power BI version.
7. Customize department colors and label formatting.
8. Add a suitable title.

To display the total attrition count alongside percentages, show the total in the chart title, a separate card, or a tooltip.

**Chart title:** Department-Wise Attrition Percentage

**Result:** The pie chart displays the percentage contribution of each department to total attrition.

### iv) Create a Bar Chart for Employee Count by Age Group

1. Locate the `Age` field in the Data pane.
2. Right-click the field and select **New group**, if available.
3. Set the bin size to **5** to group employees into five-year age intervals.
4. Create a bar chart.
5. Drag the age group or age bin field to the category axis.
6. Drag the `Employee Count` measure to the value axis.
7. Format the chart and add a suitable title.

**Chart title:** Employee Count by Age Group

**Result:** The bar chart displays the number of employees in each age group.

### v) Create a Highlight Table for Job Satisfaction Rating by Job Role

1. Select the **Matrix** visual from the Visualizations pane.
2. Drag `Job Role` to **Rows**.
3. Drag `Job Satisfaction` or the corresponding job satisfaction rating field to **Columns**.
4. Drag `Employee Count` to **Values**.
5. Open the formatting options.
6. Apply conditional formatting, such as background color, to create a highlight-table effect.
7. Adjust column widths and titles for readability.

**Chart title:** Job Satisfaction Rating by Job Role

**Result:** The matrix shows employee counts for each job role and job satisfaction rating.

### vi) Create a Horizontal Bar Chart for Education-Field-Wise Attrition

1. Select a **Clustered Bar Chart** or **Stacked Bar Chart** from the Visualizations pane.
2. Drag `EducationField` or the equivalent education field column to the category axis.
3. Drag the `Attrition Count` measure to the value axis.
4. Format the bars, labels, and chart title.

**Chart title:** Education-Field-Wise Attrition Count

**Result:** The horizontal bar chart compares attrition counts across education fields.

### vii) Create Multiple Donut Charts for Attrition Rate by Gender Across Age Groups

1. Select the **Donut Chart** visual.
2. Drag `Gender` to **Legend**.
3. Drag the `Attrition Rate` measure to **Values**.
4. Use the age group field created earlier to filter the chart.
5. Create separate donut charts for the required age groups, applying a different age-group filter to each chart.
6. Arrange the charts together on the report canvas.
7. Add titles and data labels for clarity.

**Chart title:** Attrition Rate by Gender Across Age Groups

**Result:** Multiple donut charts compare gender-wise attrition rates across different age groups.

---

## Important Notes

- Ensure that the table name and column names in the DAX formulas match the loaded dataset.
- Use the `Attrition Count` measure consistently for attrition-related visuals.
- Use filters to analyze specific age groups, education fields, or departments.
- Apply clear titles, readable labels, and consistent formatting.
- The attrition rate formula above returns a percentage on a 0–100 scale. Format it consistently and avoid multiplying by 100 again through percentage formatting.
- The exact field names may vary depending on the HR dataset.

## Conclusion

The HR dataset was analyzed using Microsoft Power BI. KPI cards were created to summarize key employee metrics, while lollipop-style, pie, bar, matrix, and donut visualizations were used to examine attrition by gender, department, age group, job role, and education field. These visualizations help identify workforce patterns and support HR analysis and decision-making.

