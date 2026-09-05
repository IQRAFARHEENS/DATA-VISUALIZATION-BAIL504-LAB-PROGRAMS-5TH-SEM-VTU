Yes. Since you want **Program 2 README in the same standard and detail level as Program 1**, I’ll keep the **manual's exact structure, terminology, and procedure**, while reflecting what you actually used in your adapted dataset and Tableau work.

I’ll also keep the **MySQL part at the end as a note**, because your manual says “After installing it, we have to connect to MySQL,” but you have not installed MySQL yet. I will **not invent MySQL steps that you have not performed**.

Copy everything below into:

`Program-02-Connecting-Data-Source/README.md`

---

# Program 2: Connecting to Data Source – Connecting to Database & Different Types of Tableau Joins

### Connecting to Data Source, Tableau Joins & Visualization Based on Joins

**Dataset used:** `Program-2-Tableau-Joins-Adapted (1).xlsx`

---

## 📌 Aim

To understand how to connect Tableau to an Excel data source, work with multiple tables, establish relationships between tables using a common field, understand different types of Tableau joins, and create a visualization based on the joined data.

The program demonstrates **Inner Join, Left Join, Right Join, and Full Outer Join** using employee demographic and salary information.

---

## 🗂️ 1. Dataset Used

The dataset used for this program is:

`Program-2-Tableau-Joins-Adapted (1).xlsx`

The Excel workbook contains multiple sheets that can be used as separate tables in Tableau.

### Main Tables Used

#### Demographics

The **Demographics** table contains employee-related information such as:

| Field             | Description                                 |
| ----------------- | ------------------------------------------- |
| `Employee ID`     | Unique identification number of an employee |
| `Nameof Employee` | Name of the employee                        |
| `Employee Gender` | Gender of the employee                      |
| `Start Date`      | Employee starting date                      |

#### Salary

The **Salary** table contains salary-related information:

| Field             | Description                                   |
| ----------------- | --------------------------------------------- |
| `EmployeeID`      | Employee identification number                |
| `Employee Salary` | Salary of the employee                        |
| `Bonus Percent`   | Bonus percentage associated with the employee |

### Common Field

The two tables are connected using:

**`Employee ID`**

This common field allows Tableau to relate/join the employee demographic information with the corresponding salary information.

> 💡 **Important:** A common field such as `Employee ID` is required to establish the connection between the two tables.

---

# 🔌 2. Connecting to the Excel Data Source

### Step 1: Open Tableau

1. Open **Tableau Public**.
2. On the Start Page, locate the **Connect** section on the left side.
3. Under **To a File**, select **Microsoft Excel**.

---

### Step 2: Select the Dataset

1. Browse to the location where the dataset is stored.
2. Select:

`Program-2-Tableau-Joins-Adapted (1).xlsx`

3. Click **Open**.
4. Tableau will display the sheets available in the Excel workbook in the **Data Source** page.

**Screenshot:** `Connecting dataset`

---

### Step 3: View the Available Sheets

After connecting the Excel file, Tableau displays the available sheets on the left side.

The dataset used in this program contains sheets including:

* **Demographics**
* **Salary**
* **Team Details**

The required tables can be dragged from the Sheets section into the workspace.

**Screenshot:** `Demographic table`

---

# 🔗 3. Connecting Demographics and Salary Tables

The **Demographics** and **Salary** tables contain a common field called **Employee ID**.

This field is used to establish the connection between the two tables.

### Step 1: Add the Demographics Table

1. Drag the **Demographics** table from the left-side Sheets section.
2. Drop it into the main Data Source workspace.
3. Tableau displays the columns and records available in the table.

---

### Step 2: Add the Salary Table

1. Drag the **Salary** table into the workspace.
2. Place it near the **Demographics** table.
3. Tableau detects the relationship between the tables using the common field **Employee ID**.

**Screenshot:** `Demographics and Salary Join`

---

### Step 3: Verify the Relationship

The relationship is established as:

```text
Demographics.Employee ID = Salary.EmployeeID
```

The connected tables can now be used to analyze employee information together with salary information.

---

# 🔄 4. Different Types of Tableau Joins

Once the **Demographics** and **Salary** tables are connected, Tableau allows different types of joins.

The four joins demonstrated in this program are:

1. **Inner Join**
2. **Left Join**
3. **Right Join**
4. **Full Outer Join**

The join type determines which records are returned from the two tables.

---

## 🟢 4.1 Inner Join

### Description

An **Inner Join** returns only the records where there is a matching value in **both tables**.

In this program, only employees whose `Employee ID` exists in both the **Demographics** and **Salary** tables will be returned.

### How to Create an Inner Join

1. Place the **Demographics** table in the Data Source workspace.
2. Drag the **Salary** table next to it.
3. Click the join/relationship area between the two tables.
4. Select **Inner Join**.
5. Verify that the common field is:

```text
Employee ID = EmployeeID
```

### Result

Only matching employee records from both tables are included.

**Screenshot:** `Inner join`

---

## 🔵 4.2 Left Join

### Description

A **Left Join** returns:

* All records from the **left table — Demographics**
* Matching records from the **right table — Salary**

If an employee exists in Demographics but has no matching record in Salary, the salary-related fields will contain **NULL** values.

### How to Create a Left Join

1. Keep **Demographics** as the left table.
2. Keep **Salary** as the right table.
3. Open the join settings.
4. Select **Left Join**.
5. Verify the join condition:

```text
Employee ID = EmployeeID
```

### Result

All employee records from the Demographics table are retained, even when corresponding salary information is missing.

**Screenshot:** `Left join`

---

## 🟠 4.3 Right Join

### Description

A **Right Join** returns:

* All records from the **right table — Salary**
* Matching records from the **left table — Demographics**

If a salary record does not have a matching employee record in Demographics, the demographic fields will contain **NULL** values.

### How to Create a Right Join

1. Keep **Demographics** as the left table.
2. Keep **Salary** as the right table.
3. Open the join settings.
4. Select **Right Join**.
5. Verify the join condition:

```text
Employee ID = EmployeeID
```

### Result

All records from the Salary table are retained, including salary records for which matching employee information is not available.

**Screenshot:** `Right join`

---

## 🟣 4.4 Full Outer Join

### Description

A **Full Outer Join** returns all records from both tables.

It includes:

* Matching records from both tables
* Records available only in Demographics
* Records available only in Salary

Where there is no matching record on one side, Tableau displays **NULL** values for the missing fields.

### How to Create a Full Outer Join

1. Keep **Demographics** as the left table.
2. Keep **Salary** as the right table.
3. Open the join settings.
4. Select **Full Outer Join**.
5. Verify the join condition:

```text
Employee ID = EmployeeID
```

### Result

All employee and salary records are included, whether or not a matching record exists in the other table.

**Screenshot:** `Full outer join`

---

# 📊 5. Comparison of Tableau Joins

| Join Type           | Records Returned                                        |
| ------------------- | ------------------------------------------------------- |
| **Inner Join**      | Only matching records from both tables                  |
| **Left Join**       | All records from Demographics + matching Salary records |
| **Right Join**      | All records from Salary + matching Demographics records |
| **Full Outer Join** | All records from both tables                            |

### Simple Representation

```text
INNER JOIN
Only matching records
Demographics ∩ Salary


LEFT JOIN
All Demographics + matching Salary


RIGHT JOIN
All Salary + matching Demographics


FULL OUTER JOIN
All Demographics + All Salary
```

> 💡 **Key Point:** The main difference between these joins is which unmatched records are retained.

---

# 📈 6. Creating a Visualization Based on Joins

After performing the joins, the joined data can be used to create visualizations.

The manual specifies creating a **Bar Chart** showing employees and their salary.

---

## Step 1: Open Sheet 1

1. Click the **Sheet 1** tab at the bottom of Tableau.
2. This opens the worksheet where the visualization is created.

---

## Step 2: Create the Bar Chart

1. Drag **Employee ID** to the **Columns** shelf.
2. Drag **Employee Salary** to the **Rows** shelf.
3. Tableau creates a bar chart showing salary values for the employees.

The resulting visualization represents:

```text
Employee ID → Columns
Employee Salary → Rows
```

**Screenshot:** `Employee Salary by Employee ID.`

---

## Step 3: Sort the Visualization

The manual requires the visualization to be sorted in **descending order**.

1. Select the sorting option in the worksheet.
2. Sort the salary values in **descending order**.
3. The employees with higher salary values will appear before those with lower salary values.

This makes it easier to compare employee salary values.

---

## Step 4: Add Employee Salary to Marks

To provide additional visual information:

1. Drag **Employee Salary** to the **Marks** card.
2. Select **Color**.
3. Select **Label**.

This allows the salary measure to be used for visual encoding and labeling within the chart.

---

# 🖥️ 7. Final Visualization

The completed Sheet 1 visualization displays **Employee Salary by Employee ID** using a bar chart.

### Configuration Used

| Tableau Area      | Field                  |
| ----------------- | ---------------------- |
| **Columns**       | `Employee ID`          |
| **Rows**          | `SUM(Employee Salary)` |
| **Marks – Color** | `Employee Salary`      |
| **Marks – Label** | `Employee Salary`      |
| **Chart Type**    | Bar Chart              |
| **Sorting**       | Descending             |

**Final Sheet:** `Employee Salary by Employee ID`

The visualization makes it possible to compare the salary values associated with different employee IDs.

---

# 🗄️ 8. MySQL Connection

The lab manual also specifies that **after installing MySQL, the dataset has to be connected to MySQL**.

The MySQL portion is kept as a separate part of this program because the current implementation uses the supplied Excel dataset in Tableau.

### Planned MySQL Workflow

After installing MySQL, the general workflow specified for the database connection will be:

```text
Install MySQL
      ↓
Create/Connect to MySQL Database
      ↓
Load the required employee tables
      ↓
Connect Tableau to MySQL
      ↓
Select the required tables
      ↓
Establish Employee ID relationship/join
      ↓
Create the visualization
```

> **Note:** MySQL has not been installed for the current implementation. Therefore, the screenshots and Tableau workbook in this repository document the **Excel-based implementation of Program 2**, as specified in the main procedure of the lab manual.

---

# 💾 9. Save the Tableau Workbook

After completing the joins and visualization:

1. Go to **File → Save As**.
2. Save the Tableau workbook.
3. The workbook used for this program is:

```text
PROGRAM 2.twb
```

4. Keep the workbook together with the dataset so that the work can be reviewed or reproduced.

---

# 📸 10. Screenshots

The `Screenshots` folder contains the step-by-step screenshots captured while completing the program.

| No. | Screenshot                        | Purpose                                 |
| --- | --------------------------------- | --------------------------------------- |
| 1   | `Connecting dataset`              | Connecting the Excel dataset to Tableau |
| 2   | `Demographic table`               | Viewing the Demographics table          |
| 3   | `Demographics and Salary Join`    | Connecting Demographics and Salary      |
| 4   | `Inner join`                      | Creating an Inner Join                  |
| 5   | `Left join`                       | Creating a Left Join                    |
| 6   | `Right join`                      | Creating a Right Join                   |
| 7   | `Full outer join`                 | Creating a Full Outer Join              |
| 8   | `Employee Salary by Employee ID.` | Final Sheet 1 bar chart                 |

---

# 📁 11. Repository Structure

```text
Program-02-Connecting-Data-Source/
│
├── README.md
│
├── PROGRAM 2.twb
│
├── Program-2-Tableau-Joins-Adapted (1).xlsx
│
└── Screenshots/
    │
    ├── 01-connecting-dataset.png
    ├── 02-demographics-table.png
    ├── 03-demographics-and-salary-join.png
    ├── 04-inner-join.png
    ├── 05-left-join.png
    ├── 06-right-join.png
    ├── 07-full-outer-join.png
    └── 08-employee-salary-by-employee-id.png
```

---

# 🎯 12. Learning Outcomes

After completing this program, the learner should be able to:

* Connect Tableau to an **Excel data source**.
* Identify multiple sheets/tables within an Excel workbook.
* Understand how tables can be connected using a **common field**.
* Use `Employee ID` as the common field between Demographics and Salary.
* Understand the concept of **Tableau Joins**.
* Create an **Inner Join**.
* Create a **Left Join**.
* Create a **Right Join**.
* Create a **Full Outer Join**.
* Understand how unmatched records are handled using **NULL values**.
* Create a **bar chart based on joined data**.
* Sort salary values in descending order.
* Use the **Marks card** for Color and Label.
* Understand the basic workflow for connecting Tableau with **MySQL**.

---

# ✅ Result

The Excel dataset containing employee demographic and salary information was successfully connected to Tableau. The **Demographics** and **Salary** tables were connected using the common field **Employee ID**, and the different types of Tableau joins — **Inner, Left, Right, and Full Outer Join** — were explored.

A bar chart was then created in **Sheet 1** to visualize **Employee Salary by Employee ID**, with salary values sorted in descending order and used for color and labeling.

The program provides practical understanding of **data-source connections, table joins, and visualization of joined data in Tableau**.

