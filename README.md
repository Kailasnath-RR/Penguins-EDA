# 🐧 Penguins Dataset – Exploratory Data Analysis (EDA)
This project performs a complete Exploratory Data Analysis (EDA) on the Palmer Penguins dataset.
The goal is to understand how physical characteristics of penguins vary across species, sex, and islands, and to extract meaningful insights using visualizations and statistics.
## 📂 Dataset Description
The dataset contains measurements for three penguin species:
- Adelie
- Chinstrap
- Gentoo

Across three islands:
- Biscoe
- Dream
- Torgersen
## Features analyzed
- species
- island
- bill_length_mm
- bill_depth_mm
- flipper_length_mm
- body_mass_g
- sex
## 🧹 Data Cleaning
- During preprocessing:
    - Missing numerical values (bill_length_mm, bill_depth_mm, flipper_length_mm, body_mass_g) were filled using mean imputation.
    - Missing sex values were filled using the mode.

    
    All missing values were successfully handled before analysis.
## 📊 Key Analyses Performed
#### ✔ Species-wise comparisons
- Mean bill length
- Mean bill depth
- Body mass analysis
- Flipper length trends
#### ✔ Sex-based comparisons
- Male vs female body mass
- Male vs female bill dimensions
#### ✔ Island-based comparisons
- Variation of bill length between islands
- Distribution differences via boxplots
#### ✔ Grouped statistics
- Used groupby() and agg() to compute:
    - mean
    - min
    - max
    - count
    - standard deviation
## 🧠 Final Insights
- Gentoo penguins are the heaviest among all species.
- Chinstrap penguins have the longest bills, followed by Gentoo and then Adelie.
- Males are heavier and have longer bills than females across all species.
- Biscoe Island penguins have the longest bills, followed by Dream and Torgersen.
    
    The dataset shows clear species and sex-based physical differences, useful for biological or ecological studies.

## 🤖 Machine Learning Summary
- Problem: Predict bill_length_mm

- Preprocessing steps
    -  Applying SimpleImputer on numerical and categorical data
    - Applying OneHotEncoder on Categorical data
- Models used
    - Decision Tree Regressor
    - Random Forest Regressor
- Best performance
    - Decision Tree Regressor
- Interpretation of MAE:-

    The model predicts bill length with high accuracy, typically within 2 mm of the true value.
## ⚙️ Pipeline Implementation (Scikit-Learn)
To improve code cleanliness, prevent data leakage, and automate preprocessing, I implemented a full end-to-end Scikit-Learn 
Pipeline for the Penguins dataset.

#### Implemented :-
 - Pipeline
 - ColumnTransformer
## 📈 Pipeline Results
- 🔹 Decision Tree Regressor
        
        Best max_leaf_nodes = 5 -> MAE ≈ 1.61 mm
- 🔹 Random Forest Regressor

        Default model MAE ≈ 1.66 mm

### 🧠 Interpretation
- Simpler models (shallow Decision Trees) performed better than Random Forest on this small dataset.

- Pipelines helped maintain cleaner code and consistent preprocessing during model comparison.

- MAE around 1.6–2.0 mm means the model predicts bill length within ~4–5% error, which is strong performance.


## 🛠 Technologies Used
- Python
- Pandas
- NumPy
- Seaborn
- Jupyter Notebook
- Sklearn
## 🚀 Future Work
- Model comparison
- Feature importance
## Thank You for Reading