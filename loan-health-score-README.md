Loan Health Score Dashboard

A credit risk analysis tool that scores bank loan applicants as **Low / Medium / High** risk — built to simulate the kind of decision-support tools used by credit officers at banks.

What This Project Does

Most loan analysis projects just show charts. This one goes further, it lets you input borrower details and instantly get a risk score with a plain-English explanation of *why* they're risky or safe.
🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core logic and data processing |
| SQL (PostgreSQL) | Storing and querying loan records |
| Pandas | Data cleaning and analysis |
| Streamlit | Interactive dashboard |
| Matplotlib / Seaborn | Charts and visualizations |

Project Structure

```
loan-health-score/
│
├── data/
│   └── loan_data.csv           # Raw dataset (Lending Club, Kaggle)
│
├── sql/
│   └── schema.sql              # Database schema
│   └── queries.sql             # Key SQL queries used for analysis
│
├── notebooks/
│   └── exploratory_analysis.ipynb   # Initial data exploration
│
├── app/
│   └── dashboard.py            # Streamlit app
│   └── scoring_logic.py        # Risk scoring functions
│
└── README.md
```

---

## 📊 Dataset

- **Source:** [Lending Club Loan Dataset — Kaggle](https://www.kaggle.com/datasets/wordsforthewise/lending-club)
- **Size:** 10,000+ loan records
- **Key Fields:** Loan amount, interest rate, debt-to-income ratio, credit history, employment length, loan status

How the Risk Score Works

The tool scores each borrower across 5 parameters:
1. **Debt-to-Income Ratio (DTI)** — lower is safer
2. **Credit History Length** — longer is safer
3. **Loan Amount vs. Income** — proportionality check
4. **Number of Past Delinquencies** — fewer is safer
5. **Employment Length** — stability indicator

Each parameter gets a sub-score. The final score maps to:
- 🟢 **Low Risk** — Safe to approve
- 🟡 **Medium Risk** — Needs further review
- 🔴 **High Risk** — Likely to default

Current Progress

- [x] Dataset downloaded and cleaned
- [x] SQL schema and database set up
- [x] Exploratory data analysis complete
- [x] Scoring logic built in Python
- [ ] Streamlit dashboard — in progress
- [ ] Explainability layer (plain-English reasons) — upcoming
