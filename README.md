# Real-World Dataset Analysis Project

A complete exploratory data analysis project using the **Diabetes dataset** distributed through scikit-learn.

## Project objective

Analyze a real-world dataset from a reliable source and demonstrate the complete data-analysis workflow:

- Understand the dataset and its analytical context
- Inspect structure, data types, distributions, missing values, and duplicates
- Clean and preprocess the data
- Detect potential outliers using the IQR method
- Perform exploratory data analysis with Pandas and NumPy
- Create meaningful statistical visualizations
- Analyze relationships and correlations
- Present findings, limitations, and practical recommendations

## Dataset

**Dataset:** Diabetes dataset  
**Source:** scikit-learn's `load_diabetes()` dataset  
**Observations:** 442  
**Variables:** 11 total — 10 predictor variables + 1 continuous target

The dataset contains baseline measurements including age, sex, body mass index (BMI), blood pressure, and six blood-serum measurements. The target is a quantitative measure of disease progression one year after baseline.

The dataset is used here for educational data analysis. It should **not** be interpreted as a clinical diagnostic dataset or used to make medical decisions.

## Key analysis areas

1. Dataset context and business/analytical objective
2. Dataset structure and data types
3. Missing-value and duplicate checks
4. Data cleaning and preprocessing
5. IQR-based outlier screening
6. Distribution analysis
7. Box plots
8. Scatter plots
9. Correlation matrix
10. BMI quartile comparison
11. Key findings and recommendations

## Repository structure

```text
real-world-dataset-analysis-project/
├── Real_World_Dataset_Analysis_Project.ipynb
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
├── data/
│   ├── diabetes_dataset.csv
│   └── README.md
├── outputs/
│   └── README.md
└── reports/
    └── REPORT_DESCRIPTION.md
```

## Run locally

```bash
python -m venv .venv
```

Windows:
```bash
.venv\Scripts\activate
```

macOS/Linux:
```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter:

```bash
jupyter notebook
```

Open `Real_World_Dataset_Analysis_Project.ipynb` and run all cells.

## Main findings

The exploratory analysis shows that:

- The dataset contains 442 observations and 11 analytical columns.
- The packaged data contains no missing values or duplicate rows after quality checks.
- The predictors are numerical and standardized.
- A subset of variables has noticeably stronger linear association with the target than the remaining predictors.
- BMI has a positive association with the target, which is also visible when comparing average target values across BMI quartiles.
- Potential outliers exist in some variables, but they should be investigated rather than automatically deleted.
- Correlation measures association and does not establish causation.

## Responsible interpretation

This is an educational EDA project. Correlations and group differences should not be interpreted as causal or clinical conclusions. A production-grade analysis would require domain expertise, appropriate statistical modeling, validation, and careful consideration of data provenance and population representativeness.
