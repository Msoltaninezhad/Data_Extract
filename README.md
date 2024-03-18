# Directory-Based Data Aggregation Script

## Overview

This Python script is designed to automate the process of gathering specific data from `.mat` files (MATLAB format) stored in a structured directory hierarchy and compiling this information into a single Excel file. It utilizes libraries such as `os` for directory traversal, `scipy.io` for reading MATLAB files, and `pandas` for data manipulation and export. It's ideal for scenarios where data is spread across multiple directories, each representing different variables or conditions, and needs to be consolidated for analysis or reporting.

## Requirements

- Pandas: A powerful data analysis and manipulation library.
- SciPy: Used for importing `.mat` files, among other mathematical and scientific computing tasks.

To install the required libraries, run:

```shell
pip install pandas scipy
## Script Breakdown

### 1. Import Necessary Libraries
- `os`: For navigating the directory structure.
- `scipy.io`: For loading `.mat` files containing MATLAB variables.
- `pandas`: For creating and manipulating dataframes, and exporting the final data to an Excel file.

### 2. Set Up Base Directory
- `base_dir`: The root directory containing the subdirectories and `.mat` files to process. Modify `"path_to_your_folder"` to your actual path.

### 3. Data Collection Preparation
- Initializes a `pandas.DataFrame` to store the collected data, specifying column names that include three variables and two data points.

### 4. Directory Traversal and Data Extraction
- Walks through each subdirectory within the base directory.
- Checks for the presence of `outParams.mat` in directories.
- Extracts directory names as variable values and `.mat` file contents as data.
- Updates the dataframe with the extracted information.

### 5. Save the Aggregated Data
- The final dataframe is exported to an Excel file. Modify `"path_to_save\\data_file.xlsx"` to your desired save path.

## Usage
1. Update `base_dir` and `output_path` in the script to match your directory structure and desired output location.
2. Ensure that your Python environment has the necessary libraries installed.
3. Execute the script. The output will be an Excel file containing the aggregated data.



