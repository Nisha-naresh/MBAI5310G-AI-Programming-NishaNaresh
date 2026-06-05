# Decision Tree Classification Projects
## NovaMart Retail and PayFlow Business Solutions

### Course Information
| Field | Detail |
|---|---|
| Student | Nisha Naresh |
| Student ID | 101008896 |
| Course | MBAI 5310G-001: AI Programming |
| University | Ontario Tech University |
| Instructor | Zahra Atf |

---

## Table of Contents
1. Repository Overview
2. Project 1: NovaMart Retail
3. Project 2: PayFlow Business Solutions
4. Repository Structure

---

## Repository Overview
This repository contains two Decision Tree classification projects completed
for the MBAI 5310G-001 AI Programming course at Ontario Tech University.
Both projects follow the same structure: understanding the business problem,
preparing the data, training a Decision Tree model, and interpreting the
results from a business perspective. Each project includes a Jupyter
Notebook, dataset, business report, and chart outputs.

---

## Project 1: NovaMart Retail
### Inventory Reorder Prediction

### Business Problem
NovaMart Retail is a mid-sized retail company that sells everyday products
through physical stores and an online channel. The business faces two major
inventory problems: stockouts, where products run out before the next
supplier delivery, and overstock, where too much inventory is ordered.
NovaMart needs a model to identify which products are likely to need a
reorder before a stockout happens so that managers can act earlier and
reduce both lost sales and unnecessary inventory costs.

### Dataset
| Item | Detail |
|---|---|
| File | novamart_inventory_reorder_dataset.xlsx |
| Rows | 365 |
| Columns | 18 |
| Target Variable | Reorder_Needed (Yes / No) |
| Reorder Needed: No | 250 |
| Reorder Needed: Yes | 115 |

### Machine Learning Model
| Item | Detail |
|---|---|
| Model | Decision Tree Classifier |
| Library | scikit-learn |
| Train/Test Split | 80% training, 20% testing |
| Random State | 42 |

### Main Evaluation Results
| Metric | Score |
|---|---|
| Training Accuracy | 1.0000 |
| Testing Accuracy | 0.7639 |
| Precision | 0.6667 |
| Recall | 0.4545 |
| F1-Score | 0.5405 |
| Overfitting Gap | 0.2361 |

### Confusion Matrix Results
| | Predicted No | Predicted Yes |
|---|---|---|
| Actual No | 45 (True Negative) | 5 (False Positive) |
| Actual Yes | 12 (False Negative) | 10 (True Positive) |

### Key Business Insights
- Current_Stock_Units is the strongest predictor of reorder need
- Lead_Time_Days helps determine how far in advance to reorder
- Website_Views reflects online demand and signals potential stockouts
- Recall is the most important metric because missing a reorder causes stockouts and lost sales
- The model shows overfitting and needs pruning before full deployment
- False negatives are more costly than false positives for NovaMart

### SWOT Analysis
| Strengths | Weaknesses |
|---|---|
| Simple and explainable rules managers can understand | Model is overfitting with training accuracy of 100% |
| Automates reorder decisions across hundreds of products | Low recall of 0.4545 means many reorder needs are missed |
| Current_Stock_Units and Lead_Time_Days are strong predictors | Synthetic dataset may not reflect real business patterns |
| Reduces manual workload for inventory managers | Does not handle new products with limited history well |
| Fast predictions with low computational cost | Decision Tree is sensitive to small changes in data |

| Opportunities | Threats |
|---|---|
| Apply max_depth pruning to reduce overfitting | False negatives cause stockouts and lost revenue |
| Add real-world data such as promotions and supplier delays | False positives cause overstock and higher holding costs |
| Integrate model into NovaMart inventory management system | Over-reliance on model without human review is risky |
| Expand model to predict reorder quantity not just Yes or No | New product categories not in training data may be misclassified |
| Use model results to negotiate better lead times with suppliers | Model may become outdated as business conditions change |

### One Limitation
The dataset is synthetic and does not capture real-world factors such as
supplier delays, local events, promotions, or new product history. New
products with limited sales history may be underestimated by the model,
meaning it may not support new product launches effectively. Real-world
factors such as economic conditions and seasonal demand changes are also
not captured in the dataset.

---

## Project 2: PayFlow Business Solutions
### Invoice Late Payment Prediction

### Business Problem
PayFlow Business Solutions helps small and medium-sized businesses manage
invoicing and payment collection. Late invoice payments create serious
cash-flow problems for businesses. When customers pay late, companies may
struggle to pay suppliers, manage payroll, and plan future growth. PayFlow
wants to identify invoices that are at high risk of being paid late before
the due date passes, so that staff can prioritize follow-up actions and
support customers earlier before payment issues become serious.

### Dataset
| Item | Detail |
|---|---|
| File | payflow_invoice_late_payment_dataset.xlsx |
| Rows | 360 |
| Columns | 17 |
| Target Variable | Late_Payment (Yes / No) |
| Late Payment: No | 201 |
| Late Payment: Yes | 159 |

### Machine Learning Model
| Item | Detail |
|---|---|
| Model | Decision Tree Classifier |
| Library | scikit-learn |
| Train/Test Split | 80% training, 20% testing |
| Random State | 42 |

### Main Evaluation Results
| Metric | Score |
|---|---|
| Training Accuracy | 1.0000 |
| Testing Accuracy | 0.5556 |
| Precision | 0.5000 |
| Recall | 0.5625 |
| F1-Score | 0.5294 |
| Overfitting Gap | 0.4444 |

### Confusion Matrix Results
| | Predicted No | Predicted Yes |
|---|---|---|
| Actual No | 22 (True Negative) | 18 (False Positive) |
| Actual Yes | 14 (False Negative) | 18 (True Positive) |

### Key Business Insights
- Days_Since_Last_Order is the strongest predictor of late payment
- Avg_Days_To_Pay reflects historical payment speed and is a reliable risk signal
- Prior_Late_Payments directly identifies high-risk customers
- Invoice_Amount suggests larger invoices carry higher late payment risk
- Recall is the most important metric because missing a late invoice causes cash-flow problems
- The model shows severe overfitting and needs pruning before business deployment
- False negatives are more costly because PayFlow loses the chance to intervene early

### SWOT Analysis
| Strengths | Weaknesses |
|---|---|
| Explainable rules that finance teams can understand | Model is overfitting with training accuracy of 100% |
| Automates late payment risk flagging across all invoices | Testing accuracy of 55.56% is low and unreliable |
| Avg_Days_To_Pay and Prior_Late_Payments are strong predictors | Recall of 0.5625 means many late payments are still missed |
| Reduces manual follow-up workload for collections staff | Synthetic dataset may not reflect real payment behaviour |
| Fast and low-cost predictions for each invoice | Decision Tree is sensitive to small changes in invoice data |

| Opportunities | Threats |
|---|---|
| Apply max_depth pruning to reduce overfitting | False negatives cause missed late invoices and cash-flow problems |
| Add real-world data such as economic conditions and contract terms | False positives cause unnecessary customer contact |
| Integrate model into PayFlow invoicing dashboard | Over-reliance on model without human review is risky |
| Use predictions to trigger automated early reminders | Bias may unfairly associate certain regions with late payment |
| Expand model to predict expected days to payment | Model may become outdated as payment behaviour changes |

### One Limitation
The dataset is synthetic and does not reflect real-world payment complexity.
Real payment behaviour is affected by factors not included in the dataset
such as seasonal business cycles, economic conditions, contract terms, and
personal relationships with account managers. The model may also unfairly
associate certain regions or industries with late payment without enough
business context.

---

## Repository Structure
```
decision-tree-projects/
│
├── README.md
│
├── NovaMart/
│   ├── NovaMart_Decision_Tree.ipynb
│   ├── novamart_inventory_reorder_dataset.xlsx
│   ├── NovaMart_Decision_Tree_Report.docx
│   └── charts/
│       ├── confusion_matrix.png
│       ├── train_vs_test.png
│       ├── feature_importance.png
│       └── target_distribution.png
│
└── PayFlow/
    ├── PayFlow_Decision_Tree.ipynb
    ├── payflow_invoice_late_payment_dataset.xlsx
    ├── PayFlow_Decision_Tree_Report.docx
    └── charts/
        ├── cm_payflow.png
        ├── tvt_payflow.png
        ├── fi_payflow.png
        └── td_payflow.png
```
