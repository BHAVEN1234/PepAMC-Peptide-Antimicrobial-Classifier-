# 📊 Baseline Model Evaluation Framework

## 🚀 Overview
This Python script evaluates the performance of machine learning models on various datasets fetched from popular repositories such as `sklearn` and `OpenML`. It automates preprocessing, hyperparameter tuning, and cross-validation to provide a comprehensive evaluation summary. Results are presented in a structured table format and saved for further analysis.

---

## ✨ Features

- 📥 **Automatic Dataset Loading**: Seamlessly fetches datasets from `sklearn` and `OpenML`.
- 🤖 **Baseline Model Evaluation**: Uses `KNeighborsClassifier` to evaluate datasets with accuracy and consistency.
- ⚙️ **Hyperparameter Optimization**: Implements `GridSearchCV` for tuning key hyperparameters.
- 📊 **Cross-Validation Results**: Computes mean and standard deviation of model performance metrics.
- 📝 **Formatted Output**: Displays results in a clean, tabular format and saves them as a CSV file.

---

## 📚 Libraries Used

- 📊 **pandas**: For data manipulation and analysis.
- 🔢 **numpy**: For numerical operations.
- 🤖 **scikit-learn**: For machine learning model evaluation and dataset handling.
- 🖋 **tabulate**: For generating formatted tables.

---

## 📝 Code Explanation

This script provides a systematic approach to evaluating baseline models across multiple datasets. Below is a breakdown of its components:

### 1. Dataset Handling

The `datasets` list contains popular datasets loaded either via `sklearn` or `OpenML`. Each dataset is processed with error handling to ensure compatibility.

- **From `sklearn`**: Datasets such as Iris and Wine are fetched directly.
- **From OpenML**: More diverse datasets are accessed by name or ID using `fetch_openml()`.

### 2. Baseline Evaluation

The `Baseline()` function is the core of the script. It performs the following:
- **Preprocessing**: Uses `ColumnTransformer` and `Pipeline` to handle categorical and numerical features.
- **Hyperparameter Tuning**: Optimizes model parameters with `GridSearchCV` (optional).
- **Cross-Validation**: Evaluates the model using `StratifiedKFold` with customizable scoring metrics such as `accuracy`, `f1_score`, and `matthews_corrcoef`.

### 3. Results Compilation

All results are aggregated into a `pandas` DataFrame, formatted using `tabulate`, and saved as a CSV file for future reference.

---

## 📋 Output

The script generates a table summarizing the performance of the baseline model for each dataset. Below is a sample output:

| Dataset                                   |   KNeighborsClassifier_AUC |   KNeighborsClassifier_AUC_STD |
|-------------------------------------------|----------------------------|---------------------------------|
| Arrhythmia                                |                   0.57744  |                     0.0148868  |
| Australian                                |                   0.856522 |                     0.0351729  |
| DNA                                       |                   0.836489 |                     0.0176211  |
| German Number (Credit Dataset)            |                   0.721    |                     0.0314484  |
| Glass                                     |                   0.668398 |                     0.0673421  |
| Heart                                     |                   0.819188 |                     0.0455073  |
| Hillvalley                                |                   0.499187 |                     0.00633222 |
| Ionosphere                                |                   0.695556 |                     0.126996   |
| Iris                                      |                   0.853333 |                     0.0718022  |
| Multiple Features                         |                   0.8055   |                     0.0301206  |
| Musk 1                                    |                   0.831495 |                     0.165486   |
| Sonar                                     |                   0.52381  |                     0.0897212  |
| Spambase                                  |                   0.798963 |                     0.0246224  |
| Vehicle                                   |                   0.917297 |                     0.0258821  |
| WBC (Breast Cancer Wisconsin Original)    |                   0.95     |                     0.0368394  |
| WBDC (Breast Cancer Wisconsin Diagnostic) |                   0.685432 |                     0.0409327  |
| Waveform                                  |                   0.6298   |                     0.0206194  |
| Wine                                      |                   0.619608 |                     0.0994152  |
| Zoo                                       |                   1        |                     0          |

---

## 🔧 Customization

### Modifying Datasets
To add or remove datasets, update the `datasets` list:
```python
datasets = [
    ("Iris", load_iris),
    ("Custom Dataset", lambda: fetch_openml(name="custom", version=1))
]

--
## 🔍 Example Usage

To run the evaluation:

1. Clone the repository and navigate to the directory.

2. Run the script:

   ```bash
   python baseline_evaluation.py
