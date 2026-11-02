# Intermediate Project Report — working outline (not submission-ready)
**Project title:** Comparative Machine Learning Approaches for Credit Card Fraud Detection on Imbalanced Data  
**Type:** Application (individual)

> This is a starter outline. Do not submit with placeholders or describe any model as trained until its code has actually run.

## 1. Introduction and Problem Description (~0.75–1 page)
Explain the real-world problem and false negatives versus false positives. State the research question: how do three algorithms and imbalance handling influence fraudulent transaction detection? Accuracy alone is uninformative given the rarity of fraud. Summarize prior work: Branco et al. (2020) KDD fraud-sequence approach; Chen & Guestrin (2016) KDD XGBoost.

## 2. Dataset (~0.75–1 page)
Source: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud . Original source contains 284,807 records, 492 labeled fraudulent, 31 columns. Feature names: `Time`, `V1`–`V28`, `Amount`; target is `Class`. **After notebook execution:** report actual missing cell count, duplicates removed, cleaned row count, train/validation/test counts, and the class-distribution figure.

## 3. Work Completed / Methodology / Preliminary Results (~1–2 pages)
**Complete this ONLY after running the notebook:** describe exact duplicate handling; stratified splits (60/20/20); baseline Logistic Regression pipeline with training-only scaling; Random Forest; XGBoost. Insert the generated validation metrics table and confusion matrices. Discuss differences in precision, recall, F1, ROC-AUC, and average precision without overstating findings. Explain the weighted Logistic Regression experiment, if executed.

[INSERT: actual `baseline_validation_metrics.csv` table]

[INSERT: actual `baseline_confusion_matrices.png` figure]

[INSERT: actual `class_weight_experiment.csv` findings]

## 4. Remaining Work (~0.5–0.75 page)
Compare additional class-imbalance strategies (e.g., SMOTE or undersampling **on training data only**); consider threshold selection on validation; repeat runs; compare tradeoffs; evaluate final chosen models once on held-out test; summarize in final report and 5–8 minute presentation. Note dataset anonymization and its limited temporal coverage as study limitations.

## References
[1] B. Branco et al., “Interleaved Sequence RNNs for Fraud Detection,” KDD 2020, doi:10.1145/3394486.3403361.
[2] T. Chen and C. Guestrin, “XGBoost: A Scalable Tree Boosting System,” KDD 2016, doi:10.1145/2939672.2939785.
[3] A. Dal Pozzolo et al., “Calibrating Probability with Undersampling for Unbalanced Classification,” IEEE SSCI 2015, doi:10.1109/SSCI.2015.33.
