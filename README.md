# D2C Churn Intelligence — Part 2: RFM Segmentation & Retention Strategy

Customer segmentation using RFM scoring and behavioural signals, with targeted retention actions for each segment.

**Snapshot date:** 2025-09-30  
**Customers:** 2,400  
**Churn window:** Next 60 days

---

## Repository Structure

```
d2c-churn-part2-rfm/
├── rfm_segmentation.ipynb    # Full RFM analysis, segment creation, charts
├── segments.csv              # 2,400 customers with segment labels + features
├── retention_strategy.md     # Per-segment retention playbook + budget allocation
├── manual_review_cases.md    # 10 ambiguous customers with specific decisions
├── charts/                   # Saved chart outputs from the notebook
├── data/                     # Place dataset CSV files here (see below)
├── requirements.txt
└── README.md
```

---

## Data Setup

Download the dataset from the Google Drive link provided in the project brief, then place all CSV files in the `data/` folder:

```
data/
├── customers.csv
├── orders.csv
├── support_tickets.csv
├── web_events_snapshot.csv
├── churn_labels.csv
├── intervention_history.csv
└── rfm_modeling_snapshot.csv
```

---

## Installation

```bash
pip install -r requirements.txt
```

---

## Running the Analysis

```bash
jupyter notebook rfm_segmentation.ipynb
```

Run all cells top to bottom. Charts will be saved to `charts/` and `segments.csv` will be written at the end.

---

## Segments Created

| Segment | Count | Churn Rate |
|---|---|---|
| Champions | 401 | 10% |
| Loyal Customers | 499 | 22% |
| New Customers | 96 | 17% |
| Occasional Buyers | 490 | 59% |
| Discount-Sensitive | 202 | 55% |
| High-Value but Unhappy | 47 | 70% |
| At-Risk | 462 | 74% |
| Dormant | 203 | 91% |

**RFM scoring:** 1–5 per dimension (R/F/M) using quintile cuts.  
**Additional signals:** avg discount %, return rate, support ticket count + negativity rate, 30-day web sessions.

---

## Key Findings

- Customers with RFM score ≤ 6 churn at 77%+; those with RFM ≥ 13 churn at <12%.
- Dormant customers (n=203, 91% churn) have near-zero discount usage — they didn't respond to existing campaigns. Reactivation ROI is poor.
- High-Value but Unhappy (n=47) represent the highest revenue-at-risk per customer (avg ₹2,350 spend, 70% churn). Product quality or service failure — not price — is the driver.
- Discount-Sensitive customers average 44% discount vs 28% for Champions. More discounting here reduces margin without building loyalty.
- Budget prioritisation: At-Risk + High-Value Unhappy should receive ~50% of the retention budget.

---

## Output Files

- `segments.csv` — customer_id, segment_name, R/F/M scores, and key features
- `charts/` — 7 charts covering RFM distribution, churn by segment, signal heatmap, scatter plots
- `retention_strategy.md` — segment-level playbook + ₹2.5L budget allocation
- `manual_review_cases.md` — 10 specific customers with ambiguous signals and recommended actions
