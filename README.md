# Loan Portfolio Analysis

This project performs a comprehensive financial and risk performance analysis of the **Prosper Loan Dataset**, using SQL queries and Tableau visualizations. The objective is to assess lending performance metrics such as loan disbursement trends, borrower risk profiles, interest recovery, losses, and profitability.

---

## Project Structure

```
├── Data Definition Language.sql         # SQL script to create the data table
├── prosper loan dataset.csv             # Raw dataset in CSV format
├── Analysis.sql                         # SQL queries for summary-level insights
├── Loan_Portfolio_Analysis.sql         # SQL queries for portfolio-specific metrics
├── Metrics.sql                          # Monthly loan performance and borrower metric queries
├── Variable definitions.pdf             # Complete dictionary of variables in the dataset
└── Loan Performance Metrics.twbx        # Tableau workbook with visual analysis dashboards
```

---

## Dataset

- **Source**: Prosper Marketplace
- **File**: `prosper loan dataset.csv`
- **Description**: This dataset contains details on ~113K loans issued between 2005 and 2014, including borrower profiles, loan terms, repayment performance, credit scores, and Prosper ratings.

---

## 🛠️ Setup Instructions

1. **Load the Dataset into MySQL**:
   - Use the `Data Definition Language.sql` to create the `prosperloandata_temp` table.
   - Load the dataset with:
     ```sql
     LOAD DATA LOCAL INFILE 'path_to/prosper loan dataset.csv' INTO TABLE prosperloandata_temp
     FIELDS TERMINATED BY ',' ENCLOSED BY '"' 
     LINES TERMINATED BY '\r\n' IGNORE 1 LINES;
     ```

2. **Run SQL Queries**:
   - Use `Analysis.sql`, `Loan_Portfolio_Analysis.sql`, and `Metrics.sql` to explore various insights.
   - Ensure you update any database/table names as needed.

3. **Explore Tableau Dashboard**:
   - Open `Loan Performance Metrics.twbx` in Tableau Desktop.
   - Explore dynamic charts and summaries for disbursement, losses, recovery rates, and more.

---

## Key Analyses

### From `Analysis.sql`
- Total loan disbursed
- Average APR and borrower rate
- Net principal loss and recovery amounts
- Average monthly payment
- Total interest and service fees

### From `Loan_Portfolio_Analysis.sql`
- Loan disbursement grouped by Prosper rating
- Distribution and trends of loan amounts

### From `Metrics.sql`
- Month-wise loan performance
- Average profit/loss per month
- Debt-to-income trends

---

## Variable Reference

Refer to `Variable definitions.pdf` for detailed explanations of 80+ fields such as:

- `LoanStatus`, `BorrowerAPR`, `ProsperRatingAlpha`
- `DebtToIncomeRatio`, `LP_NetPrincipalLoss`, `LoanOriginationDate`, etc.

---

## Visualizations (Tableau Highlights)

- Disbursement Trend Over Time
- Recovery vs Loss by Quarter
- Loan Grade vs APR Comparison
- Monthly Debt-to-Income Overview

---

## Technologies Used

- **MySQL** for data storage and analysis
- **Tableau** for visualization and dashboarding
- **SQL** for data exploration and metric extraction

---

## Outcome

This project helps stakeholders understand:

- Lending profitability and risk metrics
- Borrower behavior and loan trends
- Data-driven insights to improve loan performance strategy

---
