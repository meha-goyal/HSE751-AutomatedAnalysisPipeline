# HSE751-AutomatedAnalysisPipeline

# Automated Analysis Pipeline Notebook

https://drive.google.com/file/d/1sjADrNhoLPWDlbIC5ZUDVrDfhn4hBO8U/view?usp=sharing

## Purpose

This notebook is an automated, reproducible analysis pipeline for health data science, where The prediction task is to classify whether a patient has diabetes from diagnostic measurements. The notebook uses conditional logic to automate decisions at each stage, including data ingestion, cleaning, exploratory analysis, inferential statisitcs, and machine learning.

## How to Run

1. Open the notebook linked above
2. Select Run All at the top
3. When the first code cell asks you to upload a file, select the dataset CSV (`Example_Dataset_Diabetes.csv`).
4. Confirm that the notebook completes without errors. The first cell should report 768 rows and 9 columns.

Cells with `# CHANGE` comments contain settings you can edit, such as variables, thresholds, and significance level.

## Requirements

If you open the notebook in Google Colab, it already includes most libraries. No local installation is needed when running in Colab.

The relevant libraries are:
- Python 3
- pandas, numpy, scipy, statsmodels
- scikit-learn
- matplotlib, seaborn
- phik (installed automatically by the notebook)
- openpyxl and pyarrow (only needed if you upload Excel or Parquet files)

To run locally instead, install the libraries with `pip install pandas numpy scipy statsmodels scikit-learn matplotlib seaborn phik` and replace the Colab upload cell with `pd.read_csv("your_file.csv")`.

## Assumptions and Limitations

The pipeline assumes specific columns, particularly: Pregnancies, Glucose, D_BP, Skin_Thickness, Insulin, BMI, Pedigree, Age, and Outcome. Other datasets need the variable names in the code updated. The outcome is binary (coded 0/1) and all predictors are numeric. Zeros in Glucose, D_BP, Skin_Thickness, Insulin, and BMI are treated as missing values. Missing predictors are filled with training-set medians.
