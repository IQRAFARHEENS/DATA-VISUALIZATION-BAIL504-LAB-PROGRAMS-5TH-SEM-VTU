Program 4: Dashboard Design and Storytelling Using Tableau
Dashboard Components, Worksheet Containers, Action Filters & Tableau Storytelling

Dataset used: GDP by Country per Year_data.xlsx

📌 Aim

To design an interactive dashboard and create a meaningful data story using Tableau Public by understanding dashboard components, worksheet placement using containers, action filters, and Tableau storytelling techniques.

This program demonstrates:

Creating worksheets for data visualization
Combining worksheets into a dashboard
Understanding dashboard components
Using containers to organize worksheets
Creating interactive Action Filters
Understanding different types of Tableau actions
Creating a Story using Tableau Public
Using story points and captions
Applying the Tailoring-In storytelling technique
Adding text to highlight important observations
Publishing the Tableau workbook
🎥 1. Program Screen Recordings & Materials

The complete screen recording and supporting materials for Program 4 are available in the Google Drive folder below.

👉 
View Program 4 Screen Recording & Materials

The recording demonstrates the complete implementation of the Tableau Dashboard and Storytelling program.

🗂️ 2. Dataset Used

The dataset used for this program is:

GDP by Country per Year_data.xlsx

The dataset contains country-wise GDP Growth information across different years.

Important Fields
Field	Description
Country	Name of the country
Year	Year of observation
GDP Growth	GDP growth value for the country and year
🔌 3. Connecting to the Data Source
Step 1: Open Tableau
Open Tableau Public.
Select Microsoft Excel from the Connect section.
Browse to the location of the dataset.
Step 2: Select the Dataset

Select:

GDP by Country per Year_data.xlsx

Click Open.

Tableau loads the data and displays the available fields.

🗺️ 4. Creating the GDP Growth Map

The first worksheet is created to display GDP Growth geographically.

Step 1: Create a New Worksheet

Click the Worksheet tab at the bottom of Tableau.

Rename the worksheet:

GDP Growth Map – 2016
Step 2: Create the Map

Drag:

Country → View

Tableau automatically creates a geographical map using the Country field.

Step 3: Add GDP Growth

Drag:

GDP Growth → Color

The countries are now represented using different colors based on their GDP Growth values.

Step 4: Add Year Filter

Drag:

Year → Filters

Select:

2016

Click OK.

The map now represents GDP Growth by country for 2016.

Result

The map provides a global view of GDP Growth across countries in 2016.

📈 5. Creating the GDP Growth Trend

The second worksheet is created to display GDP Growth over time.

Step 1: Create a New Worksheet

Create a new worksheet.

Rename it:

GDP Growth Trend
Step 2: Add Year to Columns

Drag:

Year → Columns

The years appear along the horizontal axis.

Step 3: Add GDP Growth to Rows

Drag:

GDP Growth → Rows

The GDP Growth values appear along the vertical axis.

Step 4: Add Country to Color

Drag:

Country → Color

Each country is represented by a different line.

Step 5: Select Line Chart

From the Marks card, select:

Line

The visualization now displays the GDP Growth trend for different countries over time.

🖥️ 6. Creating the Dashboard

The dashboard combines the map and line chart into one interactive view.

Step 1: Create a New Dashboard

Click:

New Dashboard

Rename it:

GDP Growth Dashboard
Step 2: Add the Worksheets

From the Sheets section, drag:

GDP Growth Map – 2016

and

GDP Growth Trend

into the dashboard.

Arrange the worksheets side-by-side.

The dashboard contains:

+----------------------+----------------------+
|                      |                      |
|      GDP MAP         |    GDP TREND         |
|                      |                      |
+----------------------+----------------------+
Step 3: Add Dashboard Title

Enable:

Show Dashboard Title

Set the title to:

GDP Growth Dashboard
📦 7. Understanding Dashboard Containers

Containers are used to organize and position worksheets and other dashboard objects.

Horizontal Container

A Horizontal Container places objects from left to right.

Example:

+-------------------+-------------------+
|       Map         |    Line Chart     |
+-------------------+-------------------+
Vertical Container

A Vertical Container places objects from top to bottom.

Example:

+--------------------------------------+
|                 Map                  |
+--------------------------------------+
|              Line Chart              |
+--------------------------------------+

Containers help maintain proper alignment and organization of dashboard components.

🔄 8. Creating an Action Filter

An Action Filter creates interaction between different worksheets.

In this program, the GDP Growth Trend is used to control the GDP Growth Map.

Steps
Open:
Dashboard → Actions
Click:
Add Action → Filter
Enter the action name:
Country Selection Filter
Under Source Sheets, select:
GDP Growth Trend
Under Target Sheets, select:
GDP Growth Map – 2016
Set:
Run action on → Select
Select:
Selected fields
Set the field mapping:
Country → Country
Under clearing the selection, select:
Show all values
Click OK.
Action Filter Interaction

The interaction works as follows:

Select Country on GDP Growth Trend
                ↓
        Country Selection Filter
                ↓
      GDP Growth Map – 2016

For example:

Select India
      ↓
Map responds to India

This makes the dashboard interactive.

🧩 9. Types of Tableau Actions

Tableau provides different types of actions.

1. Filter Action

Filters another worksheet based on a user's selection.

2. Highlight Action

Highlights related marks without necessarily filtering out the remaining data.

3. URL Action

Opens a specified web page when a user interacts with a visualization.

4. Go to Sheet Action

Navigates the user to another worksheet, dashboard, or story.

5. Parameter Action

Changes a parameter value based on user interaction.

6. Set Action

Changes the members of a Tableau set through interaction.

📖 10. Creating a Story with Tableau Public

A Tableau Story consists of multiple story points arranged to communicate a meaningful data narrative.

For this program, the Tailoring-In approach is used.

Tailoring-In

The story begins with a big-picture view and progressively focuses on a specific detail.

Global View
     ↓
Specific Country
     ↓
Detailed Country Trend
🌍 11. Story Point 1 — Global View

Create a new story.

Rename it:

GDP Growth Story

Add:

GDP Growth Map – 2016
Caption
Global GDP Growth by Country – 2016

This story point provides the overall/global view of GDP Growth.

🇮🇳 12. Story Point 2 — India Selected

Duplicate the first story point.

Select India on the map.

Click Update to save the selected state.

Caption
India – Selected Country

India is now highlighted while the story focuses on the selected country.

This represents the zoom-in stage of the story.

📈 13. Story Point 3 — India GDP Growth Trend

A separate worksheet was created for India's GDP Growth trend.

Worksheet Name
India GDP Growth Trend
Steps
Duplicate the GDP Growth Trend worksheet.
Rename it:
India GDP Growth Trend
Apply a Country filter.
Select:
India
Add the worksheet to the third story point.
Caption
India GDP Growth Trend (2000–2020)

This story point provides a detailed view of India's GDP Growth over time.

📝 14. Adding Text to the Story

Text boxes can be used to communicate important observations.

For example:

India's GDP Growth shows significant variation
between 2000 and 2020, including a sharp decline
in 2020.

Text helps the audience understand the key message associated with the visualization.

🔗 15. Final Story Flow

The final story follows the Tailoring-In technique:

Global GDP Growth by Country – 2016
                  ↓
           India – Selected Country
                  ↓
       India GDP Growth Trend
             (2000–2020)

The story progresses from:

Global → Specific → Detailed

📸 16. Screenshots

The screenshots document the major stages of Program 4.

Recommended structure:

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

Each screenshot represents an important stage of the implementation.

🎥 17. Screen Recording & Supporting Materials

The complete Program 4 screen recording and supporting materials are available in the Google Drive folder:

👉 
View Program 4 Screen Recording & Supporting Materials

The recording demonstrates:

Connecting the GDP dataset
Creating the GDP Growth map
Creating the GDP Growth trend
Creating the dashboard
Configuring the Action Filter
Testing country selection
Creating the Tableau Story
Selecting India
Creating the India GDP Growth Trend
Navigating through the story points
📁 18. Repository Structure

The Program 4 folder can be organized as follows:

Program-04-Dashboard-and-Storytelling/
│
├── README.md
│
├── GDP by Country per Year_data.xlsx
│
├── Program4_Tableau_Dashboard.twbx
│
└── screenshots/
    │
    ├── 01-gdp-growth-map-2016.png
    ├── 02-gdp-growth-trend.png
    ├── 03-dashboard.png
    ├── 04-action-filter.png
    ├── 05-action-filter-india.png
    ├── 06-story-global-view.png
    ├── 07-story-india-selected.png
    └── 08-story-india-trend.png
🎯 19. Learning Outcomes

After completing this program, the learner should be able to:

Create multiple worksheets in Tableau.
Create geographical visualizations.
Create time-series line charts.
Combine worksheets into a dashboard.
Understand dashboard components.
Use horizontal and vertical containers.
Create Action Filters.
Understand different types of Tableau actions.
Create interactive dashboards.
Create Tableau Stories.
Create and navigate story points.
Add captions and text boxes.
Understand the Tailoring-In storytelling technique.
Present data as a meaningful visual narrative.
✅ 20. Result

The GDP dataset was successfully connected to Tableau Public.

The following visualizations were created:

GDP Growth Map – 2016
GDP Growth Trend
India GDP Growth Trend

An interactive dashboard named:

GDP Growth Dashboard

was successfully created by combining the map and line chart.

A Country Selection Filter was implemented so that selecting a country in the GDP Growth Trend interacts with the GDP Growth Map.

A Tableau Story named:

GDP Growth Story

was created using three story points:

1. Global GDP Growth by Country – 2016
2. India – Selected Country
3. India GDP Growth Trend (2000–2020)

The story follows the Tailoring-In approach, moving from a global view to a specific country and finally to its detailed historical trend.

🏁 21. Conclusion

This program provided practical experience in designing interactive dashboards and creating data-driven stories using Tableau Public.

The program demonstrated how multiple worksheets can be combined into a dashboard, how containers can be used to organize dashboard components, and how Action Filters can create interaction between visualizations.

A Tableau Story was also created using the Tailoring-In technique, progressing from the global GDP Growth view to India and finally to India's GDP Growth trend from 2000 to 2020.

Overall, the program demonstrates the use of Tableau dashboards, containers, Action Filters, interactive visualizations, and storytelling to communicate data effectively.

🔗 Tableau Public Workbook

Tableau Public Link:
Add your Tableau Public published workbook link here.

👩‍💻 Author

Iqra Farheen S
