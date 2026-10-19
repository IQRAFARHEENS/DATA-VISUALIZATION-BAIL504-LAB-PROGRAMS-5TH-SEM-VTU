# Experiment No. 8: Dashboards — Filters in Power BI and Formatting Dashboards

## 1. Aim

To apply different types of filters in Microsoft Power BI and format the final dashboard using the HR dataset used in Experiment No. 7.

## 2. Software Requirements

- Microsoft Power BI Desktop
- HR dataset used in Experiment No. 7
- Windows operating system

## 3. Objectives

- Understand the purpose of filters in Power BI.
- Learn about the Filters pane and slicers.
- Apply visual-level, page-level, report-level, and drill-through filters.
- Apply basic filtering to the Department field.
- Apply advanced filtering to Monthly Income.
- Apply Top N filtering to display the top four job roles by job satisfaction.
- Format the final dashboard for better readability and presentation.

## 4. Introduction

Filters remove all but the data that users want to focus on. In Power BI, filters can be applied through the Filters pane or by making selections in slicers directly on the report page.

The Filters pane displays fields associated with individual visuals and other filters added by the report designer. Filters help users focus on specific categories, values, or records without changing the original dataset.

### Types of Filters in Power BI

There are four standard types of filters available in the Filters pane.

| Filter Type | Description |
|---|---|
| Visual-level filter | Applies to a single visual on a report page. |
| Page-level filter | Applies to all visuals on a particular report page. |
| Report-level filter | Applies to all pages in the report. |
| Drill-through filter | Allows users to navigate to a detailed destination page focused on a selected entity or data point. |

### 1. Visual-Level Filter

A visual-level filter applies only to the selected visual on the report canvas. It allows users to filter the information displayed in one chart or visual without affecting other visuals.

### 2. Page-Level Filter

A page-level filter applies to all visuals on the selected report page. It is useful when the entire page needs to display information for a particular department, category, or condition.

### 3. Report-Level Filter

A report-level filter applies to all pages within a Power BI report. It is useful when the same filtering condition must remain consistent throughout the report.

### 4. Drill-Through Filter

Drill-through allows users to navigate from a summary visual to a destination report page containing detailed information about a selected entity, such as a supplier, department, or job role.

Users can right-click a data point and select the drill-through destination when the report has been configured appropriately.

## 5. Procedure

The HR dataset used in Experiment No. 7 will be used to extend the existing report by applying filters and formatting the final dashboard.

### Step 1: Open the Existing Power BI Report

1. Open Microsoft Power BI Desktop.
2. Open the HR report created in Experiment No. 7.
3. Verify that the dataset and previously created visuals are available.
4. Review the existing charts and dashboard layout.
5. Save a copy of the report if you want to preserve the original version.

### Step 2: Understand the Filters Pane

1. Open the report in Report view.
2. Locate the **Filters** pane.
3. Select a visual on the report canvas.
4. Observe the filters associated with the selected visual.
5. Identify the sections for filters on this visual, filters on this page, and filters on all pages, depending on the Power BI interface.
6. Expand a filter field to view its available filtering options.

The Filters pane allows users to apply conditions to the data displayed in the report.

### Step 3: Apply Basic Filtering to the Department Field

**Objective:** Display data for selected departments.

1. Select the report page containing the HR visuals.
2. In the Data pane, locate the `Department` field.
3. Drag the `Department` field into **Filters on this page** if you want the filter to affect the entire page, or into **Filters on this visual** if you want it to affect only one visual.
4. Expand the Department filter.
5. Select **Basic filtering** as the filter type, if it is not already selected.
6. Select the `HR` department.
7. Observe the report visuals and verify that they display only the HR department data wherever the filter applies.
8. Next, select both `HR` and `R&D`.
9. Observe the updated visuals.

**Expected result:** When HR is selected, the affected visuals display HR data only. When HR and R&D are selected, the affected visuals display data for both departments.

**Note:** The supplied lab instructions mention placing Department in **Filters on this page**. This applies the filter to the entire page, not to a single visual. For a particular visual only, use **Filters on this visual**.

### Step 4: Apply Advanced Filtering to Monthly Income

**Objective:** Display records where Monthly Income is greater than or equal to 10,000.

1. Locate the `Monthly Income` field in the Data pane.
2. Drag it into the appropriate Filters pane section.
3. Expand the Monthly Income filter.
4. Select **Advanced filtering** as the filter type.
5. Under **Show items when the value**, select:

   `is greater than or equal to`

6. Enter the value:

   `10000`

7. Apply the filter if required by the interface.
8. Observe the affected visuals.
9. Verify that only records satisfying the Monthly Income condition are included in the filtered results.

**Expected result:** The affected visuals display data for employees whose Monthly Income is greater than or equal to 10,000.

**Note:** The result depends on the data type and values in the HR dataset. Ensure Monthly Income is treated as a numeric field.

### Step 5: Apply Top N Filtering to Job Role

**Objective:** Display the top four job roles having the highest job satisfaction.

1. Locate the existing **Job Satisfaction Rating** visual created using the HR dataset.
2. Select the visual on the report canvas.
3. In the Filters pane, locate the **Filters on this visual** section.
4. Add or select the `Job Role` field under this section.
5. Expand the Job Role filter.
6. Select **Top N** as the filter type.
7. Under **Show items**, select `Top`.
8. Enter:

   `4`

9. Locate the **By value** field.
10. Add the `Job Satisfaction` measure or the appropriate job satisfaction field used by the visual.
11. If the dataset provides a numeric Job Satisfaction field and the lab requires summation, use **Sum of Job Satisfaction**.
12. Click **Apply filter** if the interface displays this option.
13. Observe the visual and verify that it displays four job roles according to the selected ranking measure.

**Expected result:** The visual displays the top four job roles ranked by the selected job satisfaction value.

**Important:** Top N ranking depends on the field selected under **By value**. Use the same Job Satisfaction field and aggregation specified in your lab instructions. If the goal is to compare average satisfaction rather than the sum, use an appropriate average measure instead.

### Step 6: Format the Final Dashboard

After applying the filters, format the report so that the information is easy to read and understand.

1. Review the layout of the existing visuals.
2. Select each visual and open the **Format visual** pane.
3. Check that every chart has a meaningful title.
4. Use consistent title fonts, font sizes, and alignment.
5. Select appropriate colors for different categories.
6. Ensure that labels and values are readable.
7. Adjust the size and placement of the visuals.
8. Align charts and cards neatly on the report canvas.
9. Format the Filters pane and slicers where the available settings permit.
10. Avoid excessive colors and unnecessary visual elements.
11. Verify that the dashboard remains readable when filters are applied.

### Step 7: Verify Filter Interactions

1. Select the Department filter and change the selected department.
2. Check whether the affected visuals update correctly.
3. Change the Monthly Income filter to a different value.
4. Verify that the filtered results change accordingly.
5. Check that the Top N filter displays four job roles when sufficient valid categories exist.
6. If a visual does not respond as expected, review the filter scope and visual interactions.
7. Confirm that page-level filters affect the selected page and report-level filters affect all report pages.

### Step 8: Save the Final Power BI Report

1. Review all filters and visuals.
2. Confirm that the Department, Monthly Income, and Top N filters work as intended.
3. Verify the formatting of titles, colors, labels, and layout.
4. Select **File → Save As** if you want to save the updated report as a separate file.
5. Enter the filename:

   `Program-08.pbix`

6. Choose the required location.
7. Click **Save**.

## 6. Summary of Filter Operations

| Experiment Task | Filter Type | Field | Condition |
|---|---|---|---|
| Department filtering | Basic filtering | Department | Select HR, then HR and R&D |
| Monthly Income filtering | Advanced filtering | Monthly Income | Greater than or equal to 10,000 |
| Top job roles | Top N filtering | Job Role | Top 4 by Job Satisfaction |
| Filter an individual chart | Visual-level filter | Selected field | Applies to one visual |
| Filter one report page | Page-level filter | Selected field | Applies to all visuals on that page |
| Filter the entire report | Report-level filter | Selected field | Applies across all report pages |
| View detailed information | Drill-through filter | Selected entity | Navigates to a configured detail page |

## 7. Advantages of Filters in Power BI

1. Filters help users focus on relevant information.
2. They make reports more interactive.
3. They allow users to compare selected categories.
4. They help identify specific records that meet a condition.
5. They support analysis of large datasets.
6. They make dashboards more useful for decision-making.

## 8. Viva Questions and Answers

**1. What is a filter in Power BI?**

A filter restricts the data displayed in a report to the records that meet specified conditions.

**2. What is the Filters pane?**

The Filters pane is used to add, configure, and manage filters for visuals, report pages, and the entire report.

**3. What are the four standard types of filters in Power BI?**

Visual-level filters, page-level filters, report-level filters, and drill-through filters.

**4. What is a visual-level filter?**

A visual-level filter affects only the selected visual on a report page.

**5. What is a page-level filter?**

A page-level filter affects all visuals on a particular report page.

**6. What is a report-level filter?**

A report-level filter affects all pages in a Power BI report.

**7. What is a drill-through filter?**

A drill-through filter allows users to navigate to a destination report page focused on a selected data point or entity.

**8. What is basic filtering?**

Basic filtering allows users to select specific values or categories to include in the results.

**9. What is advanced filtering?**

Advanced filtering allows users to specify conditions such as greater than, less than, equal to, or greater than or equal to.

**10. What is Top N filtering?**

Top N filtering displays a specified number of categories ranked according to a selected field or measure.

**11. Why is the Monthly Income filter used in this experiment?**

It identifies records where Monthly Income is greater than or equal to 10,000.

**12. Why is Top N filtering applied to Job Role?**

It displays the top four job roles based on the selected Job Satisfaction measure.

**13. What is a dashboard or report visual?**

A visual is a graphical representation of data, such as a chart, card, matrix, or table. In Power BI Desktop, these visuals are commonly arranged on report pages.

**14. Why is dashboard formatting important?**

Formatting improves readability, visual consistency, and the presentation of information.

**15. What is the difference between a filter and a slicer?**

A filter is configured through the Filters pane or other filtering mechanisms, while a slicer is an interactive visual placed directly on a report page.

## 9. Result

The HR report created in Experiment No. 7 was extended using Power BI filters. Basic filtering was applied to the Department field, advanced filtering was applied to Monthly Income to display values greater than or equal to 10,000, and Top N filtering was used to display the top four job roles according to the selected Job Satisfaction measure. The final report was formatted and saved.

## 10. Conclusion

This experiment demonstrates how filters can be used in Power BI to focus on relevant data and improve report interactivity. Visual-level, page-level, report-level, and drill-through filters provide different scopes for filtering information. Basic, advanced, and Top N filtering help users analyze specific departments, income ranges, and ranked job roles. Consistent formatting improves the readability and presentation of the final report.

**Author:** Iqra Farheen
