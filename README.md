# CS-412: Comparative Machine Learning Approaches for Credit Card Fraud Detection on Imbalanced Data

**Track:** Application. **Student:** individual project. **Language:** Python.

## Quick start (Google Colab)
1. Open https://colab.research.google.com/ and choose **File > Upload notebook**.
2. Upload `notebooks/CS412_Fraud_Detection_Intermediate.ipynb`.
3. Download `creditcard.csv` from https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud and unzip it.
4. In Colab choose **Runtime > Run all**, upload `creditcard.csv` when prompted, and read the outputs.
5. Download `CS412_intermediate_outputs.zip` from the final cell.
6. Add the notebook, extracted figures, metrics CSVs, and reports to your GitHub repository. Do not push the dataset itself.

## Reproducible methodology
- Exact duplicate records are removed before splitting, and the count removed is printed.
- Stratified 60/20/20 train/validation/test split (`random_state=42`).
- Logistic Regression scales data via an in-training pipeline only.
- All baseline metrics are from the validation split. The test set is retained for the final study.
- Three models: Logistic Regression, Random Forest, and XGBoost.
- First imbalance experiment: `class_weight='balanced'` for Logistic Regression.

## Intermediate-report figures and tables
The notebook generates `results/raw_class_distribution.csv`, `split_summary.csv`,
`class_distribution.png`, `baseline_validation_metrics.csv`,
`baseline_confusion_matrices.png`, `baseline_precision_recall_curves.png`,
and `class_weight_experiment.csv`.

## References
- Branco et al. (2020), *Interleaved Sequence RNNs for Fraud Detection*, KDD.
- Chen and Guestrin (2016), *XGBoost: A Scalable Tree Boosting System*, KDD.
- Dal Pozzolo et al. (2015), *Calibrating Probability with Undersampling for Unbalanced Classification*, IEEE SSCI.
