# Pandas Notebook Guide

This notebook provides a comprehensive introduction to the pandas library in Python, covering fundamental data structures, essential operations, and techniques for handling missing data and combining DataFrames.

## Table of Contents

1.  **Introduction to Pandas**
    *   Overview of pandas and its importance for data manipulation.
    *   Explanation of pandas data structures: Series and DataFrame.

2.  **Series**
    *   Creating Series from lists and dictionaries.
    *   Accessing elements by index.
    *   Adding Series.

3.  **DataFrame**
    *   Creating DataFrames from lists and dictionaries.
    *   Selecting specific columns and rows.
    *   Accessing individual values by row and column index.
    *   Performing arithmetic operations on DataFrames.
    *   Applying boolean logic to DataFrames.
    *   Inserting and deleting columns.

4.  **CSV File Handling**
    *   Creating CSV files from DataFrames.
    *   Reading data from CSV files using various parameters:
        *   `nrows`: Reading a specific number of rows.
        *   `usecols`: Selecting specific columns.
        *   `skiprows`: Skipping rows by index.
        *   `index_col`: Setting a column as the index.
        *   `header`: Specifying the header row.
        *   `names`: Assigning custom column names.
        *   `dtype`: Changing the data type of columns.
    *   Accessing DataFrame information (`index`, `columns`, `describe`).
    *   Viewing head and tail of the DataFrame.
    *   Slicing rows.
    *   Converting to NumPy array.
    *   Sorting by index.
    *   Modifying data using `.loc`.
    *   Accessing data using `.loc` and `.iloc`.
    *   Dropping columns.

5.  **Handling Missing Data**
    *   **`dropna()`**: Removing rows or columns with missing values.
        *   Using `axis` to specify rows or columns.
        *   Using `how` ("any" or "all") to control dropping behavior.
        *   Using `subset` to drop rows with NaN in specific columns.
        *   Using `thresh` to drop rows with less than a specified number of non-NaN values.
    *   **`fillna()`**: Filling missing values with a specified value or method.
        *   Filling with a single value.
        *   Filling with different values for different columns using a dictionary.
        *   Using `method` ("ffill" or "bfill") to fill from previous or next values.
        *   Using `limit` to fill a limited number of consecutive NaN values.
        *   Using `limit_direction` ("forward", "backward", "both") to control fill direction.
        *   Using `limit_area` ("inside" or "outside") to control the area of filling.
        *   Using `inplace` to modify the DataFrame directly.

6.  **Handling Missing Data (Replace and Interpolate)**
    *   **`replace()`**: Replacing specific values in the DataFrame.
        *   Replacing a single value.
        *   Replacing multiple values with a single value using a list.
        *   Using `regex` to replace values based on regular expressions.
        *   Replacing values using a dictionary and regular expressions.
        *   Using `method` ("ffill" or "bfill") for replacement.
        *   Using `limit` to limit the number of replacements.
        *   Using `inplace` to modify the DataFrame directly.
    *   **`interpolate()`**: Filling missing numerical data using interpolation methods.
        *   Default linear interpolation.
        *   Using `method` to specify different interpolation techniques.
        *   Using `axis` to interpolate along rows or columns.
        *   Using `limit_direction` and `limit` to control interpolation.
        *   Using `limit_area` to control the area of interpolation.
        *   Using `inplace` to modify the DataFrame directly.

7.  **Merging and Concatenating DataFrames**
    *   **`merge()`**: Joining DataFrames based on common columns (similar to SQL joins).
        *   Merging with default inner join.
        *   Merging with different column names using `on`.
        *   Using `how` ("left", "right", "outer") to control join type.
        *   Using `indicator` to show the origin of merged data.
        *   Merging based on index using `left_index` and `right_index`.
        *   Using `suffixes` to handle duplicate column names after merging by index.
    *   **`concat()`**: Stacking DataFrames or Series vertically or horizontally.
        *   Concatenating Series.
        *   Concatenating DataFrames.
        *   Handling different column names.
        *   Using `axis` to concatenate along rows or columns.
        *   Using `join` ("inner" or "outer") to control how columns are handled.
        *   Using `keys` to create a hierarchical index for concatenated DataFrames.
        *   Concatenating DataFrames and Series with different dimensions.

8.  **Group By**
    *   Grouping data by a specific column.
    *   Iterating through groups.
    *   Accessing a specific group.
    *   Performing aggregate functions on groups (`min`, `max`, `mean`).
    *   Converting grouped data into a list of tuples.

9.  **Join**
    *   Joining DataFrames based on their index.
    *   Handling missing data during joining.
    *   Joining with different indices.
    *   Using `how` ("right", "left", "inner", "outer") to control join type.
    *   Using `lsuffix` and `rsuffix` to handle duplicate column names after joining.
