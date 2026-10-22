Machine Learning Prediction of the Bulk Modulus of Crystalline Materials
Project Overview

This preliminary study investigates the use of machine learning to predict the bulk modulus of crystalline materials from composition- and structure-related features. The project uses the Matbench log_kvrh dataset and compares Linear Regression with a Random Forest regression model.

The work explores data preparation, exploratory data analysis, model training, performance evaluation, and feature importance.

Dataset
Dataset: Matbench log_kvrh
Number of records: 10,987
Input features: 135
Target: log10(K_VRH), the base-10 logarithm of the Voigt-Reuss-Hill bulk modulus in GPa.

The target is computationally derived rather than a direct experimental measurement.

Models and Results
Metric	Linear Regression	Random Forest
MAE	0.0985	0.0708
RMSE	0.1542	0.1239
R²	0.8343	0.8930

MAE and RMSE are reported on the logarithmic target scale.

In this train/test split, Random Forest achieved lower prediction errors and a higher R² score than Linear Regression.

Key Finding

The Random Forest model performed better than Linear Regression on the held-out test set. The feature-importance analysis identified volume per atom (vpa) as the most influential predictive feature in the fitted Random Forest model.

Feature importance indicates predictive contribution, not causation.

Limitations

This is a preliminary study using a random train/test split. The results do not establish generalization to entirely new material families. Bulk modulus alone is also insufficient to determine a material's suitability for demanding engineering environments.

Project Files
Executed Jupyter notebook: data preparation, analysis, modeling, and plots.
Final report: written discussion of the methodology, results, and limitations.
Data Source

The dataset is available through the Matbench project:
https://github.com/materialsproject/matbench