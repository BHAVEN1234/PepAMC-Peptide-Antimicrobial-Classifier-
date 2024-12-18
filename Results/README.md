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
| DNA                                         | 3              | 180            | 0                | 180                | 3186        |
| Wine                                        | 3              | 13             | 13               | 0                  | 178         |
| Vehicle                                     | 2              | 18             | 18               | 0                  | 846         |
| Waveform                                    | 2              | 40             | 40               | 0                  | 5000        |
| Hillvalley                                  | 2              | 100            | 100              | 0                  | 1212        |
| Sonar                                       | 2              | 60             | 60               | 0                  | 208         |

---

## 📈 Model Evaluation Summary

To evaluate model performance, this script utilizes a `KNeighborsClassifier` and performs hyperparameter tuning and cross-validation across the datasets. The evaluation results are organized by dataset, providing `AUC` (Area Under the Curve) scores and their standard deviations, giving a clear view of the model’s effectiveness.  

| **Dataset**                               | **Framework**             | **AUC**                        | **AUC_STD**                   | **Best_Params**                                              | **Time_Taken**       |
|-------------------------------------------|---------------------------|---------------------------------|-------------------------------|-------------------------------------------------------------|-----------------------|
| Iris                                      | KNeighborsClassifier      | 0.8533333333333335             | 0.07180219742846006           | {'classifier__n_neighbors': 7, 'classifier__weights': 'distance'} | 2.8770437240600586   |
| WBDC (Breast Cancer Wisconsin Diagnostic) | KNeighborsClassifier      | 0.6854323308270677             | 0.04093269008836167           | {'classifier__n_neighbors': 7, 'classifier__weights': 'uniform'}  | 9.412885427474976    |
| Spambase                                  | KNeighborsClassifier      | 0.7989625577666699             | 0.024622408860984428          | {'classifier__n_neighbors': 5, 'classifier__weights': 'distance'} | 27.55205273628235    |
| Heart                                     | KNeighborsClassifier      | 0.8191883116883115             | 0.045507263028688995          | {'classifier__n_neighbors': 7, 'classifier__weights': 'uniform'}  | 1.1435601711273193   |
| Glass                                     | KNeighborsClassifier      | 0.6683982683982684             | 0.06734211156108369           | {'classifier__n_neighbors': 7, 'classifier__weights': 'uniform'}  | 1.129058837890625    |
| WBC (Breast Cancer Wisconsin Original)    | KNeighborsClassifier      | 0.95                           | 0.03683941988065038           | {'classifier__n_neighbors': 3, 'classifier__weights': 'uniform'}  | 1.5516104698181152   |
| Ionosphere                                | KNeighborsClassifier      | 0.6955555555555556             | 0.1269956343992288            | {'classifier__n_neighbors': 3, 'classifier__weights': 'uniform'}  | 2.868738889694214    |
| Arrhythmia                                | KNeighborsClassifier      | 0.5774396135265699             | 0.014886832236702835          | {'classifier__n_neighbors': 7, 'classifier__weights': 'uniform'}  | 27.50302004814148    |
| Multiple Features                         | KNeighborsClassifier      | 0.8055                         | 0.03012059096365805           | {'classifier__n_neighbors': 7, 'classifier__weights': 'distance'} | 21.490187883377075   |
| Australian                                | KNeighborsClassifier      | 0.8565217391304347             | 0.035172930723222             | {'classifier__n_neighbors': 7, 'classifier__weights': 'distance'} | 1.9750316143035889   |
| DNA                                       | KNeighborsClassifier      | 0.83648883105617               | 0.017621144879413367          | {'classifier__n_neighbors': 7, 'classifier__weights': 'distance'} | 23.80613112449646    |
| Wine                                      | KNeighborsClassifier      | 0.6196078431372549             | 0.09941518087232178           | {'classifier__n_neighbors': 7, 'classifier__weights': 'distance'} | 1.3791205883026123   |
| Vehicle                                   | KNeighborsClassifier      | 0.9172969187675069             | 0.025882129365932635          | {'classifier__n_neighbors': 5, 'classifier__weights': 'uniform'}  | 1.825406551361084    |
| Waveform                                  | KNeighborsClassifier      | 0.6298000000000001             | 0.020619408332927518          | {'classifier__n_neighbors': 7, 'classifier__weights': 'uniform'}  | 11.706374883651733   |
| Hillvalley                                | KNeighborsClassifier      | 0.49918710201869665            | 0.006332217868819316          | {'classifier__n_neighbors': 5, 'classifier__weights': 'uniform'}  | 9.176762819290161    |
| Sonar                                     | KNeighborsClassifier      | 0.5238095238095238             | 0.08972116038769891           | {'classifier__n_neighbors': 5, 'classifier__weights': 'uniform'}  | 4.245889663696289    |
---

## 🔍 Project Highlights

- **Automated Data Loading**: Seamlessly loads datasets from `sklearn` and `OpenML`.
- **Summary Generation**: Provides clear summaries of dataset characteristics.
- **Model Evaluation**: Performs automated hyperparameter tuning and cross-validation.
- **Result Presentation**: Outputs are saved in table format for easy comparison and analysis.

--- 

This README file serves as a comprehensive guide to understanding the dataset structures and the performance of models tested on each dataset. Thank you for exploring this project!
