# Comprehensive Study on Performance of Students due to Alcohol Consumption

An exploratory data analysis (EDA) of the UCI "Student Alcohol Consumption" dataset, examining how alcohol use and related social/family factors relate to student academic performance.

## Table of Contents

- [About](#about)
- [Contents](#contents)
- [Analysis Overview](#analysis-overview)
- [Dataset](#dataset)
- [Prerequisites](#prerequisites)
- [Usage](#usage)

## About

The dataset was collected from a survey of students in a secondary school math course. It contains social, gender, and study-related attributes for each student alongside their final grades. This project focuses specifically on how alcohol consumption and related lifestyle/family factors (e.g. address, parental cohabitation status, parents' education/jobs, study time, family relations, free time, going out, health, absences) relate to student performance (grades `G1`, `G2`, `G3`).

## Contents

| File | Description |
|---|---|
| [FinalComprehensive Study.ipynb](FinalComprehensive%20Study.ipynb) | Main Jupyter notebook containing the full analysis |
| [student-mat.csv](student-mat.csv) | Source dataset (student math course performance, UCI Student Alcohol Consumption dataset) |
| [Comprehensive Study.pdf](Comprehensive%20Study.pdf) | Exported PDF report of the notebook |

## Analysis Overview

The notebook (`FinalComprehensive Study.ipynb`) walks through:

1. **Data exploration** – dataset description, loading the CSV, and reviewing categorical and numerical features.
2. **Correlation analysis** – relationships between features and final grades.
3. **Pivot tables & box plots** – summarizing performance across categorical groupings.
4. **Feature importance** – using several classifiers (Random Forest, AdaBoost, Extra Trees, Decision Tree, KNN, Naive Bayes, Logistic Regression, SVM, SGD) to assess which factors most influence performance.
5. **Outlier detection** – using the IQR method.
6. **Hypothesis testing** – statistical tests (t-tests) addressing questions such as:
   - Does study time differ by gender?
   - Does study time depend on being in a romantic relationship?
   - Does the number of past class failures depend on gender?
   - Does the number of absences depend on gender?

## Dataset

`student-mat.csv` contains 395 student records with 33 attributes, including:

- **Demographics**: `school`, `sex`, `age`, `address`, `famsize`, `Pstatus`
- **Family background**: `Medu`, `Fedu`, `Mjob`, `Fjob`, `guardian`
- **School-related**: `reason`, `traveltime`, `studytime`, `failures`, `schoolsup`, `famsup`, `paid`, `activities`, `nursery`, `higher`, `internet`
- **Social/lifestyle**: `romantic`, `famrel`, `freetime`, `goout`, `Dalc` (workday alcohol consumption), `Walc` (weekend alcohol consumption), `health`, `absences`
- **Grades**: `G1`, `G2`, `G3` (first, second, and final period grades)

Source: [UCI Machine Learning Repository – Student Alcohol Consumption](https://archive.ics.uci.edu/dataset/320/student+performance)

## Prerequisites

- **Python 3.x**
- **Jupyter** environment to run the notebook (JupyterLab, Jupyter Notebook, or VS Code with the Jupyter extension)
- The following Python libraries:
  - `pandas`, `pandas_profiling`
  - `numpy`
  - `matplotlib`, `seaborn`, `plotly`
  - `scipy`
  - `scikit-learn`

Install the libraries with:

```bash
pip install pandas pandas_profiling numpy matplotlib seaborn plotly scipy scikit-learn jupyter
```

## Usage

1. Install the requirements above (a Jupyter environment such as JupyterLab or VS Code with the Jupyter extension is also required).
2. Open `FinalComprehensive Study.ipynb`.
3. Ensure `student-mat.csv` is in the same directory as the notebook.
4. Run the cells in order.

A pre-rendered version of the analysis is also available in `Comprehensive Study.pdf`.
