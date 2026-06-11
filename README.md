# Designing Credit Card Rewards Around Real Customer Behavior
**A Data-Driven Approach to Product Design | K-Means Clustering + Reward Simulation**

---

## The Question

Most credit card rewards are built around *who* a customer is — income bracket, credit score, age group. But two customers with identical demographics can have completely different spending lives.

This project asks: **what happens when you design rewards around how people actually spend?**

---

## What This Project Does

Using transaction data from 5,000 credit card accounts, I:

1. **Segmented customers** into behavioral profiles using K-Means clustering on spend signatures (category percentages, transaction frequency, monthly volatility)
2. **Validated** that the segments are genuinely distinct — not just mathematical artifacts
3. **Designed a 3-tier card portfolio** mapped directly to the behavioral clusters
4. **Simulated profitability** using industry-standard interchange rates, stress-testing every segment × card combination

---

## Key Findings

- **Six distinct behavioral segments** emerged from the data — ranging from the Digital Power Shopper (29.4% of users, $3,210/month avg spend) to the Frequent Flyer (7.9%, $533/month)
- **The value gap is real:** two customers can share the same spending *pattern* while representing 6x different revenue opportunities
- **Three products serve 100% of users profitably** — confirmed by a full margin stress test across all segment × card combinations
- **Annual fees are structural, not arbitrary:** the Omni Digital tier's $120 fee exists because Online Retail interchange (~1.8%) sits below the reward rate. The fee bridges that gap.

---

## The Portfolio

| Product | Target Segment | Annual Fee | Strategic Role |
| :--- | :--- | :--- | :--- |
| **Everyday Essential** | Convenience Seeker, Modern Gifter, Frequent Flyer | $0 | Volume driver — 51%+ of users |
| **Omni Digital** | Digital Power Shopper | $120 | Growth engine — largest + highest-spend segment |
| **Apex Premium** | Wellness Whale, Socialite | $450 | Margin anchor — high-interchange categories |

---

## Files

| File | Description |
| :--- | :--- |
| `notebook.ipynb` | Full analysis — data audit, feature engineering, clustering, simulation |
| `deck.pptx` | 8-slide executive summary for non-technical audiences |

---

## Methods & Tools

- **Language:** Python
- **Clustering:** K-Means (scikit-learn) with Elbow Method + Silhouette Score for k selection
- **Feature Engineering:** Spend category percentages, transaction frequency, monthly spend volatility, credit utilization ratio
- **Simulation:** Interchange-based margin model (industry-average Mastercard/Visa World Elite rates)
- **Libraries:** pandas, numpy, scikit-learn, seaborn, matplotlib

---

## Data

**Source:** [Credit Card Transactions dataset](https://www.kaggle.com/datasets) via Kaggle  
5,000 unique accounts · multi-category transaction data · no PII

---

## How to Run

```bash
git clone https://github.com/YOUR_USERNAME/credit-card-rewards-clustering
cd credit-card-rewards-clustering
pip install -r requirements.txt
jupyter notebook notebook.ipynb
```

> **Note:** Update the data path in the notebook's import cell to point to your local copy of the Kaggle dataset.

---

*Interchange rates used in the simulation are industry estimates for Mastercard/Visa World Elite tiers. Actual rates are negotiated privately between networks and issuers.*
