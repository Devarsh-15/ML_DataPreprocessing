# ML_DataPreprocessing

My Data Preprocessing for ML practice &amp; notebooks

**Titanic Data Preprocessing – Day 1**

Day 1 covers the first stage of data preprocessing on the Titanic dataset:
environment setup, basic EDA, and missing-value handling.

📊 Key Steps

Loaded dataset and ran quick EDA (info(), describe(), value_counts()).

Detected and visualized missing data with isnull() and missingno (matrix, bar, heatmap).

Created missing indicators (flags for original NaNs).

Imputed numeric/categorical columns using:

SimpleImputer (mean/median/mode)

IterativeImputer

KNNImputer

Organized everything in a scikit-learn Pipeline + ColumnTransformer for reproducibility.
