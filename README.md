 Credit Risk Modeling (PD, LGD, EAD, EL & Scorecard)

This project presents a complete end-to-end Credit Risk Modeling framework involving model building, model testing, model validation, and risk quantification techniques used in financial institutions. The objective is to estimate Probability of Default (PD), Loss Given Default (LGD), Exposure at Default (EAD), and compute Expected Loss (EL), while also developing a fully interpretable credit scorecard.

 Project Overview

The workflow begins with extensive data preprocessing, including handling missing values, outlier treatment, categorical encoding, feature binning, and data transformation.

 PD Model (Logistic Regression)

Logistic Regression is used as the baseline PD model due to its interpretability.

Additional models like Random Forest and XGBoost are compared for performance.

Model testing: AUC-ROC, KS Statistic, Gini Index, Confusion Matrix.

Model validation: PSI, overfitting checks, significance testing.

 LGD Model (Two-Stage Modeling)

Implemented using:

Logistic Regression to classify whether LGD > 0

Linear Regression to estimate LGD amount for positive-LGD cases

This structure handles the semi-continuous nature of LGD.

 EAD Model (Linear Regression)

Linear Regression is used to estimate borrowers’ exposure at the time of default based on utilization rate, outstanding balance, and repayment characteristics.

 Expected Loss (EL) Calculation

The models are combined to compute EL:

EL
=
PD
×
LGD
×
EAD
EL=PD×LGD×EAD

This is essential for credit risk capital, provisioning, and pricing decisions.

 Scorecard Development

Weight of Evidence (WOE) transformation

Information Value (IV) ranking

Score scaling and cutoff creation

Segmentation into Low, Medium, and High-risk groups

 Repository Contents

Credit_Risk_data_preprocessing.ipynb – Data cleaning & preparation

Credit_risk_PD_model.ipynb – PD model development

Credit_risk_LGD_EAD_models.ipynb – LGD & EAD modeling

Credit_risk_PD_model_Monitoring.ipynb – Monitoring & PSI

 Conclusion

This project replicates a production-grade credit risk life cycle used in banking:
data preparation → model building → model testing → model validation → EL calculation → scorecard development.
