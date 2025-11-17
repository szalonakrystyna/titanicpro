# titanicpro
**Titanic Data Analysis**
Predictive Analytics & Exploratory Data Analysis (EDA)

**Overview**
This project presents an exploratory data analysis (EDA) and predictive modelling workflow using the Titanic dataset.
The goal is to understand which factors influenced passenger survival and to visualise the key relationships inside the data.

The notebook includes:
- Data cleaning & preprocessing
- Handling missing values
- Exploratory visualisations (distribution, correlations, heatmaps)
- Feature engineering
- Simple machine learning model for survival prediction

**Tools & Libraries**
The analysis was performed using Python 3.9+.
Main packages:
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- jupyter / colab

**Exploratory Data Analysis (EDA)**
Missing values:
- Missing values identified in Age, Cabin, and Embarked.
- Age imputed using median by passenger class.

Key visualisations:
- Distribution plots (Age, Fare, Sex).
- Survival rate by:
sex
class
age groups
family size
- Heatmap of feature correlations.
- Pairplot of selected variables.

**FE Feature Engineering**
Created additional features:
- FamilySize = SibSp + Parch + 1
- IsAlone
- Age bins (child/teen/adult/senior)
- Encoded categorical variables (Sex, Embarked, Class)

**MLM Machine Learning Model**
A baseline ML model was trained:
Model: Logistic Regression / Random Forest (configurable)
Metrics used:
- Accuracy
- F1-score
- Confusion Matrix
- ROC-AUC
- The baseline model achieves ~77–82% accuracy depending on random seed and preprocessing.

**Results Summary**

Women had significantly higher survival probability (~74% vs ~19%).
Passengers in 1st class survived much more often.
Children under 12 also had elevated survival rates.
Fare and class strongly correlated with survival.
Cabin information is incomplete but carries strong predictive value when available.

**Diagrams**
### Distribution of Passenger Ages
![Age Histogram](Distri_of_Passenger_Age.png)
### Fare vs Age Scatterplot
![Fare vs Age](images/Age_vs_fare_with_surv.png)
### Survival by Passenger Class
![Pclass Survival Chart](images/Survival_rate_by_class.png)
### Survival by Title
![Title Survival Chart](images/Survival_rate_by_title.png)
### Correlation heatmap
![Correlation Heatmap](images/Corr_heatmap.png)
### Feature Importance
![Feature Importance – RandomForest](images/Feature_Importance.png)

**How to Run**
Clone repo:
git clone https://github.com/<twoj_login>/titanic-data-analysis.git
cd titanic-data-analysis

Install dependencies:
pip install -r requirements.txt

Run notebook:
jupyter notebook notebooks/titanic_analysis.ipynb

**Future Work**
- Hyperparameter tuning using GridSearchCV
- Gradient boosting models (XGBoost, LightGBM)
- Model explainability (SHAP values)
- Deployment with Streamlit

**Author**
Anna Stefańska
Data Science & AI beginner focused on medical and imaging applications.



