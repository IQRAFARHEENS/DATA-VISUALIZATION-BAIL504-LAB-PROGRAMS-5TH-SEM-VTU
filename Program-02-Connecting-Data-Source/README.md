
# Program 2: Connecting to Data Source – Tableau Joins
### Connecting to Data Source, Different Types of Tableau Joins & Visualization

**Dataset used:** `Program-2-Tableau-Joins-Adapted (1).xlsx`

---

## 📌 Aim

To understand how to connect an Excel data source to Tableau, work with multiple tables, establish a connection using a common field, and perform different types of Tableau joins.

This program demonstrates:

- Connecting an Excel workbook to Tableau
- Working with multiple tables
- Identifying a common field between tables
- Creating a relationship between tables
- Understanding the physical layer in Tableau
- Creating an **Inner Join**
- Creating a **Left Join**
- Creating a **Right Join**
- Creating a **Full Outer Join**
- Creating a bar chart using joined data
- Sorting the visualization in descending order
- Using a measure for **Color**
- Using a measure for **Label**

---

# 🗂️ 1. Dataset Used

The dataset used for this program is:

`Program-2-Tableau-Joins-Adapted (1).xlsx`

The Excel workbook contains three related sheets:

1. **Demographics**
2. **Salary**
3. **Team Details**

For the main join demonstration, the following two tables are used:

- `Demographics`
- `Salary`

The common field used to connect the tables is:

**`Employee ID`**

---

## 1.1 Demographics Table

The `Demographics` table contains basic employee information.

| Field | Description |
|---|---|
| `Employee ID` | Unique identifier of the employee |
| `Nameof Employee` | Name of the employee |
| `Employee Gender` | Gender of the employee |
| `Start Date` | Employee's start date |

---

## 1.2 Salary Table

The `Salary` table contains employee salary information.

| Field | Description |
|---|---|
| `EmployeeID` | Employee identifier |
| `Employee Salary` | Salary of the employee |
| `Bonus Percent` | Employee bonus percentage |

---

## 1.3 Team Details Table

The workbook also contains a third sheet called `Team Details`.

It contains:

| Field | Description |
|---|---|
| `EmployeeID` | Employee identifier |
| `Team` | Employee's team |
| `SeniorManagement` | Indicates senior management status |
| `LastLoginTime` | Employee's last login time |

The main join demonstration in this program uses the **Demographics** and **Salary** tables.

---

# 🔑 2. Common Field Used for Joining

When combining two tables, Tableau needs a field that can be used to match records.

In this program, the common field is:

**`Employee ID`**

The relationship between the two main tables is:

```text
Demographics.Employee ID = Salary.EmployeeID
````

This allows Tableau to associate information belonging to the same employee.

For example:

### Demographics

| Employee ID | Nameof Employee | Gender |
| ----------: | --------------- | ------ |
|           1 | Douglas         | Male   |
|           2 | Thomas          | Male   |
|           3 | Maria           | Female |

### Salary

| EmployeeID | Employee Salary |
| ---------: | --------------: |
|          1 |           97308 |
|          2 |           61933 |
|          3 |          130590 |

Employee ID `1` in Demographics corresponds to Employee ID `1` in Salary.

Therefore, Tableau can combine the information:

| Employee ID | Name    | Gender | Salary |
| ----------: | ------- | ------ | -----: |
|           1 | Douglas | Male   |  97308 |

---

# 🔌 3. Connecting to Excel Files in Tableau

## Step 1: Open Tableau

1. Open **Tableau Public**.
2. On the Start Page, locate the **Connect** section on the left side.

---

## Step 2: Select Microsoft Excel

Under:

**To a File**

select:

**Microsoft Excel**

---

## Step 3: Select the Dataset

Browse to the location where the dataset is saved.

Select:

```text
Program-2-Tableau-Joins-Adapted (1).xlsx
```

Click **Open**.

---

## Step 4: View the Available Sheets

After opening the workbook, Tableau displays the sheets available in the Excel file.

The available sheets are:

* `Demographics`
* `Salary`
* `Team Details`

These tables can be dragged into the Tableau Data Source workspace.

**Screenshot:** `01-connecting-dataset.png`

---

# 📊 4. Adding the Demographics Table

1. From the Sheets section on the left, locate **Demographics**.
2. Drag **Demographics** into the Data Source workspace.
3. Tableau displays the fields available in the table.
4. The table contains employee demographic information.

**Screenshot:** `02-demographics-table.png`

---

# 🔗 5. Adding the Salary Table

1. From the Sheets section, locate **Salary**.
2. Drag **Salary** next to the `Demographics` table.
3. Tableau identifies the common field.
4. The common field is:

```text
Employee ID
```

The relationship is:

```text
Demographics.Employee ID = Salary.EmployeeID
```

**Screenshot:** `03-demographics-and-salary-join.png`

---

# 🧩 6. Relationship and Physical Layer

Tableau first represents the connection between the tables in the logical layer.

The two tables are connected using:

```text
Employee ID = EmployeeID
```

To create the traditional Tableau joins used in this program:

1. Double-click the `Demographics` logical table.
2. Tableau opens the physical layer.
3. The Demographics table appears in the physical layer.
4. Add the `Salary` table to the physical layer.
5. Tableau displays the Join configuration.

The Join configuration provides:

* Inner
* Left
* Right
* Full Outer

---

# 🔄 7. Types of Tableau Joins

A **Join** combines records from two tables based on a common field.

In this program, the common field is:

```text
Employee ID
```

The four join types demonstrated are:

1. Inner Join
2. Left Join
3. Right Join
4. Full Outer Join

To understand the differences clearly, consider the following example.

---

## Example Tables

### Demographics Table

| Employee ID | Name    |
| ----------: | ------- |
|           1 | Douglas |
|           2 | Thomas  |
|           3 | Maria   |
|           4 | Jerry   |
|           5 | Larry   |

### Salary Table

| EmployeeID | Employee Salary |
| ---------: | --------------: |
|          1 |           97308 |
|          2 |           61933 |
|          3 |          130590 |
|          6 |           75000 |

Here:

* Employee IDs `1, 2, 3` exist in both tables.
* Employee IDs `4, 5` exist only in Demographics.
* Employee ID `6` exists only in Salary.

This example makes it easy to understand what each join returns.

---

# 🟢 7.1 Inner Join

## Definition

An **Inner Join** returns only the records where the common field has a matching value in **both tables**.

The join condition is:

```text
Demographics.Employee ID = Salary.EmployeeID
```

Only Employee IDs that appear in both tables are returned.

---

## Example

From the example:

### Matching Employee IDs

```text
1 → exists in both
2 → exists in both
3 → exists in both
```

Therefore, the Inner Join result is:

| Employee ID | Name    | Employee Salary |
| ----------: | ------- | --------------: |
|           1 | Douglas |           97308 |
|           2 | Thomas  |           61933 |
|           3 | Maria   |          130590 |

Employee IDs `4`, `5`, and `6` are not included because they do not have matching records in both tables.

---

## How to Create Inner Join in Tableau

1. Place `Demographics` in the physical layer.
2. Add `Salary`.
3. Click the Join configuration.
4. Select **Inner Join**.
5. Verify:

```text
Employee ID = EmployeeID
```

6. Tableau returns only matching records.

**Screenshot:** `04-inner-join.png`

---

## Result

The Inner Join keeps only records common to both tables.

```text
Demographics ∩ Salary
        ↓
Matching records only
```

---

# 🔵 7.2 Left Join

## Definition

A **Left Join** returns:

* All records from the **left table**
* Matching records from the **right table**

In this program:

```text
Left Table  = Demographics
Right Table = Salary
```

Therefore, all records from Demographics are retained.

---

## Example

Demographics contains:

```text
1, 2, 3, 4, 5
```

Salary contains:

```text
1, 2, 3, 6
```

The Left Join keeps **all Demographics records**.

The result is:

| Employee ID | Name    | Employee Salary |
| ----------: | ------- | --------------: |
|           1 | Douglas |           97308 |
|           2 | Thomas  |           61933 |
|           3 | Maria   |          130590 |
|           4 | Jerry   |            NULL |
|           5 | Larry   |            NULL |

Employee IDs `4` and `5` are retained because they exist in the left table.

Since no matching salary information exists for them, their salary values are:

`NULL`

---

## How to Create Left Join in Tableau

1. Keep `Demographics` as the left table.
2. Keep `Salary` as the right table.
3. Open the Join configuration.
4. Select **Left Join**.
5. Verify:

```text
Employee ID = EmployeeID
```

**Screenshot:** `05-left-join.png`

---

## Result

All records from Demographics are retained.

```text
All Demographics
       +
Matching Salary
```

---

# 🟠 7.3 Right Join

## Definition

A **Right Join** returns:

* All records from the **right table**
* Matching records from the **left table**

In this program:

```text
Left Table  = Demographics
Right Table = Salary
```

Therefore, all Salary records are retained.

---

## Example

Salary contains:

```text
1, 2, 3, 6
```

Demographics contains:

```text
1, 2, 3, 4, 5
```

The Right Join keeps **all Salary records**.

The result is:

| Employee ID | Name    | Employee Salary |
| ----------: | ------- | --------------: |
|           1 | Douglas |           97308 |
|           2 | Thomas  |           61933 |
|           3 | Maria   |          130590 |
|           6 | NULL    |           75000 |

Employee ID `6` is retained because it exists in the right table.

Since there is no matching employee information in Demographics, the employee name is:

`NULL`

---

## How to Create Right Join in Tableau

1. Keep `Demographics` as the left table.
2. Keep `Salary` as the right table.
3. Open the Join configuration.
4. Select **Right Join**.
5. Verify:

```text
Employee ID = EmployeeID
```

**Screenshot:** `06-right-join.png`

---

## Result

All records from Salary are retained.

```text
All Salary
    +
Matching Demographics
```

---

# 🟣 7.4 Full Outer Join

## Definition

A **Full Outer Join** returns **all records from both tables**.

It includes:

* Matching records
* Records found only in Demographics
* Records found only in Salary

If a record has no matching record in the other table, Tableau displays `NULL` for the missing fields.

---

## Example

Demographics contains:

```text
1, 2, 3, 4, 5
```

Salary contains:

```text
1, 2, 3, 6
```

The Full Outer Join contains:

```text
1, 2, 3, 4, 5, 6
```

The result is:

| Employee ID | Name    | Employee Salary |
| ----------: | ------- | --------------: |
|           1 | Douglas |           97308 |
|           2 | Thomas  |           61933 |
|           3 | Maria   |          130590 |
|           4 | Jerry   |            NULL |
|           5 | Larry   |            NULL |
|           6 | NULL    |           75000 |

All records from both tables are retained.

---

## How to Create Full Outer Join in Tableau

1. Keep `Demographics` as the left table.
2. Keep `Salary` as the right table.
3. Open the Join configuration.
4. Select **Full Outer Join**.
5. Verify:

```text
Employee ID = EmployeeID
```

**Screenshot:** `07-full-outer-join.png`

---

## Result

All records from both tables are retained.

```text
All Demographics
       +
All Salary
```

---

# 📋 8. Comparison of Join Types

| Join Type           | Left Table Records | Right Table Records | Main Result                  |
| ------------------- | ------------------ | ------------------- | ---------------------------- |
| **Inner Join**      | Matching only      | Matching only       | Only common records          |
| **Left Join**       | All                | Matching only       | All left-table records       |
| **Right Join**      | Matching only      | All                 | All right-table records      |
| **Full Outer Join** | All                | All                 | All records from both tables |

---

# 💡 9. Easy Way to Remember the Joins

### Inner Join

**Only what is common**

```text
A ∩ B
```

### Left Join

**Everything from the left**

```text
A + matching B
```

### Right Join

**Everything from the right**

```text
B + matching A
```

### Full Outer Join

**Everything from both**

```text
A + B
```

---

# 📈 10. Creating a Visualization Based on Joins

After performing the joins, the joined data can be used to create a visualization.

The laboratory exercise requires a **Bar Chart**.

---

## Step 1: Open Sheet 1

Click the **Sheet 1** tab at the bottom of Tableau.

This opens the worksheet where the visualization is created.

---

## Step 2: Add Employee ID to Columns

1. Locate **Employee ID** in the Data Pane.
2. Drag `Employee ID` to the **Columns** shelf.

This places the employee IDs along the horizontal axis.

---

## Step 3: Add Employee Salary to Rows

1. Locate `Employee Salary`.
2. Drag `Employee Salary` to the **Rows** shelf.
3. Tableau creates a bar chart.

The basic configuration is:

```text
Columns → Employee ID
Rows → Employee Salary
```

**Screenshot:** `08-employee-salary-by-employee-id.png`

---

# 📊 11. Understanding Sheet 1

The Sheet 1 visualization displays the salary associated with each employee ID.

The salary field is treated as a measure and is aggregated by Tableau.

Therefore, the Rows shelf displays:

```text
SUM(Employee Salary)
```

The height of each bar represents the salary value.

A higher bar represents a higher salary value.

---

# 🔽 12. Sort the Salary in Descending Order

The laboratory instructions require the salary values to be sorted in descending order.

### Steps

1. Select the salary visualization.
2. Use Tableau's **Sort Descending** option.
3. Tableau rearranges the bars according to salary.
4. The higher salary values appear before the lower salary values.

Descending order means:

```text
Highest Salary
      ↓
      ↓
      ↓
Lowest Salary
```

---

# 🎨 13. Add Employee Salary to Color

The laboratory instructions also require `Employee Salary` to be used for **Color**.

### Steps

1. Locate `Employee Salary`.
2. Drag it to the **Color** option in the Marks card.

The bars are now visually differentiated according to salary values.

---

# 🏷️ 14. Add Employee Salary to Label

To display the salary value directly on each bar:

1. Drag `Employee Salary` to the **Label** option in the Marks card.
2. Tableau displays the salary value on the corresponding bar.

The Marks card now uses:

```text
Color → Employee Salary
Label → Employee Salary
```

---

# 🖥️ 15. Final Sheet 1 Configuration

The final Sheet 1 visualization uses:

| Tableau Area      | Field                  |
| ----------------- | ---------------------- |
| **Columns**       | `Employee ID`          |
| **Rows**          | `SUM(Employee Salary)` |
| **Marks → Color** | `Employee Salary`      |
| **Marks → Label** | `Employee Salary`      |
| **Chart Type**    | Bar Chart              |
| **Sort**          | Descending             |

### Final Worksheet Name

The Sheet 1 worksheet is named:

**Employee Salary by Employee ID**

---

# 📸 16. Screenshots

The screenshots document the major steps performed during the program.

Recommended naming:

```text
Screenshots/
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

Each screenshot represents an important stage of the implementation.

---

# 💾 17. Saving the Tableau Workbook

After completing the joins and visualization:

1. Go to **File → Save As**.
2. Save the Tableau workbook.
3. The workbook used for this program is:

```text
PROGRAM 2.twb
```

4. Keep the workbook and Excel dataset together in the Program 2 folder.

---

# 🗄️ 18. MySQL Connection – Future Step

The laboratory manual also mentions connecting the data source to **MySQL** after installing MySQL.

The current implementation of this program uses the Excel dataset in Tableau.

MySQL has not yet been installed for this implementation.

The planned workflow is:

```text
Install MySQL
       ↓
Create/Connect to MySQL Database
       ↓
Load Employee Data
       ↓
Connect Tableau to MySQL
       ↓
Select Required Tables
       ↓
Use Employee ID as Common Field
       ↓
Create Joins
       ↓
Create Visualization
```

This section is included to document the database-connection requirement from the laboratory instructions. The current screenshots and workbook demonstrate the **Excel-based implementation**.

---

# 📁 19. Repository Structure

The Program 2 folder is organized as follows:

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

# 🎯 20. Learning Outcomes

After completing this program, the learner should be able to:

* Connect an Excel workbook to Tableau.
* Identify different sheets in an Excel workbook.
* Understand tables and fields.
* Identify a common field between two tables.
* Use `Employee ID` as a join key.
* Understand Tableau relationships.
* Open the physical layer in Tableau.
* Create an Inner Join.
* Create a Left Join.
* Create a Right Join.
* Create a Full Outer Join.
* Understand how unmatched records produce `NULL` values.
* Create a bar chart using joined data.
* Sort salary values in descending order.
* Use a measure on the Color option.
* Use a measure on the Label option.
* Understand the basic workflow for connecting Tableau with MySQL.

---

# ✅ 21. Result

The Excel workbook was successfully connected to Tableau.

The `Demographics` and `Salary` tables were connected using the common field:

```text
Employee ID
```

The four major Tableau join types were studied and demonstrated:

* **Inner Join**
* **Left Join**
* **Right Join**
* **Full Outer Join**

A bar chart was created in **Sheet 1** using:

```text
Employee ID → Columns
Employee Salary → Rows
```

The salary visualization was sorted in descending order, and `Employee Salary` was added to the **Color** and **Label** options of the Marks card.

---

# 🏁 22. Conclusion

This program provides practical understanding of connecting Excel data to Tableau and combining related tables using different join types.

The program demonstrates how the choice of join affects which records are included in the resulting dataset.

By working with Inner, Left, Right, and Full Outer Joins, the learner gains a clear understanding of how Tableau handles matching and unmatched records.

The joined data was then used to create a salary-based bar chart in Sheet 1, providing a practical example of how joined datasets can be transformed into visual insights.

```

Also, the MySQL section is clearly marked as **future/not yet performed**, so your GitHub README doesn't falsely claim that you completed a MySQL connection.
```
