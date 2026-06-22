# Model Evaluation, Explainability, and Fairness Reflection — Nonprofit Donor Retention

## Assignment title
Week 6 — Model Evaluation, Explainability, and Fairness Reflection

## Dataset description
The dataset (`nonprofit_donor_retention_dataset.csv`) contains **370 donor records** from a nonprofit organisation, described by **17 columns**. Each record captures a single donor's profile and behaviour, combining:

- **Demographics:** age, age group, gender, region, donor type
- **Giving & engagement signals:** total donations last year, average donation amount, number of campaigns contacted, emails opened in the last 6 months, events attended last year, months since last donation, volunteer status, communication preference, estimated annual income
- **History & outcome:** whether the donor was retained the previous year, and the target outcome for this year

Two numeric columns (`annual_income_estimate`, `average_donation_amount`) contain a small number of missing values, which are filled with the column median during preprocessing. There are no duplicate donors.

## Target variable
**`donor_retained`** — a binary flag where `1` means the donor gave again (retained) and `0` means the donor lapsed. The classes are roughly balanced (about 48% retained / 52% lapsed).

## Model used
A **Decision Tree Classifier** (`scikit-learn`, `max_depth=4`, `random_state=42`), chosen for its interpretability. The sensitive group columns (`gender`, `region`, `age_group`) are excluded from the model inputs and reserved for the fairness audit only.

## Main evaluation results
| Metric | Value |
|--------|-------|
| Accuracy (test) | ~0.66 |
| Precision | ~0.63 |
| Recall | ~0.71 |
| F1-score | ~0.67 |
| Cross-validated accuracy (5-fold mean) | ~0.71 (std ~0.045) |

- **Confusion matrix:** TN = 24, FP = 15, FN = 10, TP = 25
- **Most important features:** months since last donation, total donations last year
- **Overfitting:** training accuracy ~0.85 vs testing ~0.66 at depth 4 (a shallower depth-2 tree generalises better)

## Main business interpretation
The model predicts donor retention with moderate, stable accuracy. The most important metric for this use case is **recall**, because the costly mistake is failing to spot a donor who is drifting away. The dominant error type is the **false positive** (predicting a donor will stay when they actually lapse), which risks the organisation under-investing in at-risk donors. Recency of giving is the single strongest driver of predictions, confirmed by both SHAP and LIME. A regional fairness gap is present: the model over-predicts retention for the South region and is much less accurate there.

## One limitation of the model
The model shows a meaningful **fairness gap by region** — accuracy for the South region drops to about 0.42 and retention is systematically over-predicted there — and it **overfits** at the chosen tree depth. As a result it is suitable only as an **early prototype**, and should be retrained at a shallower depth and recalibrated by region before any real business use.

## Files in this repository
- `Nonprofit_Donor_Retention_Assignment.ipynb` — completed Jupyter notebook
- `Nonprofit_Donor_Retention_Assignment.pdf` — PDF export of the notebook
- `nonprofit_donor_retention_dataset.csv` — dataset
- `README.md` — this file

## How to run
```bash
pip install pandas numpy matplotlib scikit-learn shap lime
jupyter notebook Nonprofit_Donor_Retention_Assignment.ipynb
```
Run the cells top to bottom; each task is self-contained and depends only on cells above it.
