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

# Titanic Data Preprocessing – Day 2

This notebook continues the **Data Preprocessing Roadmap** using the Titanic dataset.  
Day-2 focused on **Outlier Detection, Treatment, and Feature Scaling**.

---

### ✅ Topics Covered

- **Outlier Detection**

  - Visual methods: Boxplots, Scatterplots, Histograms
  - Statistical methods: Z-Score, IQR Rule
  - Reusable Outlier Detection Function (IQR + Z-Score)
  - Advanced: Isolation Forest, DBSCAN (introductory)

- **Outlier Treatment**

  - Removal of extreme outliers
  - Winsorization / Capping
  - Log & Power Transformations (distribution smoothing)
  - Before vs. After visualization

- **Feature Scaling & Normalization**

  - StandardScaler (Z-score scaling)
  - MinMaxScaler (0–1 normalization)
  - RobustScaler (resistant to outliers)
  - PowerTransformer (for skewed distributions)
  - Comparison of scaling methods using histograms & summary stats

- **Pipeline Integration**
  - Combining outlier handling + scaling into a single Scikit-Learn pipeline
  - Reproducible preprocessing workflow

---

### 📌 Key Learnings

- Outliers **distort the scale** and can mislead models, especially distance-based ones (e.g., KNN, SVM, clustering).
- Both **visual & statistical checks** are important — neither alone is enough.
- Different scaling methods suit different data distributions:
  - Use **StandardScaler** for normally distributed data.
  - Use **MinMaxScaler** when features must be bounded (e.g., neural nets).
  - Use **RobustScaler** when many outliers exist.
  - Use **PowerTransformer** to reduce skewness.
- Pipelines ensure **clean, consistent, and repeatable preprocessing**.

---

### 📂 Files Added

- `Notebooks/Day2_Outliers_Scaling.ipynb`
- Updated `README.md` with Day-2 learnings
- Saved dataset version: `Data/titanic_day2.csv`

---
