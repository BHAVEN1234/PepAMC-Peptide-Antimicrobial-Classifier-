# Machine Learning Model Evaluation and Feature Selection Framework 🚀

## Overview

This Python project evaluates the performance of machine learning models on various datasets and implements a genetic algorithm for feature selection. It automates preprocessing, hyperparameter tuning, cross-validation, and feature selection to provide comprehensive evaluation summaries.

## ✨ Features

- 📥 **Automatic Dataset Loading**: Seamlessly fetches datasets from sklearn and OpenML.
- 🤖 **Baseline Model Evaluation**: Uses KNeighborsClassifier to evaluate datasets.
- ⚙️ **Hyperparameter Optimization**: Implements GridSearchCV for tuning key hyperparameters.
- 📊 **Cross-Validation Results**: Computes mean and standard deviation of model performance metrics.
- 🧬 **Genetic Algorithm Feature Selection**: Implements SAGAFS-GA for optimized feature selection.
- 📈 **Performance Visualization**: Plots fitness score evolution over generations.
- 📝 **Formatted Output**: Displays results in a clean, tabular format and saves them as CSV files.

## 📚 Libraries Used

- 📊 pandas: For data manipulation and analysis.
- 🔢 numpy: For numerical operations.
- 🤖 scikit-learn: For machine learning model evaluation and dataset handling.
- 📉 matplotlib and seaborn: For data visualization.
- 🕰️ time: For performance timing.
- 📁 os: For file and directory operations.

## 📝 Code Explanation

### Baseline Evaluation

The `Baseline()` function evaluates models across multiple datasets:

- Preprocessing: Uses ColumnTransformer and Pipeline for feature handling.
- Hyperparameter Tuning: Optimizes model parameters with GridSearchCV.
- Cross-Validation: Evaluates models using StratifiedKFold with customizable metrics.

### SAGAFS-GA Implementation

The `SAGAFS_GA` class implements a genetic algorithm for feature selection:

- Initialization: Sets up algorithm parameters and population.
- Fitness Function: Evaluates feature subsets using cross-validation.
- Evolution: Implements selection, crossover, and mutation operations.
- Visualization: Plots fitness scores over generations.

## 📋 Output

The framework generates:

1. A table summarizing baseline model performance for each dataset.
2. CSV files with detailed results and timing information.
3. Plots showing the evolution of fitness scores for the genetic algorithm.

## 🔧 Customization

### Modifying Datasets

To add or remove datasets, update the `datasets` list:

```python
datasets = [
    ("Iris", load_iris),
    ("Custom Dataset", lambda: fetch_openml(name="custom", version=1))


]
```
### Modify the SAGAFS_GA initialization in the main loop:
```python
ga_fs = SAGAFS_GA(estimator=estimator, cv=cv, scoring='accuracy', 
                  population_size=20, generations=50)
```
## 🔍 Usage
1)Clone the repository and navigate to the project directory.
2)Set up a Python virtual environment and activate it.
3)Install required dependencies: pip install -r requirements.txt
4)Run the evaluation script: python main_script.py
5)Check console output and generated CSV files for results.

## 📄 License

This project is licensed under the MIT License - see the `LICENSE` file for details.

---

## 🙌 Acknowledgments

Thanks to the developers of `sklearn`, `OpenML`, and `tabulate` for making dataset loading and formatting so convenient.
