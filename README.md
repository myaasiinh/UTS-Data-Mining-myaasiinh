# Data Mining & Business Intelligence - UTS 2024

**Instructor**: Sam FCH  
**Type**: Online  
**Duration**: 72 Hours  

---

## Description
This project involves analyzing and cleaning a dataset of retail transactions (`Online Retail-unclean.xlsx`). The dataset contains transactions from various countries and includes missing data. The tasks include data cleaning, aggregation, and sampling.

---

## Tasks

### Task 1: Missing Data Analysis

#### Questions
1. **Which columns have missing data?**
   - Columns with missing data and their percentages:
     ```
     CustomerID     24.927802%
     Description     0.268311%
     Country         0.001476%
     UnitPrice       0.000923%
     ```

2. **Which countries have missing data?**
   - Countries with missing data:
     ```
     United Kingdom    133600
     EIRE                 711
     Hong Kong            288
     Unspecified          202
     Switzerland          125
     France                66
     Israel                47
     Portugal              39
     Australia              5
     Singapore              3
     Canada                 3
     Bahrain                2
     ```

---

### Task 2: Data Cleaning

#### 2a. Clean the missing data in the dataset
The missing data was cleaned as follows:
- **Numerical Columns**: Filled with the **median** value.
  - Example: `UnitPrice` was filled with the median value `2.08`.
- **Categorical Columns**: Filled with the **mode** value.
  - Example: `Description` was filled with the mode value `'WHITE HANGING HEART T-LIGHT HOLDER'`.
  - Example: `Country` was filled with the mode value `'United Kingdom'`.
- **CustomerID**: Filled using the **mode within each country**. If a mode was unavailable for a group, the default value `0` was used.

After cleaning, no missing values remained in the dataset:


#### 2b. Explanation of the Data Cleaning Process
1. **Numerical Columns**:
   - The median was chosen to handle missing values because it is not affected by extreme outliers.
2. **Categorical Columns**:
   - The mode was used as it represents the most frequent and logical value for categorical data.
3. **CustomerID**:
   - Values were filled with the mode of the country group to maintain relevance. If all values in a group were missing, a fallback value of `0` was used to ensure no missing values remained.

---

### Task 3: Justify Missing Data Imputation
1. **Numerical Columns**:
   - Median was used to avoid distortion by outliers.
2. **Categorical Columns**:
   - Mode was used to maintain consistency and logical replacement.
3. **CustomerID**:
   - The mode within each country ensured contextually relevant imputations. The fallback of `0` was used only when no mode was available, preserving data completeness.

---

### Task 4: Aggregation
The total `UnitPrice` was aggregated for each country by month. The results were saved in the file:
- **Output**: `Aggregasi.xlsx`

---

### Task 5: Sampling
Stratified sampling was performed for each country. Sample sizes were determined using:
1. `alpha = 0.03`
2. `alpha = 0.01`

The results were saved in the following files:
- **Sampling Alpha 0.03**: `Sampling_alpha_003.xlsx`
- **Sampling Alpha 0.01**: `Sampling_alpha_001.xlsx`

---

## Instructions

1. **Deliverables**:
   - Task 1 (1a and 1b), Task 2b, and Task 3 should be written in a Word document named `Jawaban.docx`.
   - Task 2a: Save the cleaned dataset in an Excel file named `Online-Retail-Clean.xlsx`.
   - Task 4: Save the aggregation results in an Excel file named `Aggregasi.xlsx`.
   - Task 5: Save the sampling results in an Excel file named `Sampling.xlsx` for both `alpha` values.

2. **Submission**:
   - Upload all files (`Jawaban.docx`, `Online-Retail-Clean.xlsx`, `Aggregasi.xlsx`, `Sampling.xlsx`) to a new GitHub repository.
   - Submit the GitHub repository link in the designated UTS section on Sinau.

---

## Notes

- You may use Python or Jupyter Notebook for data cleaning, aggregation, and sampling. Submitting the Python script or notebook file will earn an additional 70% of your score.
- The additional score can be used as a bonus for other assignments.

---

## Warning

- **Plagiarism**: Plagiarism will not be tolerated! Answers must be completed independently. If identical answers (copy-paste) are found among students, a grade of **D** will be assigned.

Good luck with your UTS!

