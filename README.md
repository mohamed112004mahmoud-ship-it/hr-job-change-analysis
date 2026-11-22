# HR Analytics: Job Change Analysis

Explore how candidate characteristics relate to job-change intent in an HR analytics dataset.

## Dataset

- **Source:** [Kaggle: HR Analytics Job Change of Data Scientists](https://www.kaggle.com/datasets/arashnic/hr-analytics-job-change-of-data-scientists)
- **Files:** `aug_train.csv` (original) and `HR_clean.csv` (cleaned)
- **Size:** 19,158 rows and 14 columns
- **Target:** `target` — 1 means looking for a job change; 0 means not looking
- **Cleaning result:** all rows retained; no missing values or duplicate rows in `HR_clean.csv`

## Questions answered

1. What percentage of candidates are looking for a job change?
2. How does relevant experience relate to job-change intent?
3. How does university enrollment relate to job-change intent?
4. How do city development index and training hours correlate with the target?
5. How does job-change intent vary by years of experience?

## Tools used

Python, Pandas, NumPy, Seaborn, Matplotlib, and Jupyter Notebook.

## Key findings

1. **Overall target:** 24.9% (4,777 candidates) have `target = 1`; 75.1% (14,381) have `target = 0`.
2. **Relevant experience:** job-change intent is 21.5% among candidates with relevant experience and 33.8% among those without it.
3. **Correlation:** city development index has a negative correlation with the target (**r = -0.34**), while training hours have almost no correlation (**r = -0.02**).

The experience analysis also shows a general decline in job-change intent as experience increases, with some fluctuations. In the cleaning step, `<1` was encoded as 0 and `>20` as 21; these are representative codes for ranges, not exact years. Missing experience values were filled with the median.

These findings describe associations in this dataset; they do not establish cause and effect. Missing values in categorical fields such as `gender`, `enrolled_university`, `education_level`, `major_discipline`, `company_size`, and `company_type` were labeled `Unknown`. `experience` and `last_new_job` were numerically coded and their missing values were filled with their medians. The cleaned file contains no missing values.

## Charts

![Target distribution](images/target.png)

![Job-change rate by relevant experience](images/Relevant%20experience.png)

![Job-change rate by university enrollment](images/enrolled_university.png)

![Correlation heatmap](images/Correlation%20Between%20HR%20Variables.png)

![Job-change rate by experience](images/Job-Change%20Rate%20by%20Years%20of%20Experience.png)

## How to run

1. Keep `aug_train.csv` in the same folder as `hr_project_starter.ipynb`.
2. Install the notebook dependencies: `pandas`, `numpy`, `seaborn`, and `matplotlib`.
3. Open `hr_project_starter.ipynb` in Jupyter Notebook and run the cells from top to bottom.
4. The notebook writes `HR_clean.csv` and saves chart images in the `images/` folder.

## Files reviewed

- `aug_train.csv`
- `HR_clean.csv`
- `hr_project_starter.ipynb`
- Five chart images from the notebook's `images/` folder

## Still needed

- Add the dataset source link in the Dataset section.


