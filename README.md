FraudShield AI
AI-Powered Fraud Detection & AML Intelligence Platform — All Payment Types
Live demo: #https://ajayfoluso.github.io/fraudshield/

Proof of Concept v3.2.0 — Built for regulatory demonstration and institutional review


What Is FraudShield AI?
FraudShield AI is an AI-powered fraud detection and anti-money laundering (AML) screening platform that works across all payment methods and fund transfer types — wire transfers, ACH, SWIFT, SEPA, crypto, P2P, mobile money, cash deposits, and card payments.
A compliance analyst enters details about a financial transaction — payer identity, payee identity, amount, and transfer type — and the system returns:

A risk score (0–100) computed across 5 AI models
Explainable AI signals describing exactly why the score was assigned in plain English
8 live database checks against OFAC, FinCEN, Interpol, card hotlists, network graphs, and AML typologies
A timestamped case ID, exportable audit log, and AI-assisted SAR draft — ready for regulatory submission

The platform is designed to catch fraud, money laundering, and suspicious activity before it causes damage — across every payment rail — while simultaneously generating a paper trail presentable to FinCEN, the US Treasury, and USCIS.

Who Uses It
AudienceUse CaseBank compliance teamsReal-time screening across all payment rails before funds are releasedFintech fraud departmentsWire, ACH, P2P, crypto, and card fraud detectionAML investigatorsMoney laundering pattern detection, structuring alerts, cross-border analysisRegulators & auditorsFinCEN, Treasury, USCIS review — full audit trail and SAR draft generation

Payment Methods & Transfer Types Covered
FraudShield analyzes all of the following with the same risk engine, AI models, and database checks:
Payment TypeExample Fraud ScenariosACH TransferStructuring under $10k, unauthorized debits, account takeoverWire Transfer (Domestic)Business email compromise, mule accountsWire Transfer (International)Sanctions evasion, high-risk jurisdiction routingSWIFTCorrespondent bank fraud, cross-border layeringSEPAEuropean fraud rings, first-party fraudCredit / Debit CardStolen card, card testing, CNP fraudPrepaid / Gift CardSocial engineering scams, fraud payout vehicleCrypto TransferWallet screening, mixer detection, exchange fraudP2P (Zelle / Venmo)Romance scams, impersonation, off-hours transfersCash DepositSmurfing, structuring, bulk cash placementMobile MoneyDeveloping market fraud, SIM swap exploitation

Card-specific verification signals (BIN lookup, CVV match, AVS, 3D Secure, hotlist check) activate only when a card account type is selected. All other payment types use behavioral, network, and sanctions-based signals.


Key Features
Universal Transaction Analysis

Full payer and payee profiles — name, account type, KYC status, account age, prior chargebacks
195-country dropdowns for both origin and destination
Time-of-day detection, IP/country mismatch, device channel, 30-day volume baseline
Structuring pattern detection (sub-$10k BSA threshold)
First-time recipient flagging
High-risk and FATF grey/black list country detection

Card-Specific Fraud Detection (activates for card types)

Secure tokenization — raw card numbers are never stored; the processor returns a token + verification signals
BIN lookup — identifies issuing bank, card type, and country
Verification signals: AVS address match, CVV result, 3D Secure, name match score, declined attempts, multi-card device detection
Card hotlist check — screens against known stolen and compromised card feeds

8 Database Checks — All Payment Types
Every analysis fires checks against 8 data sources, displayed live with status (CLEAR / WARNING / FLAGGED):
DatabaseSourceApplies ToOFAC SDNUS Treasury OFAC APIAll payment typesFinCEN 314(a)FinCEN Secure PortalAll payment typesInterpol / WatchlistsInterpol i-Link / ComplyAdvantageAll payment typesDevice FingerprintSardine / Seon / ThreatMetrixAll payment typesNetwork Graph DBInternal Neo4j Graph DBAll payment typesAML TypologiesFATF / FinCEN LibraryAll payment typesBIN DatabaseMastercard BIN APICard transactions onlyCard HotlistRippleshot / Ethoca / Visa DMCard transactions only

In this proof of concept, database responses are simulated. In production, each fires a live API call within 50–350ms.

AI Model Ensemble

Isolation Forest
Random Forest
Logistic Regression
Graph Neural Network (detects hidden connections between accounts)
BIN / Card Intelligence (activates for card transactions only)

Regulatory Outputs

Timestamped case ID and exportable audit log
AI-assisted SAR (Suspicious Activity Report) draft — downloadable, ready for compliance officer review before FinCEN submission
Plain-English explainable AI signals for every risk flag


How Fraud Is Detected Without a Card Number
For non-card transactions (wire, ACH, crypto, P2P, mobile money), fraud is detected entirely through behavioral and contextual signals:

Payer KYC status and account age
Payee sanctions screening (OFAC, FinCEN, Interpol)
Transaction amount vs. 30-day historical baseline
Destination country risk (FATF grey/black list)
Time of day and IP/country mismatch
Structuring pattern detection
First-time recipient flag
Hidden network connections via graph analysis
AML typology pattern matching

These signals are weighted across 5 AI models to produce the composite risk score. No card data required.

Regulatory Alignment
StandardCoverageFinCEN FIN-2024-A011Geofit Deepfake TypologiesTreasury AI MRF 2025Explainability Mandate §3.4BSA / 31 CFR 1010Structuring & STR ElementsFATF Recommendations 16 & 20Wire transfer rules & STR filingOFAC SDN ScreeningSanctions list cross-checkPCI DSS 4.0Card data handling & tokenizationGDPR Article 22Automated decision-making safeguards

Proof of Concept Status
What is fully functional:

All input fields and form logic across all payment types
Risk scoring engine
Explainable AI signal generation
Simulated database check animations with realistic results
SAR draft generator (downloadable .txt file)
Audit log exporter

What is simulated:

External database API calls (OFAC, FinCEN, Rippleshot, Sardine, etc.)
Card tokenization flow (demonstrates the architecture without connecting to Stripe/Visa)

Production roadmap:

Connect live OFAC SDN API, FinCEN Secure Portal, Rippleshot feed
Integrate Stripe Elements for real card tokenization
Add crypto wallet screening (Chainalysis / Elliptic)
Add analyst case management queue with role-based access
Deploy real-time transaction monitoring via webhook ingestion


Tech Stack

Pure HTML / CSS / JavaScript — no frameworks, no dependencies
Zero backend — runs entirely in the browser
Deployable to any static host (GitHub Pages, Netlify, Vercel)


Getting Started

Clone or download this repository
Open index.html in any browser — or deploy to GitHub Pages
Select any payment/account type and fill in transaction details
Click Run Analysis
Watch all 8 database checks fire in real time in the middle panel
View risk score, AI signals, and model breakdown on the right
Download the SAR draft or audit log from the Case Management panel


FraudShield AI · Proof of Concept v3.2.0
Covers: ACH · Wire · SWIFT · SEPA · Crypto · P2P · Mobile Money · Cash · Cards
Aligned to FinCEN FIN-2024-A011 · BSA 31 CFR 1010 · FATF Rec. 16 & 20 · PCI DSS 4.0 · Treasury AI MRF 2025
