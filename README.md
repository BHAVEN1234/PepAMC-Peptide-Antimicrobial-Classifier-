
# 🚀 Peptide-Antimicrobial-Classifier  

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)  
![MIT License](https://img.shields.io/badge/License-MIT-green.svg)  
![Status](https://img.shields.io/badge/Status-Active-brightgreen)  

**An innovative tool leveraging machine learning to classify peptides for antimicrobial activity, offering enhanced insights for scientific research.**  

---

## 📋 Table of Contents  
- [🧐 About The Project](#-about-the-project)  
- [🛠️ Built With](#-built-with)  
- [🌟 Features](#-features)  
- [🚀 Getting Started](#-getting-started)  
  - [🔧 Prerequisites](#prerequisites)  
  - [📦 Install Dependencies](#install-dependencies)  
- [🛠️ Usage](#usage)
- [📑 Comprehensive Documentation](#comprehensive-documentation)
- [📊 Results](#results)  
- [📜 License](#license)  
- [🤝 Contributing](#contributing)  
- [📧 Contact](#contact)  
- [📌 Acknowledgments](#acknowledgments)

---

## 🧐 About The Project  

Many websites and systems rely on secure applications to prevent **cyber-attacks** through open ports and vulnerable services. This project applies **machine learning models** to predict and classify peptide-based antimicrobial activity, empowering researchers to identify peptides that may prevent infections from resistant pathogens.

By utilizing datasets such as **Wine** and **Iris**, this project demonstrates the effectiveness of ML classifiers in feature selection and optimization for real-world applications.

---

## 🛠️ Built With  
- ![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white) **Python**  
- ![scikit-learn](https://img.shields.io/badge/scikit--learn-0.24.2-green?logo=scikit-learn&logoColor=white) **scikit-learn**  
- ![NumPy](https://img.shields.io/badge/NumPy-1.21.0-red?logo=numpy&logoColor=white) **NumPy**  
- ![Matplotlib](https://img.shields.io/badge/Matplotlib-3.4.2-orange?logo=matplotlib&logoColor=white) **Matplotlib**  
- ![Seaborn](https://img.shields.io/badge/Seaborn-0.11.1-yellow?logo=seaborn&logoColor=white) **Seaborn**  
- ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white) **Jupyter Notebook**

---

## 🌟 Features  
✅ Multiple models including **Logistic Regression** and **SVM**  
✅ **Cross-validation** using Stratified KFold  
✅ **Metrics:** Accuracy and Matthews Correlation Coefficient (MCC)  
✅ Preprocessing with **MinMaxScaler** and **StandardScaler**  
✅ **Visualization tools** using Matplotlib and Seaborn  

---

## 🚀 Getting Started  

### 🔧 Prerequisites  
To run this project, you need the following tools and libraries installed:  

1. **Python 3.x**  
   Make sure Python is installed. You can download it [here](https://www.python.org/downloads/).  

2. **Jupyter Notebook**  
   Recommended for running and experimenting with code. Install it via:  
   ```bash
   pip install notebook
   ```

3. **Required Python Libraries**  
   Install all necessary libraries by running:  
   ```bash
   pip install scikit-learn numpy matplotlib seaborn
   ```

4. **Dataset (Wine/Iris)**  
   Ensure access to the **Wine** or **Iris** datasets, which are available through scikit-learn:  
   ```python
   from sklearn.datasets import load_wine, load_iris
   ```

---
### 📦 Install Dependencies  
To install the necessary dependencies for this project, create a `requirements.txt` file using the following command in your terminal:

```bash
pip freeze > requirements.txt
```
```bash
pip install -r requirements.txt
```
## 🛠️ Usage  
Load the dataset (e.g., Wine or Iris).  
Preprocess the data using scaling tools like `MinMaxScaler` or `StandardScaler`.  
Train and evaluate the models (Logistic Regression or SVM).  
Visualize results using plots to assess model performance.

---
## 📑 Documentation  

For detailed documentation, refer to the [Comprehensive Documentation](docs/Comprehensive_Documentation.pdf).
Baseline Model Updated Document [Baseline Model Updated](docs/Baseline_model_updated.pdf).

## 📊 Results  

Visualizing the results is essential for assessing model performance and understanding key metrics. Below are some significant plots generated using Seaborn and Matplotlib:

### Best Fitness vs. Generation Graph  
This graph illustrates the relationship between the best fitness values achieved and the number of generations during the model training process. A well-defined trend can indicate the convergence of the model.

![Best Fitness vs. Generation](images/best_fitness_vs_generation.jpeg)
![Best Fitness vs. Generation](images/best_fitness_vs_generation1.jpeg)
![Best Fitness vs. Generation](images/best_fitness_vs_generation2.jpeg)


---

## 📜 License  

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

## 🤝 Contributing  

Contributions are welcome! Follow these steps to contribute:

1. Fork the repository  
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)  
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)  
4. Push to the branch (`git push origin feature/AmazingFeature`)  
5. Open a pull request  

---

## 📧 Contact  

- **Jesus Armando Beltran Verdugo**: [abeltr99@calstatela.edu](mailto:abeltr99@calstatela.edu)  
- **Bhaven Chheda**: [bchheda@calstatela.edu](mailto:bchheda@calstatela.edu)  
- **Tirth Shah**: [tshah6@calstatela.edu](mailto:tshah6@calstatela.edu)  

---

## 📌 Acknowledgments  

Special thanks to the Python, scikit-learn, and Matplotlib communities for their amazing tools that power this project.
