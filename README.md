# fraudshield
# 🛡️ FraudShield — AI/ML Fraud Detection Intelligence System

An AI/ML fraud detection intelligence system combating synthetic identity fraud, deepfake account takeover, and AML evasion — aligned with FinCEN FIN-2024-A001 and the U.S. Treasury AI Risk Management Framework (2026).

-----

## 🔍 Overview

FraudShield is a browser-based fraud detection prototype that simulates real-time financial transaction risk scoring using ensemble machine learning models. It maps flagged transactions against documented financial crime typologies and produces explainable AI outputs to support compliance and investigative decision-making.

-----

## ⚙️ How It Works

### 1. Transaction Input

The system accepts simulated transaction parameters including:

- Transaction amount
- Country of origin
- KYC (Know Your Customer) verification status
- Transaction type (wire, ACH, crypto, etc.)
- Transaction frequency and prior volume

These inputs mirror real-world data points used by financial institutions to assess risk.

### 2. Multi-Model Ensemble Scoring

FraudShield runs each transaction through four independent models simultaneously:

|Model                  |Type           |What It Does                                                            |
|-----------------------|---------------|------------------------------------------------------------------------|
|**Isolation Forest**   |Unsupervised ML|Detects anomalies by isolating outlier transactions from normal patterns|
|**Random Forest**      |Supervised ML  |Uses decision trees trained on fraud indicators to classify risk        |
|**Logistic Regression**|Statistical ML |Calculates probability of fraud based on weighted input features        |
|**Threshold Rules**    |Rule-based     |Applies hard compliance rules (e.g., structuring detection near $10,000)|

Each model produces an independent risk score. The final **Ensemble Risk Score** is a weighted combination of all four outputs, reducing false positives and increasing detection reliability.

### 3. Explainable AI (XAI) Output

For every transaction, the system surfaces the specific signals that drove the risk score — such as:

- KYC mismatch detected
- Amount near structuring threshold
- High-risk jurisdiction flagged
- Unusual transaction velocity

This satisfies the explainability mandate outlined in the **U.S. Treasury Financial Services AI Risk Management Framework (February 2026)**, which requires that AI-driven financial decisions be interpretable by human reviewers.

### 4. FinCEN Typology Mapping

The system automatically maps flagged transactions against the six fraud typologies documented in **FinCEN Alert FIN-2024-A001 (November 2024)**:

1. Synthetic Identity Fraud
1. Structuring / Smurfing (AML evasion)
1. High-Risk Jurisdiction Activity
1. KYC Bypass Attempts
1. Abnormal Transaction Velocity
1. Sanctioned Entity Indicators

Each typology card updates in real time — showing CLEAR, REVIEW, or DETECTED status based on transaction inputs.

### 5. Risk Classification

The final ensemble score maps to one of four risk tiers:

|Score Range|Classification |Recommended Action               |
|-----------|---------------|---------------------------------|
|0–30       |🟢 Low Risk     |No action required               |
|31–59      |🟡 Medium Risk  |Enhanced monitoring              |
|60–79      |🟠 High Risk    |Manual review required           |
|80–100     |🔴 Critical Risk|Immediate escalation / SAR filing|

-----

## 🏛️ Regulatory Alignment

|Framework                  |Relevance                     |
|---------------------------|------------------------------|
|FinCEN Alert FIN-2024-A001 |Typology detection logic      |
|U.S. Treasury AI RMF (2026)|Explainable AI output design  |
|Bank Secrecy Act (BSA)     |AML structuring rules         |
|FATF Recommendations       |High-risk jurisdiction mapping|

-----

## 🛠️ Technology

- **Frontend:** HTML5, CSS3, Vanilla JavaScript
- **ML Simulation:** Client-side scoring logic modeling Isolation Forest, Random Forest, Logistic Regression, and rule-based thresholds
- **Deployment:** GitHub Pages (static hosting)
- **No external dependencies or API keys required**

-----

## 🎯 Purpose

This prototype was developed as part of an active research and development endeavor focused on applying artificial intelligence to financial crime prevention in support of U.S. financial system integrity.

-----

*Built and maintained by Foluso Ajayi*
