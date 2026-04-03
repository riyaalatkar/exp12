## Lab Report: Categorical Data Analysis
**Student Name:** Riya Latkar
**PRN:** 25070123092
**Experiment No:** 12

### 1. Aim
To perform descriptive and comparative analysis on categorical datasets using the Python `pandas` library, focusing on frequency distributions, cross-tabulations, and data filtering.

### 2. Theory
Categorical data represents types of data which may be divided into groups. In Python, the `pandas` library provides powerful tools for this:
* **Frequency Distribution:** Identifying how often each category (e.g., 'Grade' or 'Department') occurs.
* **Cross-tabulation (Crosstab):** A method to compute a simple cross-tabulation of two or more factors, showing the relationship between variables (e.g., Gender vs. Grade).
* **Normalization:** Converting raw counts into percentages or proportions to understand the relative distribution.
* **Grouping & Filtering:** Segmenting data based on specific criteria to extract targeted insights.

### 3. Logic
The analysis follows a three-step logical flow:
1.  **Exploration:** Loading the data and viewing the first few rows to understand the structure.
2.  **Univariate Analysis:** Counting occurrences of single variables (value counts) to find the most/least common categories.
3.  **Bivariate Analysis:** Using `crosstab` and `groupby` to see how two variables interact (e.g., which department has the most female students).

### 4. One-Liner Code Explanations
* `pd.read_csv('Expt11.csv')`: Loads the dataset from a CSV file into a DataFrame.
* `df['Grade'].value_counts()`: Calculates the total number of occurrences for each unique grade.
* `normalize=True * 100`: Converts frequency counts into percentages.
* `pd.crosstab(df['Gender'], df['Grade'])`: Creates a frequency table showing the intersection of Gender and Grade.
* `df.groupby('Department')['Gender'].value_counts()`: Groups the data by department and then counts the gender distribution within each.
* `pf['Category'].unique()`: Lists all distinct categories present in the column without duplicates.
* `pf[pf['Category']=='Electronics']`: Filters the DataFrame to show only rows where the category is 'Electronics'.
* `pf.sort_values(by='Category')`: Reorganizes the rows alphabetically based on the 'Category' column.

### 5. Algorithm
1.  **Import** the `pandas` library.
2.  **Load** the dataset from an external file or a manually defined dictionary.
3.  **Inspect** the data using `.head()` or by printing the DataFrame.
4.  **Perform Frequency Analysis** on key columns using `.value_counts()`.
5.  **Generate Contingency Tables** using `pd.crosstab()` to observe relationships between two categorical variables.
6.  **Apply Normalization** to the index or columns to get percentage-based insights.
7.  **Filter and Sort** the data to isolate specific segments (e.g., specific departments or order types).

### 6. Conclusion
By completing this experiment, I have mastered the ability to manipulate and analyze categorical data in Python. I successfully used `pandas` to summarize data distributions and uncover hidden relationships between variables (such as Departmental grading patterns). These skills are foundational for performing Exploratory Data Analysis (EDA) in any data science project.

---
