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

## Installation
To run the script, you need to install the required libraries. You can install them using the following command:

```bash
pip install tabulate scikit-learn pandas numpy openml
