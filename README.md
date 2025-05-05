# Student Performance Analysis

This project contains Python code for exploring and visualizing student performance data. The analysis focuses on understanding the distribution of final grades and the relationship between various factors such as study hours and school support.

## Libraries Used

* **pandas (pd):** For data manipulation and reading CSV files.
* **matplotlib.pyplot (plt):** For creating basic plots and customizations.
* **seaborn (sns):** For creating more advanced and statistically-oriented visualizations.

## Data Source

The analysis relies on a CSV file named `Student.csv`. The script attempts to read this file using pandas. If the file is not found, an error message will be printed.

## Data Exploration

The script includes the following steps for initial data exploration:

1.  **Handling Errors:** Attempts to read the `Student.csv` file and includes error handling for the case where the file is not found.
2.  **Printing the First Few Rows:** `df.head()` is used to display the initial rows of the DataFrame, providing a glimpse of the data.
3.  **Getting Summary Statistics:** `df.describe()` provides descriptive statistics for the numerical columns in the DataFrame (e.g., count, mean, standard deviation, min, max, quartiles).
4.  **Getting the Shape of the DataFrame:** `df.shape` returns the number of rows and columns in the DataFrame.
5.  **Getting Information about Columns and Their Values:** `df.info()` provides a concise summary of the DataFrame, including data types and non-null values.
6.  **Checking for Missing Values:** `df.isnull().sum()` calculates the number of missing values in each column.

## Data Visualization

The script generates the following plots to visualize different aspects of the data:

1.  **Bar Plot of Final Grade by School Support:**
    * Uses `sns.catplot()` with `kind='bar'` to show the average final grade for students with and without school support.
    * Sets the figure title to "Final Grade Distribution by School Support".
    * Sets the titles of the individual subplots based on the 'school_support' categories.
    * **Observation:** Data shows that students in those receiving support and those that do not the performance is almost similar.

2.  **Scatter Plot of Study Hours vs. Final Grade:**
    * Uses `sns.relplot()` with `kind='scatter'` to visualize the relationship between study hours and final grade.
    * Sets the figure title to "Relationship Between Study Hours and Final Grade".
    * **Observation:** The scatter plot shows there is no relationship between the number of study hours and final grade.

3.  **Histogram of Final Grades:**
    * Uses `plt.hist()` to display the distribution of final grades.
    * Labels the x-axis as "Final Grade" and the y-axis as "Frequency".
    * Sets the plot title to "Distribution of Final Grades".
    * **Observation:** The distribution doesn't seem strongly skewed to the left (negatively skewed) or the right (positively skewed).

4.  **Count Plot of School Support:**
    * Uses `sns.catplot()` with `kind='count'` to show the number of students with and without school support.
    * Orders the bars to display 'yes' before 'no'.
    * Sets the figure title to "Number of Students by School Support".
    * Labels the y-axis as "Number of Students".
    * **Observation:** The number of students who received school support are slightly more than those who did not receive support.

## How to Run the Script

1.  Make sure you have Python installed on your system.
2.  Install the necessary libraries: `pip install pandas matplotlib seaborn`
3.  Save the provided Python code as a `.py` file (e.g., `student_analysis.py`).
4.  Ensure that the `Student.csv` file is in the same directory as the Python script, or provide the correct path to the file in the `pd.read_csv()` function.
5.  Run the script from your terminal: `python student_analysis.py`

The script will print some initial data information and display the generated plots.

## Further Analysis

This script provides a basic exploration and visualization of the student performance data. Further analysis could involve:

* Investigating the reasons behind the lack of a strong correlation between study hours and final grades.
* Exploring other potential factors that might influence final grades.
* Performing statistical tests to determine the significance of observed differences between groups (e.g., students with and without school support).
* Building predictive models to forecast student performance.