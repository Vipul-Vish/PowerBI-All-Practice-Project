# 🏦 India Banking Transactions Dashboard (Power BI)

An interactive Power BI dashboard that analyses **550K+ Indian bank transactions (2019-2024)** to understand payment behaviour, account mix, geography and loan opportunity.

> **Dataset:** India Bank Transactions (Kaggle) | **Tool:** Power BI Desktop | **Language:** DAX

![Dashboard Preview](ScreenShot/p8.png)


## 🎯 Project Overview

Banks generate huge volumes of transaction data, but raw numbers don't help decision-making. This project turns that data into a clean, interactive dashboard that answers: **who transacts, how they pay, where they are, and where the business opportunity lies.**

---

## ❓ Business Questions

- How many transactions happened, and what is the total and average value?
- Which payment modes (RTGS, NEFT, UPI, etc.) drive the most money?
- Which account types contribute the most transactions?
- Which states have the most loan customers?
- What share of customers has no loan (cross-sell opportunity)?
- How does transaction value change across years and months?

---

## 📂 Dataset

| Item | Details |
|---|---|
| Source | Kaggle: India Bank Transactions |
| Period | 2019 to 2024 (**2024 is partial data**) |
| Size | ~550K transactions |
| Key fields | transaction date, amount, transaction_type, account_type, channel, state, loan_type, has_loan, kyc_status, customer_id |

---

## 📊 Dashboard Features

**KPI cards**
- Total Transactions (550K)
- Total Amount (16.45bn)
- Monthly Growth %
- Average Transaction Amount

**Visuals**
- Total Amount by Year (column chart)
- Total Customers by Loan Type (column chart)
- Loan Customers by State (bar chart)
- Total Amount by Transaction Type (bar chart)
- Transactions by Account Type (donut chart)
- Transactions by State (map)
- Total Transaction Amount by Month (line chart)

**Slicers**
- Year Month, Channel, KYC Status (cross-filter the whole dashboard)

---

## 🔍 Key Insights

1. **High-value transfers drive the money.** RTGS accounts for the largest share of total transaction value, far ahead of Cheque and NEFT. Everyday modes like UPI, POS and ATM carry very little value in comparison.
2. **Savings accounts lead.** Savings ≈ 40% of transactions, Current ≈ 25%, Salary ≈ 20%, NRI ≈ 8%, Fixed Deposit ≈ 7%.
3. **Loan opportunity is big.** Most customers have no loan. Personal, Home and Auto loans are the largest loan categories among those who do.
4. **Geography matters.** Maharashtra, Karnataka, Tamil Nadu and Delhi have the highest number of loan customers, making them natural targets for loan product campaigns.
5. **Stable yearly volume.** Yearly transaction value stays at roughly 3.3bn from 2019 to 2023 (2024 is incomplete, so it is not comparable).

> 💡 **Recommendation:** Focus loan cross-sell campaigns on high-volume states and on Savings/Salary account holders who currently have no loan.

---

## 🧮 Data Model & DAX

A dedicated **Calendar (date) table** is connected to the transactions table and marked as the date table. This enables correct time intelligence and month sorting.



## 🧠 Challenges & Learnings

- **Month sorting:** Months were sorting by value instead of time. Fixed using a Month Num column and *Sort by column*, which removed a fake "downtrend".
- **Seasonality vs trend:** Plotting Month 1-12 across all years shows *seasonality*, not a time trend. For a true trend, use the Year Month axis.
- **Partial data:** 2024 has incomplete data, so it is clearly flagged to avoid misleading conclusions.
- **Currency formatting:** Formats like ₹ must be applied to the **measure/field**, not to the visual.
- **Design:** Clear titles, consistent colours and aligned visuals make a dashboard read like a story, not a pile of charts.

---

## ⚠️ Limitations

- 2024 data is incomplete, so yearly comparison with 2024 is not valid.
- Yearly totals are very uniform, which suggests the dataset may be synthetic. Insights are for learning and portfolio purposes, not real banking decisions.
- The dataset has no default or repayment fields, so loan *risk* cannot be analysed.

---

## 🚀 Future Improvements

- [ ] Page 2: Customer & Loan analysis (loan type vs state, loan penetration)
- [ ] Insight panel on the dashboard (Top finding / Risk / Recommendation)
- [ ] YoY growth visuals and Top-N analysis
- [ ] Drill-through and tooltip pages
- [ ] Page navigation buttons and more slicers (State, Account Type)

---

## ▶️ How to Use

1. Download the dataset from Kaggle: `<add dataset link here>`
2. Clone this repo:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   ```
3. Open `India_Banking_Dashboard.pbix` in **Power BI Desktop**.
4. If asked, update the data source path (*Transform data → Data source settings*) to your local CSV.
5. Click **Refresh** and explore using the slicers.

### 📁 Repository Structure
```
├── README.md
├── p8.pbix
├── ScreenShot/
│   └── p8.png
└── data/            
```

---

## 👤 Author

**Vipul Kumar**
Aspiring Data Analyst | BS Data Science, IIT Madras
Skills: SQL, Power BI, Excel, Python (Pandas), Linux

🔗 LinkedIn: `<https://www.linkedin.com/in/vipul-kumar-13b243378/>`

⭐ If you found this project useful, consider giving it a star and sharing your feedback!