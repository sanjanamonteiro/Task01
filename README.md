 # Titanic Dataset Preprocessing and Outlier Removal

This project demonstrates a typical data preprocessing workflow on the Titanic dataset using Python and popular data science libraries. The code covers the following steps:

## Steps Performed

1. **Data Import and Exploration**
    - Load the Titanic dataset with Pandas.
    - Display dataset columns, preview data, check datatypes, summary statistics, and missing values.

2. **Handling Missing Values**
    - Fill missing values in the `Age` column using the median.
    - Fill missing values in the `Embarked` column using the mode.
    - Drop the `Cabin` column due to excessive missing data.

3. **Encoding Categorical Features**
    - Convert the `Sex` column to numerical values (`male`=0, `female`=1).
    - Apply one-hot encoding to the `Embarked` column (dropping the first category to avoid multicollinearity).

4. **Standardizing Numerical Features**
    - Standardize the `Age` and `Fare` columns using `StandardScaler` from `scikit-learn` so that they have mean 0 and standard deviation 1.

5. **Outlier Visualization and Removal**
    - Visualize outliers in the `Age` and `Fare` columns using boxplots before and after removing outliers.
    - Remove outliers using the IQR (Interquartile Range) method:
        - Any value lying outside `[Q1 - 1.5*IQR, Q3 + 1.5*IQR]` is considered an outlier and removed.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

Install the necessary packages using pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## How to Use

1. Place the Titanic dataset CSV file at the specified path (e.g., `/content/Titanic-Dataset.csv`).
2. Run the code cells sequentially in a Jupyter Notebook or Python environment.
3. Inspect the output for each step, especially the plots for outlier detection.

## Key Points

- **Missing Data Handling:** Uses statistical imputation (median/mode) for missing values, and removes columns with excessive missing data.
- **Feature Engineering:** Encodes categorical variables for use in machine learning models.
- **Standardization:** Normalizes numerical features to improve model performance.
- **Outlier Removal:** Cleans the data by removing extreme values that could skew analysis or modeling results.

## Visualization

The code provides boxplots before and after removing outliers to help you visually confirm the impact of the outlier removal step.

---

This pipeline is a solid foundation for further analysis, visualization, or building predictive models for the Titanic dataset.
