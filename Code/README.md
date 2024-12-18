# 🧬 SAGAFS-GA: Supercharged Feature Selection for Machine Learning 🚀

## 🚀 Overview
SAGAFS-GA is a cutting-edge feature selection algorithm that combines the power of Simulated Annealing (SA) with Genetic Algorithms (GA) to supercharge your machine learning models. This innovative tool optimizes feature subsets, enhancing classification performance while keeping your models lean and efficient.

---

## ✨ key Features

- 🎯 **Adaptive Feature Selection:** Dynamically selects the most impactful features.
- 🔧 **Hyperparameter Optimization:** Seamless integration with scikit-learn's GridSearchCV.
- 🔌 **Flexible Estimator Support:** Works with a wide range of scikit-learn classifiers.
- 📊 **Advanced Performance Metrics:** Evaluates models using accuracy, Matthews Correlation Coefficient, and F1-score.
- 📈 **Insightful Visualizations:** Plots fitness evolution and feature importance heatmaps.

---

## 📚 Libraries Used

- 📊 **pandas**: For data manipulation and analysis.
- 🔢 **numpy**: For numerical operations.
- 🤖 **scikit-learn**: For machine learning model evaluation and dataset handling.
- 🖋 **tabulate**: For generating formatted tables.

---

## 🚀 Quick Start
```python
from sagafs_ga import SAGAFS_GA
from sklearn.neighbors import KNeighborsClassifier
from sklearn.model_selection import StratifiedKFold
from sklearn.datasets import load_iris

# Load your data
X, y = load_iris(return_X_y=True)

# Configure SAGAFS-GA
saga_fs = SAGAFS_GA(
    estimator=KNeighborsClassifier(),
    cv=StratifiedKFold(n_splits=5),
    scoring='accuracy',
    population_size=20,
    generations=10,
    param_grid={
        'n_neighbors': [3, 5, 7],
        'weights': ['uniform', 'distance']
    }
)

# Unleash the power of SAGAFS-GA
saga_fs.fit(X, y)

# Visualize the magic
saga_fs.plot_fitness_over_generations()
saga_fs.plot_heatmap(saga_fs.best_individual, [f"Feature_{i}" for i in range(X.shape[1])])
```
## 🧠 Advanced Capabilities

- 🧬 **SSOCF Crossover:** Sophisticated crossover strategy for optimal feature combination.
- 🔄 **Dynamic Rate Adaptation:** Auto-adjusts mutation and crossover rates for peak performance.
- 👑 **Elitism:** Preserves the best solutions across generations.
- 🧹 **Smart Preprocessing:** Handles various data types and manages missing values automatically
---
---
## 📊 Supported Datasets
SAGAFS-GA has been tested on a variety of datasets, including:
- Iris
- Breast Cancer Wisconsin (Diagnostic and Original)
- Spambase
- Heart Disease
- Glass Identification
- Ionosphere
- Arrhythmia
- Wine
- Vehicle
- Sonar
---
## 🔧 Customization

### Modifying Datasets
To add or remove datasets, update the `datasets` list:
```python
datasets = [
    ("Iris", load_iris),
    ("Custom Dataset", lambda: fetch_openml(name="custom", version=1))
]
```
## 🔍 Example Usage

To run the evaluation:

1. **Clone the repository** and navigate to the project directory:

    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```

2. **Set up a Python virtual environment**:

    Create and activate a virtual environment to keep dependencies isolated.

    ```bash
    # Create a virtual environment named 'venv'
    python3 -m venv venv
    ```

3. **Activate the virtual environment**:

    - On **Linux/macOS**:
    
      ```bash
      source venv/bin/activate
      ```

    - On **Windows**:
    
      ```bash
      venv\Scripts\activate
      ```

4. **Install the required dependencies**:

    Ensure you have a `requirements.txt` file in the project directory that lists all necessary packages. Install the dependencies with:

    ```bash
    pip install -r requirements.txt
    ```

5. **Run the evaluation script**:

    ```bash
    python baseline_evaluation.py
    ```

6. **Check the results**:

    View the console output for a formatted table summarizing the results, or open the saved CSV file for a complete summary of model performance across datasets.

7. **Deactivate the virtual environment** (when done):

    ```bash
    deactivate
    ```

This guide provides a full setup for running the evaluation script, including setting up and activating a virtual environment, installing dependencies, and deactivating the environment after completion.

## 📄 License

This project is licensed under the MIT License - see the `LICENSE` file for details.

---

## 🙌 Acknowledgments

Thanks to the developers of `sklearn`, `OpenML`, and `tabulate` for making dataset loading and formatting so convenient.


