# Dataset Summary Generator

## Overview
This Python script loads multiple datasets from popular machine learning repositories (such as `sklearn` and `OpenML`), summarizes their characteristics, and presents the results in a well-organized table format using the `tabulate` library. The generated summary includes details such as:

- Dataset name
- Number of classes (unique target labels)
- Number of features
- Number of numerical features
- Number of categorical features
- Size of the dataset (number of instances)

The final output is a formatted table displaying the above information for each dataset.

## Features
- **Automatic Dataset Loading**: The script fetches datasets from various sources such as `sklearn` and `OpenML`.
- **Dataset Summary**: For each dataset, it provides an overview including numerical and categorical feature counts, as well as the number of instances.
- **Table Format**: The summaries are displayed in an aesthetically pleasing table using the `tabulate` library.
  
## Libraries Used
- **pandas**: Data manipulation and analysis.
- **numpy**: Numerical computations and data operations.
- **scikit-learn**: Machine learning datasets.
- **tabulate**: Beautiful table formatting.

## Code Explanation

### Dataset Summarization
The `summarize_dataset()` function calculates:

- **Number of Classes**: The unique values in the target variable.
- **Number of Features**: Total number of features in the dataset.
- **Numerical Features**: Features that are numeric (e.g., integer, float).
- **Categorical Features**: Non-numeric features (e.g., string, object).
- **Dataset Size**: The number of instances or rows in the dataset.

### Loading Datasets
Datasets are loaded using either the `load_iris()` or `fetch_openml()` functions. Each dataset is passed through the `summarize_dataset()` function to extract the relevant information and store it in a list.

### Output
Once all datasets are summarized, the results are stored in a pandas DataFrame and displayed in a table format using the `tabulate` library.

## Example Output

The script will display a table like this:

| Dataset                              | Number of Classes | Number of Features | Numerical Features | Categorical Features | Size of the Dataset |
|--------------------------------------|-------------------|--------------------|--------------------|----------------------|---------------------|
| Iris                                 | 3                 | 4                  | 4                  | 0                    | 150                 |
| WBDC (Breast Cancer Wisconsin Diagnostic) | 2                 | 30                 | 30                 | 0                    | 569                 |
| Spambase                             | 2                 | 57                 | 57                 | 0                    | 4601                |
| Heart                                | 14                | 4                  | 3                  | 1                    | 559                 |
| Glass                                | 2                 | 9                  | 9                  | 0                    | 214                 |
| WBC (Breast Cancer Wisconsin Original) | 2                 | 9                  | 9                  | 0                    | 699                 |
| Ionosphere                           | 2                 | 34                 | 34                 | 0                    | 351                 |
| Arrhythmia                           | 13                | 279                | 206                | 73                   | 452                 |
| Multiple Features                    | 10                | 216                | 216                | 0                    | 2000                |
| Australian                           | 2                 | 14                 | 6                  | 8                    | 690                 |
| German Number (Credit Dataset)       | 2                 | 20                 | 7                  | 13                   | 1000                |
| DNA                                  | 3                 | 180                | 0                  | 180                  | 3186                |
| Wine                                 | 3                 | 13                 | 13                 | 0                    | 178                 |
| Vehicle                              | 2                 | 18                 | 18                 | 0                    | 846                 |
| Waveform                             | 2                 | 40                 | 40                 | 0                    | 5000                |
| Zoo                                  | 2                 | 16                 | 1                  | 15                   | 101                 |
| Hillvalley                           | 2                 | 100                | 100                | 0                    | 1212                |
| Sonar                                | 2                 | 60                 | 60                 | 0                    | 208                 |
| Musk 1                               | 2                 | 167                | 166                | 1                    | 6598                |

## Contribution
Feel free to fork this repository, contribute improvements, or add additional datasets to the list.

## License
This project is open-source and available under the MIT License.
