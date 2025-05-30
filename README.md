### Heart Disease Prediction Project

**Author: Liyin Shi**

#### Abstract
This peoject develops a supervised machine learning model to predict heart disease using UCI Heart Disease Dataset. Three models - Random Forest, Logistic Regression and XGBoost - are implemented, with hyperparameter tuning and evaluation. The Random Forest model stood out, achieving the highest F1 score of 0.90.

#### Rationale
Heart disease is a concerning global health challenge which is extremely hard to predict and a main cause of morality globally. Predictive models can help clinicians in early diagnosis, enabling timely and effective interventions. This project demonstrates the potential of machine learning to address this critical real-world problem.

#### Research Question
How effectively can machine learning models predict heart disease based on clinical features and which model performs the best based on the F1 score metric?

#### Data Sources
The project uses the UCI Heart Disease Dataset, which includes 13 clinical features for 303 patients, such as age, sex, cholesterol levels, maximum heart rate (thalach), and quailified chest pain type (1 ~ 4). The target variable indicates the absence (0) or presence (1 ~ 4) of heart disease. The dataset contains missing data in multiple features so it will be preprocessed to handle outliers and missing values in Heart_Disease_EDA.ipynb, resulting in a cleaned dataset (heart_disease_processed.csv).

#### Methodology
The project follows a structured workflow:
##### 1. Exploratory Data Analysis (EDA):
Conducted data cleaning to address outliers (e.g., replacing missing values with median values).
Standardized numerical features using StandardScaler and encoded categorical variables.
Visualized feature distributions and correlations using histograms, box plots, and a correlation heatmap to identify key predictors.

##### 2. Model Development:
Three machine learning models - Random Forest, Logistic Regression, and XGBoost - are trained. GridSearch CV is used for hyperparameter tuning to optimize the F1 score.

##### 3. Model Evaluation:
Models are evaluated using accuracy, precision, recall and F1 score. A confusion matrix and feature importance plot fot the best model (Random Forest) are generated.

##### 4. Visualization
A bar plot of feature importance highlights key predictors for Random Forest.


#### Results
The Random Forest model outperformed others, achieving:
    Accuracy: 0.9016
    Precision: 0.8438
    Recall: 0.9643
    F1 Score: 0.9000
Logistic Regression and XGBoost yielded F1 scores of 0.8621 and 0.8421 respectively.

Key findings:
Maximum heart rate (thalach and thal) and chest pain type (cp) were the most influential features for predicting heart disease.
The high recall indicates the model is effective at identifying patients with heart disease, which is critical for medical applications.

#### Next Steps
Expand Dataset: Incorporate more diverse potential heart disease patient data to improve generalizability across populations.
Experiment with additional algorithms, such as Support Vector Machines or Neural Networks, to improve performance.
Feature Engineering: Explore interaction terms or new features to capture additional patterns in the data.

#### Conclusion
The project successfully developed a random forest model to predict heart disease, particularly with high recall, demonstrating its potential as a diagnostic tool. However, the precision indicates room for reducing false positives. The project successfully meets the course objectives of applying data mining techniques, but clinical deployment requires further validation to ensure reliability. Future work should focus on testing alternative algorithms and expanding the dataset.

#### Bibliography
UCI Machine Learning Repository. “Heart Disease Dataset.” https://archive.ics.uci.edu/dataset/45/heart+disease

