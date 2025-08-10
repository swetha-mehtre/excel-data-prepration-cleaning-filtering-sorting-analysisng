
# Excel Project on Student Data Analysis

This project analyzes a student dataset containing information on attendance, assignment scores, lab scores, final exam scores, and total scores for students from various departments. The goal is to clean the data, perform calculations, visualize, and summarize student performance using Excel features.

---

## Step 1: Data Cleaning — Fix Invalid Attendance Values

**Issue:** Some attendance percentages exceed 100%, which is not possible.

**Action:** Use Excel filters to identify attendance values >100%, then correct them manually to a max of 100%.

**Effect:** Ensures attendance data is realistic and consistent for analysis.

---

## Step 2: Calculate Averages

Calculate average scores overall and by department.

**Example:**

* To calculate the average **Total Score** for all students:
  `=AVERAGE(H2:H100)`  *(assuming Total Score is column H)*

* To calculate average **Attendance (%)** for the CSE department:
  Use **AVERAGEIF**:
  `=AVERAGEIF(C2:C100, "CSE", D2:D100)`
  *(C = Department, D = Attendance (%))*

**Effect:** Understand overall and departmental student performance trends.

---

## Step 3: Sort and Filter Data

* Sort students by **Total Score** descending to see top performers.
* Filter by **Department** to view specific groups.

**How:** Use Excel’s Sort & Filter tool on columns.

**Effect:** Helps focus on specific data segments or rank students easily.

---

## Step 4: Conditional Formatting

Highlight critical values automatically.

**Examples:**

* Highlight attendance less than 75%:
  Use conditional formatting → New Rule → Use formula:
  `=$D2<75` and choose a red fill.
* Highlight Total Scores above 80 in green for high achievers.

**Effect:** Visual cues for identifying students needing attention or excelling.

---

## Step 5: Charts

Create charts to visualize data distribution.

**Examples:**

* **Bar Chart:** Average Total Scores by Department.
* **Pie Chart:** Percentage of students per Department.

**How:** Insert → Charts → Choose chart type → Select data.

**Effect:** Makes data easier to understand at a glance.

---

## Step 6: Pivot Tables

Summarize and analyze large data sets quickly.

**Example:**

* Create a pivot table to show average Assignment Score, Lab Score, and Final Exam Score by Department.

**Effect:** Dynamic summaries that can be filtered or expanded easily.

---

## Step 7: Identify Top Performers

Find students with highest Total Scores.

**Example:**

* Use **LARGE** formula to find top scores:
  `=LARGE(H2:H100,1)` returns highest score.
* Use **INDEX MATCH** to find corresponding student:
  `=INDEX(B2:B100,MATCH(LARGE(H2:H100,1),H2:H100,0))`

**Effect:** Quickly spot best students for recognition or analysis.

---

## Step 8: Attendance Analysis

Identify students with poor attendance for follow-up.

**Example:**

* Filter attendance below 75% using filter or conditional formatting.

**Effect:** Helps focus on students who may need support or warning.

---

# Summary

This Excel project helps in cleaning, analyzing, and visualizing student academic data effectively. Using Excel formulas, filters, conditional formatting, charts, and pivot tables, we can gain insights into student performance by department and overall.

