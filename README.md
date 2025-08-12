# RISK ANALYSIS DASHBOARD 
This project analyzes client data from a banking institution to assess loans, deposits, and risk exposure. The goal is to identify income, geographic, and product concentration risks while providing actionable recommendations for diversification. 

🛠️ **TOOLS AND TECHNOLOGIES USED**
- Excel (CSV) – Initial dataset storage and review

- MySQL – Data storage and relational database management

- Jupyter Notebook (Python) – Data cleaning, transformation, and analysis

- Power BI – Interactive data visualization and dashboard creation
  

📂 **DATASET INFORMATION**
**Source:** banking.csv

**Key Columns:**
Client ID, Name, Age, Location ID – Customer identification and demographics
Joined Bank – Date the client became a customer
Fee Structure – Banking service tier (High, Mid, Low)
Loyalty Classification – Client loyalty segmentation
Estimated Income, Superannuation Savings – Financial standing indicators
Amount of Credit Cards, Credit Card Balance – Credit product usage
Bank Loans, Business Lending – Loan portfolio insights
Checking Accounts, Saving Accounts, Foreign Currency Account – Deposit and account types
Properties Owned, Risk Weighting – Asset and risk profile


🔄 **WORKFLOW**
**1️⃣ Data Acquisition**
Obtained the dataset in .csv format containing client demographic, financial, and banking details.

**2️⃣ Data Storage (MySQL)**
Created a MySQL database schema to store the dataset.

Imported CSV into MySQL using the LOAD DATA INFILE command.

**3️⃣ Data Cleaning & Transformation (Python – Jupyter Notebook)**
- Connected MySQL database to Jupyter Notebook using mysql.connector

- Performed data cleaning:

* Handled missing values

* Removed duplicates

* Standardized column names and data types

- Conducted exploratory data analysis (EDA) to identify trends.

**4️⃣ Data Visualization (Power BI)**
Connected the cleaned dataset to Power BI.

Created 4 dashboard pages:

- Home (Overview) – KPIs & general metrics

- Loan Analysis – Loan portfolio breakdown

- Deposit Analysis – Deposit sources & trends

- Summary – Engagement, fees, and final recommendations



**INSIGHT GENERATION:**
Page 1 – Home (General Overview)
**Total Clients:** 1,190

**Total Loan:** $1.71B

**Total Deposits:** $1.49B

**Checking Accounts:** $383.08M

**Savings Accounts:** $277.79M

**Business Lending:** $1.02B

<img width="884" height="488" alt="c709d946bd2ca7a7abbba066ed7ddbec" src="https://github.com/user-attachments/assets/f92a2e51-f33a-4fbd-9fbe-a08b27266901" />


**Deeper Insights:**

Business lending makes up ~59% of the bank’s total loan portfolio.

Checking accounts hold 38% more funds than savings accounts — suggesting customers prefer liquid deposit accounts over long-term savings.

With $1.49B in deposits and $1.71B in loans, the loan-to-deposit ratio is ~115% — slightly aggressive, meaning the bank is lending more than it has in deposits.



Page 2 – Loan Analysis
**Bank Loans:** $692.99M (~40% of total loans)

**Business Lending:** $1.02B (~60% of total loans)

**Credit Card Balance:** $3.75M (~0.2% of total loans)

**Bank Loan by Income Band:**

**High income:** $347.55M (50.15%)

**Low income:** $178.76M (25.86%)

**Mid income:** $166.72M (24.06%)

**By Nationality:**

European clients dominate, followed by Asian, American, Australian, and African.

**By Occupation:**

Project Manager, Structural Analyst, Database Administrator take the highest bank loans.

Actuary, Accountant are among the lowest.

<img width="882" height="489" alt="862d8d294a6999e4698196b338fb3bc1" src="https://github.com/user-attachments/assets/ad0e9458-8e0a-44be-9976-f4b4c49a07c0" />


**Deeper Insights:**

High-income clients dominate loans — a concentration risk if the high-income group faces market shocks.

Credit card lending is minimal, suggesting a missed opportunity in consumer lending.

Loan concentration in specific occupations could be risky if those industries face downturns.



Page 3 – Deposit Analysis
**Total Deposit**: $1.49B

**Bank Deposit:** $794.52M (~53% of deposits)

**Deposit by Income Band:**

**High income:** $765.57M (51.49%)

**Low income:** $384.17M (25.79%)

**Mid income:** $339.62M (22.86%)

**Deposit by Nationality:**

Europeans: $655.4M (~44% of deposits)

Asians, Americans, Australians, Africans follow.

Deposit by Occupation:

Top: Social Worker, Structural Analyst, Database Administrator.

<img width="885" height="491" alt="54c89921ec651362c67d54bd50e8e4d8 (1)" src="https://github.com/user-attachments/assets/6a5d1a14-3856-49e5-804c-621a75e322d4" />


**Deeper Insights:**

High-income individuals not only dominate loans but also deposits — a double dependency risk.

European clients provide the largest share of both deposits and loans — a geographic concentration risk.

Social Workers leading deposits is unusual — possibly due to institutional deposits or a few high-value accounts in that category.



Page 4 – Summary
**Total Fees:** $22.56M

**Foreign Currency Accounts:** $33.97M

**Engagement Accounts:** 1,179 (~99% of clients)

**Bank Deposits:** $794.52M

<img width="883" height="491" alt="449ba57c37abc82aceaca2ce3a0625d3" src="https://github.com/user-attachments/assets/bec587c2-5cac-4542-b73c-503f6f072234" />




**Deeper Insights:**

Fees make up a relatively small fraction of total revenue potential — suggesting untapped fee-based income opportunities.

Foreign currency deposits are just 2.3% of total deposits — potential for growth in forex-linked products.

Nearly all clients are “engaged” (have active accounts), which is a strong retention indicator.





**RISK/EXPOSURE MATRIX**






| **Risk Factor**                 | **Exposure**  | **Reason for Concern**                                                                                              | **Mitigation Strategy**                                                         |
|----------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Income Concentration             | High          | 50%+ of loans and deposits come from high-income clients — vulnerable if this group’s economy slows.                 | Diversify lending/deposit base to mid and low-income segments.                   |
| Geographic Concentration         | High          | European clients dominate both deposits and loans (~44% of deposits, largest share of loans).                        | Expand into other regions to reduce geographic risk.                             |
| Product Concentration – Loans    | High          | 60% of loan portfolio in business lending; low diversification in consumer lending.                                  | Increase retail loan products (e.g., credit cards, personal loans).              |
| Product Concentration – Deposits | Medium        | Checking accounts hold significantly more than savings — risk if clients withdraw large amounts.                     | Introduce incentives for long-term savings products.                             |
| Loan-to-Deposit Ratio             | Medium-High   | 115% — aggressive lending could cause liquidity strain in downturn.                                                  | Build deposit base, especially from stable sources.                              |
| Occupational Risk                | Medium        | Loans and deposits concentrated in a few professions — industry downturns could affect repayment.                    | Broaden client base across more occupations.                                     |
| Low Fee Income                   | Low-Moderate  | $22.56M in fees — small portion of total business.                                                                    | Develop more fee-based services (insurance, wealth management).                  |
| Low Foreign Currency Holdings    | Low           | Only 2.3% of deposits — low exposure to FX products.                                                                  | Market FX and international products to existing clients.                        |


