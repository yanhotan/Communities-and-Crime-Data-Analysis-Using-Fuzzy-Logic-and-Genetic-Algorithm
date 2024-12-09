# Communities and Crime Data Analysis Using Fuzzy Logic and Genetic Algorithm

This project implements a comprehensive pipeline to analyze the **Communities and Crime** dataset using Fuzzy Logic, KMeans clustering, and a Genetic Algorithm for feature selection. The goal is to predict violent crimes per population while optimizing feature selection and model performance.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [Dependencies](#dependencies)
4. [Workflow](#workflow)
    - Data Exploration
    - Data Cleaning and Preprocessing
    - Feature Selection
    - Model Building
    - Model Tuning
    - Model Testing
5. [Results](#results)
6. [Usage](#usage)
7. [License](#license)

---

## Introduction
This repository focuses on building an interpretable predictive model using Fuzzy Logic and advanced feature selection methods. It uses the **Communities and Crime dataset** from the UCI repository to predict crime prevalence, ensuring robustness and interpretability through:
- Fuzzy Membership functions.
- KMeans clustering for value groupings.
- Genetic Algorithm-based feature selection.

---

## Project Overview
### Key Components:
1. **Data Cleaning:**
   - Handle missing values by either dropping columns with excessive missing data or imputing the median.

2. **Feature Selection:**
   - Low correlation features are removed to simplify the model.
   - Genetic Algorithm identifies the optimal subset of features to maximize model performance.

3. **Fuzzy Logic Model:**
   - Membership functions are generated for key features and target variables.
   - Rules are created based on membership grades for prediction.

4. **Model Tuning:**
   - Genetic Algorithm parameters like population size, number of top features, and mutation/crossover probabilities are optimized.

5. **Evaluation:**
   - Performance metrics include Mean Squared Error (MSE) and Mean Absolute Error (MAE).

---

## Dependencies
The project requires the following libraries:
- Python 3.8+
- Pandas
- NumPy
- Scikit-learn
- Scikit-fuzzy
- XGBoost
- Matplotlib
- Seaborn
- ucimlrepo

Install the dependencies using:
```bash
pip install -r requirements.txt
```

---

## Workflow
### **1. Data Exploration**
- Explore the dataset to understand its structure and identify missing values.
- Check for the type and range of values in each feature.

### **2. Data Cleaning and Preprocessing**
- Drop columns with excessive missing values.
- Replace missing values in the remaining columns with their median.
- Remove non-numeric columns for consistent processing.

### **3. Feature Selection**
- **Low-Correlation Features Removal:** Features with low correlation to the target are dropped.
- **Genetic Algorithm:**
  - Population-based optimization selects the best feature subset.
  - Ensures the features chosen have high predictive power.

### **4. Model Building**
- Use Fuzzy Logic to define membership functions for selected features and the target variable.
- Generate rules from the training data based on membership grades.
- Predict crime prevalence using these rules.

### **5. Model Tuning**
- Various settings for the Genetic Algorithm and correlation thresholds are tested to minimize MSE.
- The best setting is applied to the test set for final evaluation.

### **6. Model Testing**
- Evaluate the model on the test set using the optimal settings.
- Metrics include:
  - Mean Squared Error (MSE)
  - Mean Absolute Error (MAE)

---

## Results
- The Genetic Algorithm identified the optimal feature subset, improving performance.
- Fuzzy Logic provided interpretable rules, making the model transparent for stakeholders.
- Final model performance:
  - **MSE:** [To be updated after run]
  - **MAE:** [To be updated after run]

---

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/crime-fuzzy-genetic.git
   cd crime-fuzzy-genetic
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook to:
   - Explore and clean the data.
   - Perform feature selection.
   - Build and evaluate the model.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

## Acknowledgments
- Dataset sourced from the UCI Machine Learning Repository.
- Inspired by Jeffrey A. Shaffer's work on Data Visualization and Fuzzy Logic techniques.

Feel free to contribute to the project or raise issues on GitHub!
