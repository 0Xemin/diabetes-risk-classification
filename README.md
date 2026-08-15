# Diabetes Risk Classification

> **Note**: This project was developed as the End-of-Year Final Project for the Data Mining course, as well as a submission for the Huawei Machine Learning Bootcamp.

This project focuses on the classification and prediction of diabetes risk using various advanced Machine Learning algorithms, with a strong emphasis on Tree-based models and Gradient Boosting techniques. A key challenge addressed in this project is handling imbalanced datasets using synthetic data generation methods like SMOTE, followed by rigorous hyperparameter tuning to achieve optimal predictive performance.

## 📁 Project Structure

- `diabet-prediction-gradientboost.ipynb`: The main Jupyter Notebook encompassing the entire end-to-end Data Science pipeline, including Exploratory Data Analysis (EDA), data preprocessing, model training, hyperparameter optimization, and comprehensive model evaluation.
- `requirements.txt`: The list of Python dependencies required to run the project seamlessly.

## 🛠️ Technologies and Algorithms Used

* **Data Manipulation & Visualization:** `pandas`, `numpy`, `matplotlib`, `seaborn`
* **Machine Learning Classifiers:** 
  * Random Forest Classifier
  * AdaBoost Classifier
  * Gradient Boosting Classifier (Scikit-Learn)
  * XGBoost Classifier
  * LightGBM Classifier
* **Data Preprocessing:** `OneHotEncoder`, `ColumnTransformer`
* **Imbalanced Data Handling:** `SMOTE` (`imbalanced-learn`) for mitigating class imbalance.
* **Model Optimization & Validation:** `RandomizedSearchCV` for hyperparameter tuning, and `StratifiedKFold` for robust cross-validation.

## 🚀 Setup and Installation

To run this project locally, ensure you have Python installed on your machine.

1. Navigate to the project directory in your terminal or command prompt.
2. Install the necessary dependencies by running:

```bash
pip install -r requirements.txt
```

3. Once the packages are installed, launch Jupyter Notebook to open and execute the project files:

```bash
jupyter notebook
```

## 📈 Workflow and Methodology

1. **Data Operations & Cleaning:** Loading the dataset, dealing with missing or erroneous values, and encoding categorical variables appropriately.
2. **Exploratory Data Analysis (EDA):** Visualizing distributions, feature relationships, and correlations to gain deep insights into the underlying patterns of the dataset.
3. **Data Balancing:** Applying the SMOTE (Synthetic Minority Over-sampling Technique) to synthetically balance the minority class in the training data, thereby preventing model bias towards the majority class.
4. **Model Training:** Training multiple powerful ensemble models on the balanced dataset.
5. **Hyperparameter Tuning & Evaluation:** Optimizing model hyperparameters using `RandomizedSearchCV`. The models are ultimately evaluated using critical classification metrics such as Accuracy, Confusion Matrix, and Classification Report (Precision, Recall, F1-Score).
