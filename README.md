## Patient Readmission Prediction

This project builds and evaluates machine-learning models to predict hospital readmissions among diabetic patients using the UCI “diabetic\_data.csv” dataset.

Overview

1. Data Loading & Exploration

   * Inspect dataset size, feature types and target distribution
   * Convert readmission times into a binary “readmitted/not readmitted” label

2. Preprocessing & Feature Engineering

   * Identify and handle missing or anomalous values
   * Impute or drop features based on clinical relevance
   * Encode categorical variables (one-hot, ordinal, target encoding)
   * Scale numeric features with RobustScaler or StandardScaler
   * Balance classes via oversampling (e.g. SMOTE)

3. Model Training & Hyperparameter Tuning

   * Compare Support Vector Machine, Random Forest, XGBoost, and LightGBM classifiers
   * Use cross-validated grid search or randomized search for best parameters
   * Evaluate models by accuracy, precision, recall, F1-score, and ROC AUC

4. Feature Importance & Selection

   * Extract feature importances and SHAP values
   * Visualize top predictors and prune low-impact features
   * Retrain best models on reduced feature sets

5. Final Evaluation

   * Test the final model on a held-out validation set
   * Report classification metrics and confusion matrix
   * Discuss clinical implications and limitations

Repository Structure
• diabetic\_data.csv
Raw patient data file
• Patient\_Readmission\_Prediction.ipynb
Jupyter notebook with the full workflow
• requirements.txt
List of Python libraries and versions

Setup

1. Clone the repository and change into its directory
2. (Optional) Create a virtual environment and activate it
3. Install dependencies with
   pip install -r requirements.txt

Usage

1. Ensure diabetic\_data.csv is in the project root
2. Launch Jupyter Notebook and open Patient\_Readmission\_Prediction.ipynb
3. Run each cell in order to reproduce data cleaning, modeling, and analysis

Results
• Random Forest achieves approximately 68 % accuracy and 0.58 F1-score on the test set
• XGBoost and SVM models were evaluated for comparison
• Key features include number of prior admissions, lab test counts, and patient age

Next Steps
• Additional feature engineering (interaction terms, temporal trends)
• Ensemble or stacking of top models
• Deployment as a simple API or dashboard


