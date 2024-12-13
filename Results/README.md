# 📝 Dataset Evaluation and Model Performance Summary

This project consists of a Python script that automatically loads, analyzes, and evaluates various machine learning datasets from popular repositories like `sklearn` and `OpenML`. The results include comprehensive summaries and performance evaluations, which are presented in an easy-to-read, well-structured table format using the `tabulate` library. This README outlines the datasets, their characteristics, and the machine learning models’ performance metrics.

---

## 📂 Data Loading Summary

The script loads multiple datasets and provides a detailed overview of each dataset’s structure, including the number of classes, features, feature types, and dataset size.

| 🗂 **Dataset**                               | 🏷 **Classes** | 📊 **Features** | 🔢 **Numerical** | 🔤 **Categorical** | 📏 **Size** |
|---------------------------------------------|----------------|----------------|------------------|--------------------|-------------|
| Iris                                        | 3              | 4              | 4                | 0                  | 150         |
| WBDC (Breast Cancer Wisconsin Diagnostic)   | 2              | 30             | 30               | 0                  | 569         |
| Spambase                                    | 2              | 57             | 57               | 0                  | 4601        |
| Heart                                       | 14             | 4              | 3                | 1                  | 559         |
| Glass                                       | 2              | 9              | 9                | 0                  | 214         |
| WBC (Breast Cancer Wisconsin Original)      | 2              | 9              | 9                | 0                  | 699         |
| Ionosphere                                  | 2              | 34             | 34               | 0                  | 351         |
| Arrhythmia                                  | 13             | 279            | 206              | 73                 | 452         |
| Multiple Features                           | 10             | 216            | 216              | 0                  | 2000        |
| Australian                                  | 2              | 14             | 6                | 8                  | 690         |
| German Number (Credit Dataset)              | 2              | 20             | 7                | 13                 | 1000        |
| DNA                                         | 3              | 180            | 0                | 180                | 3186        |
| Wine                                        | 3              | 13             | 13               | 0                  | 178         |
| Vehicle                                     | 2              | 18             | 18               | 0                  | 846         |
| Waveform                                    | 2              | 40             | 40               | 0                  | 5000        |
| Zoo                                         | 2              | 16             | 1                | 15                 | 101         |
| Hillvalley                                  | 2              | 100            | 100              | 0                  | 1212        |
| Sonar                                       | 2              | 60             | 60               | 0                  | 208         |
| Musk 1                                      | 2              | 167            | 166              | 1                  | 6598        |

---

## 📈 Model Evaluation Summary

To evaluate model performance, this script utilizes a `KNeighborsClassifier` and performs hyperparameter tuning and cross-validation across the datasets. The evaluation results are organized by dataset, providing `AUC` (Area Under the Curve) scores and their standard deviations, giving a clear view of the model’s effectiveness.

| **Dataset**                                | **KNeighborsClassifier_AUC** | **KNeighborsClassifier_AUC_STD** |
|--------------------------------------------|-------------------------------|-----------------------------------|
| Arrhythmia                                 | 0.57744                       | 0.0148868                        |
| Australian                                 | 0.856522                      | 0.0351729                        |
| DNA                                        | 0.836489                      | 0.0176211                        |
| German Number (Credit Dataset)             | 0.721                         | 0.0314484                        |
| Glass                                      | 0.668398                      | 0.0673421                        |
| Heart                                      | 0.819188                      | 0.0455073                        |
| Hillvalley                                 | 0.499187                      | 0.00633222                       |
| Ionosphere                                 | 0.695556                      | 0.126996                         |
| Iris                                       | 0.853333                      | 0.0718022                        |
| Multiple Features                          | 0.8055                        | 0.0301206                        |
| Musk 1                                     | 0.831495                      | 0.165486                         |
| Sonar                                      | 0.52381                       | 0.0897212                        |
| Spambase                                   | 0.798963                      | 0.0246224                        |
| Vehicle                                    | 0.917297                      | 0.0258821                        |
| WBC (Breast Cancer Wisconsin Original)     | 0.95                          | 0.0368394                        |
| WBDC (Breast Cancer Wisconsin Diagnostic)  | 0.685432                      | 0.0409327                        |
| Waveform                                   | 0.6298                        | 0.0206194                        |
| Wine                                       | 0.619608                      | 0.0994152                        |
| Zoo                                        | 1.0                           | 0                                |

---

## 🔍 Project Highlights

- **Automated Data Loading**: Seamlessly loads datasets from `sklearn` and `OpenML`.
- **Summary Generation**: Provides clear summaries of dataset characteristics.
- **Model Evaluation**: Performs automated hyperparameter tuning and cross-validation.
- **Result Presentation**: Outputs are saved in table format for easy comparison and analysis.

--- 

This README file serves as a comprehensive guide to understanding the dataset structures and the performance of models tested on each dataset. Thank you for exploring this project!
