# Career Switch Prediction

A machine learning project that predicts whether an employee is likely to change their career using supervised and unsupervised machine learning techniques.

## 👥 Authors

**Zead Raihan & Tasfin Mahmud**

This project was collaboratively developed as part of the **CSE 422: Artificial Intelligence** course.

## 📌 Project Overview

The goal of this project is to predict whether an employee will change their career based on demographic information, education, employment history, and other relevant features.

The project approaches the problem using both:

* **Supervised Learning** — predicting the target variable `will_change_career`
* **Unsupervised Learning** — identifying natural groups of candidates using K-Means clustering

## 📊 Dataset

The dataset contains **5,000 records** and **14 columns**, including the target variable.

### Target Variable

`will_change_career`

* `0` — Will not change career
* `1` — Will change career

The dataset contains a mixture of numerical and categorical features, along with missing values that required preprocessing.

## 🔧 Data Preprocessing

The following preprocessing steps were applied:

* Removed identifier and high-cardinality columns such as `enrollee_id` and `city`
* Corrected a corrupted `company_size` category
* Handled missing values
* Encoded categorical variables
* Applied ordinal encoding where appropriate
* Applied one-hot encoding to categorical features
* Used `StandardScaler` for feature scaling
* Used a stratified **80/20 train-test split**

## 🤖 Machine Learning Models

The project evaluates five machine learning approaches:

### Supervised Learning

1. **K-Nearest Neighbours (KNN)**
2. **Decision Tree**
3. **Logistic Regression**
4. **Neural Network**

### Unsupervised Learning

5. **K-Means Clustering**

## 📈 Results

| Model               | Accuracy | Precision | Recall | F1-Score |    AUC |
| ------------------- | -------: | --------: | -----: | -------: | -----: |
| Decision Tree       |   79.40% |    59.13% | 59.13% |   59.13% | 0.7745 |
| Logistic Regression |   78.10% |    60.25% | 38.49% |   46.97% | 0.7551 |
| KNN                 |   77.50% |    57.71% | 40.08% |   47.31% | 0.7449 |
| Neural Network      |   77.00% |    55.29% | 45.63% |   50.00% | 0.7613 |

The dataset is imbalanced, with approximately **74.76%** of candidates belonging to the non-switching class and **25.24%** belonging to the switching class. Therefore, accuracy was considered together with precision, recall, F1-score, and AUC.

## 🔍 K-Means Clustering

K-Means was used as an unsupervised learning approach to investigate whether candidates naturally form different groups.

The clustering analysis produced three clusters and examined their career-switching rates. The results showed differences in switching behaviour across the clusters, providing an additional perspective on the dataset.

## 🛠️ Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* TensorFlow / Keras

## 📂 Project Files

```text
Career-Switch-Prediction/
│
├── CSE422_Career_Switch_Prediction.ipynb
├── Career_Switch_Prediction_Dataset.csv
└── README.md
```

## ▶️ How to Run

1. Clone this repository:

```bash
git clone https://github.com/YOUR-USERNAME/career-switch-prediction.git
```

2. Open the project folder.

3. Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow jupyter
```

4. Open the notebook:

```bash
jupyter notebook
```

5. Run the cells in:

`CSE422_Career_Switch_Prediction.ipynb`

## 🎓 Course

**CSE 422 — Artificial Intelligence**

This project was developed as a course project to apply supervised and unsupervised machine learning techniques to a real-world prediction problem.
