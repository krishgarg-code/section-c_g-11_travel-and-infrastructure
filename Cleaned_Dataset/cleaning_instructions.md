# 📊 Dataset Preprocessing & Cleaning

The original dataset required multiple preprocessing steps before it could be used for analysis and model training. The following steps were performed:

### 1. Dataset Size Reduction (Sampling for Stability)

- The initial dataset contained more than **300,000 rows**.
- To improve computational stability and reduce training time, the dataset was **randomly sampled down to 10,000 rows** using Python-based randomization.
- This helped maintain a representative subset of the data while enabling faster experimentation.

### 2. Handling Missing Values

- Rows with missing/blank values were removed from the following important columns:
  - Junction Control
  - Road Surface Condition
  - Road Type
  - Weather Condition

### 3. Removing Irrelevant Column

- The **Carriageway Type** column was removed because it contained a large number of missing values and was not essential for the analysis.

### 4. Correcting Data Inconsistencies

- A typo in the **Accident Severity** column was corrected:
  - `fetal` → `fatal`
- This ensured consistency in class labels used for model training.
