# GS-Financial-Data-Integrity-Audit
Applying BSc Computer Science principles to audit financial data integrity, resolve logic breaks, and implement operational risk controls within a simulated Goldman Sachs Wealth Management workflow.
# 🏦 Financial Data Integrity & Operational Audit

**Project Type:** Systems-Oriented Wealth Management Simulation  
**Developer Background:** BSc Computer Science  
**Domain:** Fintech Operations & Risk Mitigation  

## 📖 Executive Summary
This project involves a high-fidelity operational audit of a wealth management transaction pipeline. Moving beyond simple bookkeeping, this analysis applies **Software Engineering principles**—such as data validation, exception handling, and root cause analysis—to financial workflows. The objective was to identify systemic "logic breaks" within a ₹250,000 portfolio and refactor the data model to ensure zero-fail settlement.

## 🛠️ Technical Stack & Methodology
- **Analytics Engine:** Microsoft Excel (Advanced Data Modeling & Statistical Functions)
- **Methodology:** - **RCA (Root Cause Analysis):** Identifying why calculations fail at the data-ingestion layer.
    - **Schema Standardization:** Enforcing strict data types across the ledger.
    - **Risk Control Framework:** Implementing T-1 liquidity verification protocols.

## 🔍 In-Depth Technical Analysis & "Debugging"

### 1. Data Type Conflict & Schema Refactoring
During the audit, I identified a critical **Calculation Break**. The ledger was attempting to aggregate values containing string prefixes (the `₹` symbol). 

* **The Problem:** Non-numeric characters were passed into the `SUM` function, causing a logical error and inaccurate reporting.
* **The Resolution:** I refactored the column schema to **Numeric/Float** types and moved the currency indicator to the metadata/header layer. This ensured 100% computational accuracy and enabled automated data visualization.

### 2. Operational Risk & Fail-Safe Design
In a BSc CS context, this is equivalent to **Exception Handling**. To prevent "Transaction Time-out" or "Insufficient Fund" errors:

* **Pre-Trade Logic:** Implemented a **T-1 Liquidity Verification**. If the system detects a capital deficit 24 hours before settlement, a risk alert is triggered.
* **Automated Triggers:** Established time-based triggers for recurring obligations (Subscriptions/Service Fees) to eliminate manual entry lag and prevent late-fee penalties.

### 3. Workflow Optimization (Standardization)
I transitioned unstructured, manual transaction logs into a **Standardized Reporting Schema**. By categorizing "Needs" vs "Wants" as data parameters, the model allows for granular querying of capital allocation, similar to how a database manages structured entries.

## 📂 Repository Structure
- [Financial_Data_Integrity_Project_SOW.pdf](./Financial_Data_Integrity_Project_SOW.pdf) : The architectural project scope and technical requirements.
- [Operational_Workflow_Audit_Analysis.xlsx](./Operational_Workflow_Audit_Analysis.xlsx) : The final refactored data model containing the audit trail.

## 📊 Data Source
Simulated Wealth Management data provided by the **Goldman Sachs: Operations Job Simulation** via **Forage**.
