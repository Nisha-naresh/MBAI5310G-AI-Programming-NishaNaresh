# MBAI5310G-AI-Programming-NishaNaresh

## Student Information
- **Name:** Nisha Naresh
- **Student ID:** 101008896
- **Course:** MBAI 5310G, AI Programming
- **University:** Ontario Tech University
- **Term:** Spring 2026
- **Instructor:** Zahra Atf

## Repository Overview
This repository contains my weekly applied coding tasks and final project for MBAI 5310G. The work focuses on AI programming, machine learning, deep learning, NLP, model evaluation, GitHub-based documentation, and responsible AI reflection. The weekly assignments move from supervised classification (decision trees) to unsupervised learning (clustering) and on to model evaluation and business interpretation, and the final project is a research proposal on explainable multimodal AI in healthcare.

## Weekly Assignments
- **Week 02:** Bank customer churn prediction. Data preparation and a supervised classification workflow on the bank customer churn dataset.
- **Week 03:** Bank customer churn prediction continued, with model comparison and classification outputs.
- **Week 04:** Decision Tree classification, two business cases. **NovaMart Retail** predicts whether a product needs reordering before a stockout (target `Reorder_Needed`), and **PayFlow Business Solutions** predicts late invoice payments. Both use a `DecisionTreeClassifier` in scikit-learn with an 80/20 train and test split, and each includes a notebook, dataset, business report, and result charts (confusion matrix, feature importance, target distribution, train vs test).
- **Week 05:** Supplier delay risk segmentation for **ProcurePro Office Supplies** using K-means clustering. An unsupervised workflow groups 360 purchase orders into three risk segments so procurement managers can prioritise high-risk orders, with PCA, elbow, scatter, and bar visualisations.
- **Week 06:** Customer support escalation prediction. A supervised classification workflow on the customer support escalation dataset (`customer_support_escalation_dataset.csv`) that prepares and cleans the data, trains and evaluates a model, and interprets the main drivers of escalation for the business. The pipeline follows four stages: data preparation, model development, model evaluation, and business interpretation.

## Final Project
**Explainable Multimodal AI for Clinical Prediction and Patient-Specific Medical Decision Support.**

The final project is a research proposal (paper) on multimodal AI for healthcare. In plain terms, it sets out a system that would look at several kinds of patient data at once (structured records, clinical notes, and medical images or signals), predict a clinical outcome such as deterioration, and then explain *why* it made that prediction for the individual patient. The proposal evaluates three things that are usually treated separately: predictive performance, the reliability of the explanations (faithfulness and stability), and whether the explanations actually help clinicians trust and use the result. It proposes an empirical, mixed-methods data-science study that would combine a computational strand (model building and technical evaluation) with a human-centered strand (a structured study of clinician trust). Full details, including background, problem statement, research gap, methodology, ethics, timeline, and references, are in the `Research Paper/` folder.

## Repository Structure
- `assignment/`: weekly applied tasks (week-02 to week-06)
- `Research Paper/`: final project proposal, paper, and documentation
- `README.md`: this file

```
MBAI5310G-AI-Programming-NishaNaresh/
│
├── README.md
│
├── assignment/
│   ├── week-02/
│   │   ├── readme.md
│   │   ├── Assignment 2_Nisha_Naresh.ipynb
│   │   ├── bank_customer_churn_prediction_dataset.xls
│   │   └── class_Worksheets/
│   │
│   ├── week-03/
│   │   ├── README.md
│   │   ├── Assignment 3_Naresh_Nisha.ipynb
│   │   ├── bank_customer_churn_prediction_dataset.xls
│   │   └── class_worksheets/
│   │
│   ├── week-04/
│   │   ├── Readme.md
│   │   ├── NovaMart_Decision_Tree/
│   │   │   ├── Novamart_Decision_Tree.ipynb
│   │   │   ├── NovaMart_Decision_Tree_Report.docx
│   │   │   ├── novamart_inventory_reorder_dataset/
│   │   │   │   ├── novamart_inventory_reorder_dataset.xlsx
│   │   │   │   └── business_plan_novamart_inventory_reorder.docx
│   │   │   └── model_results/
│   │   │       ├── confusion_matrix.png
│   │   │       ├── feature_importance.png
│   │   │       ├── target_distribution.png
│   │   │       └── train_vs_test.png
│   │   │
│   │   └── Payflow_Decision_Tree/
│   │       ├── Payflow_Decision_Tree.ipynb
│   │       ├── PayFlow_Decision_Tree_Report.pdf
│   │       ├── payflow_invoice_late_payment_dataset/
│   │       │   ├── payflow_invoice_late_payment_dataset.xlsx
│   │       │   └── payflow_invoice_late_payment_business_plan.docx
│   │       └── model_results/
│   │           ├── cm_payflow.png
│   │           ├── fi_payflow.png
│   │           ├── td_payflow.png
│   │           └── tvt_payflow.png
│   │
│   ├── week-05/
│   │   ├── Readme.md
│   │   └── procurepro_supplier_delay_risk/
│   │       ├── procurepro_supplier_delay_risk.ipynb
│   │       ├── ProcurePro_Segmentation_Report.pdf
│   │       ├── procurepro_supplier_delay_risk_dataset/
│   │       │   ├── procurepro_supplier_delay_risk_dataset.xlsx
│   │       │   └── procurepro_supplier_delay_risk_business_plan.docx
│   │       └── model_results/
│   │           ├── bar_procurepro.png
│   │           ├── elbow_procurepro.png
│   │           ├── pca_procurepro.png
│   │           ├── scatter_procurepro.png
│   │           └── target_procurepro.png
│   │
│   └── week-06/
│       ├── readme.md
│       ├── Assignment 6_Nisha_Naresh.ipynb
│       └── customer_support_escalation_dataset.csv
│
└── Research Paper/
    ├── Readme.md
    └── paper/
        └── Research_Proposal_Explainable_Multimodal_AI.docx   (the research paper)
```

## Tools Used
- Python
- Jupyter Notebook / Google Colab
- GitHub
- scikit-learn (Decision Tree classification, K-means clustering)
- pandas and NumPy
- matplotlib for visualisations
- TensorFlow / Keras
- Other libraries as needed

## Responsible AI Note
All work in this repository is for educational purposes. I will not upload confidential, private, sensitive, copyrighted, or restricted datasets. When using AI tools for support, I will disclose how they were used and verify the final work.
