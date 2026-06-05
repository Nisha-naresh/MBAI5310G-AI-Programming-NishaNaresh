# ProcurePro Office Supplies
## Supplier Delay Risk Segmentation Using K-means Clustering

---

### Course Information
| Field | Detail |
|---|---|
| Student | Nisha Naresh |
| Student ID | 101008896 |
| Course | MBAI 5310G-001: AI Programming |
| University | Ontario Tech University |
| Instructor | Zahra Atf |

---

### What This Project Does
This project uses unsupervised machine learning to discover hidden
patterns in supplier purchase order data. Instead of treating every
order the same way, K-means clustering groups orders into three
meaningful segments based on supplier behaviour, delivery history,
and order characteristics. The goal is to help ProcurePro procurement
managers identify high-risk orders early and take action before
delivery failures happen.

---

### Business Problem
ProcurePro Office Supplies is a B2B procurement service that helps
medium-sized organizations such as consulting firms, schools, clinics,
and coworking spaces source and manage office-related products.

The core challenge is supplier delivery uncertainty. Late deliveries
cause empty inventory shelves, delayed internal projects, emergency
replacement purchases, and reduced customer satisfaction. Every day
a delayed order goes unnoticed is a day the business loses the
opportunity to intervene.

Without a data-driven approach, procurement managers must manually
review hundreds of orders to decide which ones need attention. This
project automates that process by grouping orders into clear risk
segments so that the team knows exactly where to focus first.

---

### Dataset
| Item | Detail |
|---|---|
| File | procurepro_supplier_delay_risk_dataset.xlsx |
| Rows | 360 purchase orders |
| Columns | 20 |
| Missing Values | 127 filled using median and mode |
| Duplicate Rows | 0 |
| Target Column | Supplier_Delay_Risk (Yes / No) |
| Features Used for Clustering | 10 numerical features |

**Features used for clustering:**

| Feature | What It Measures |
|---|---|
| Order_Value_CAD | Total value of the purchase order |
| Number_of_Line_Items | Number of product lines in the order |
| Promised_Lead_Time_Days | Delivery days promised by the supplier |
| Past_On_Time_Rate | Historical on-time delivery rate |
| Supplier_Rating | Overall supplier performance score |
| Quality_Incidents_Last_6M | Quality issues in the last 6 months |
| Prior_Delays_Last_6M | Delivery delays in the last 6 months |
| Distance_KM | Distance between supplier and delivery point |
| Inventory_Buffer_Days | Safety stock days held in inventory |
| Seasonal_Demand_Index | Seasonal demand pressure index |

---

### Clustering Method
| Item | Detail |
|---|---|
| Algorithm | K-means Clustering |
| Number of Clusters | 3 selected using Elbow Method |
| Scaling Method | StandardScaler |
| Dimensionality Reduction | PCA with 2 components for visualization |
| PCA Explained Variance | 27.52% |
| Library | scikit-learn |

The number of clusters was chosen by running the Elbow Method across
K values from 1 to 10. The inertia dropped sharply from K=1 to K=3
and slowed significantly after K=3, confirming that 3 clusters is
the most efficient and interpretable choice for this business problem.

---

### Main Results

#### Cluster Summary
| Segment | Orders | On-Time Rate | Supplier Rating | Quality Incidents | Inventory Buffer |
|---|---|---|---|---|---|
| Low Risk Reliable Suppliers | 139 | 0.88 | 4.22 | 0.37 | 17.65 days |
| Moderate Risk Suppliers | 125 | 0.71 | 3.15 | 0.76 | 17.44 days |
| High Delay Risk Suppliers | 96 | 0.83 | 3.99 | 1.70 | 8.96 days |

#### What Each Segment Means

**Low Risk Reliable Suppliers (139 orders)**
The safest group. These suppliers have the highest on-time rate,
the highest supplier rating, and the fewest quality incidents.
Despite being located the furthest away at an average of 1112 km,
they consistently deliver on time. These are the benchmark suppliers
for ProcurePro.

**Moderate Risk Suppliers (125 orders)**
The middle group. These suppliers have the lowest on-time rate and
supplier rating across all segments. They need structured monitoring
and proactive communication to prevent delays from escalating.

**High Delay Risk Suppliers (96 orders)**
The most urgent group. These suppliers have the highest quality
incidents at 1.70 per order and the lowest inventory buffer days
at 8.96. There is very little safety stock to absorb delays, making
early intervention critical for every order in this segment.

---

### Business Recommendation
The three segments discovered give ProcurePro a clear action plan:

| Segment | Recommended Action |
|---|---|
| High Delay Risk Suppliers | Assign backup suppliers, increase inventory buffer, send early reminders, require frequent status updates |
| Moderate Risk Suppliers | Send proactive milestone reminders, review shipping modes, offer performance improvement incentives |
| Low Risk Reliable Suppliers | Offer preferred contract terms, volume commitments, and recognition programs |

The most important insight from this project is that the High Delay
Risk segment has the lowest inventory buffer days of only 8.96 days.
This means there is very little time to react once a delay starts.
Early identification of these orders is not just useful, it is
essential for protecting customer satisfaction and avoiding emergency
procurement costs.

All model predictions should be reviewed by procurement managers
before taking contract action. Supplier performance can change due
to weather disruptions, operational improvements, or market
conditions that are not captured in historical data. Human judgment
remains essential at every decision point.

---

### Key Insight
> The single most actionable finding from this project is that
> High Delay Risk orders have only 8.96 inventory buffer days on
> average. Once a delay starts for these orders, the business has
> less than 9 days before shelves go empty. Early detection through
> clustering gives procurement teams the time they need to act.

---

### Limitations
- The dataset is synthetic and may not reflect real supply chain complexity
- K-means assumes equally sized circular clusters which may not match reality
- PCA explains only 27.52% of total variance meaning clusters have complex structure
- Historical supplier data may not reflect recent improvements or disruptions
- Model should never be used to make automatic contract decisions without human review

---

### Repository Structure
