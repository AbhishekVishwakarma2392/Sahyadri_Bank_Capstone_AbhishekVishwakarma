# Sahyadri Bank Digital Transformation Roadmap
### Team Capstone Project


# Executive Recommendation Summary

Sahyadri Bank should execute a **phased digital transformation strategy** by prioritising **Loan Origination** as the first transformation domain (**Value: 4.25, Feasibility: 4.00**), enabled through **Initiative I9 – Digital Loan Journey Rebuild**.

Initiative I9 represents an **Operational Transformation** delivering:

- **Investment:** ₹180 lakh
- **3-Year Benefit:** ₹990 lakh
- **Benefit-to-Investment Ratio:** 5.50×

This exceeds the board's benchmark target of **5.0× return per ₹ invested**.

However, the downside stress test scenario (**-30% benefit, +30% investment**) lowers the return ratio to **2.96×**, indicating execution risk. Therefore, implementation should begin with a **90-day Proof of Concept (PoC)** before committing full-scale capital investment.

### Recommended Transformation Sequence

#### Wave 1
- Loan Origination (I9)

#### Wave 2
- First-Account Onboarding

#### Defer Until Later Stages
- I2 – Merchant Payments App
- I4 – Wealth & Insurance Marketplace
- I7 – SME Supplier-Lender Marketplace

Operational initiatives should first establish core digital capabilities and generate measurable financial returns before large-scale platform investments.

---

# Part 1 – Transformation Classification & Business Models

## 1. Failure Modes & Mitigations

| Failure Mode | Description | Recommended Fix |
|-------------|------------|----------------|
| Lack of Urgency | Branch managers view digital transformation as optional | Establish time-bound digital KPIs linked to performance reviews |
| Insufficient Leadership | CEO communicates vision but assigns no owner | Appoint a Chief Digital Officer (CDO) with P&L accountability |
| Limited Vision | Multiple disconnected apps without strategic architecture | Define a unified target operating model and domain architecture |
| Weak Execution Capabilities | Cloud and data skill gaps delay delivery | Upskill teams and deploy cross-functional agile pods |
| Missing Middle-Out Leadership | Process managers excluded from redesign initiatives | Assign process managers as Product Owners |

---

## 2. Initiative Inventory & Classification Matrix

| ID | Initiative | Transformation Type | Business Model | Description |
|----|------------|--------------------|---------------|-------------|
| I1 | Digitise Branch Paperwork | Operational Transformation | Product | Replaces paper account-opening forms with digital forms |
| I2 | Merchant Payments App | Business-Model Transformation | Platform | Multi-sided payments ecosystem connecting merchants and consumers |
| I3 | SME Cash-Flow Solution | Business-Model Transformation | Solution | Integrated credit, accounting and payments offering |
| I4 | Wealth & Insurance Marketplace | Strategic Transformation | Platform / Solution | Expansion into adjacent financial-service ecosystems |
| I5 | Digital Cheque Clearing | Operational Transformation | Product | Digitises physical cheque movement and clearing |
| I6 | Customer-Service Chatbot | Operational Transformation | Product | Automates customer support queries |
| I7 | SME Supplier-Lender Marketplace | Business-Model Transformation | Platform | Connects SMEs, suppliers and lenders |
| I8 | AI-Assisted Collections Reminders | Operational Transformation | Product | Uses analytics-driven collections communication |
| I9 | Digital Loan Journey Rebuild | Operational Transformation | Product | Digitises end-to-end loan processing |

---

## 3. Business Model Grid

### Product
**Example:** Standard savings account sold over the counter

- Low customisation
- Low comprehensiveness

### Project
**Example:** Custom infrastructure loan for a dam builder

- High customisation
- Low comprehensiveness

### Solution
**Example:** SME Cash-Flow Solution (I3)

- High customisation
- High comprehensiveness

### Platform
**Example:** Merchant Payments App (I2)

- Low-to-medium customisation
- High comprehensiveness

### Grid Dimensions

| Axis | Description |
|--------|------------|
| Horizontal | Standardised ←→ Highly Customised |
| Vertical | Single Product ←→ Multi-Sided Ecosystem |

---

## 4. Portfolio Financial Summary by Transformation Type

### Formula

\[
3\text{-Year Benefit per ₹ Invested} = \frac{Annual Benefit \times 3}{Investment}
\]

| Transformation Type | Count | Investment (₹ Lakh) | Annual Benefit (₹ Lakh) | 3-Year Benefit per ₹ | Rank |
|-------------------|--------|--------------------|------------------------|---------------------|------|
| Operational Transformation | 5 | 360 | 720 | 6.00 | Best |
| Business-Model Transformation | 3 | 700 | 1,010 | 4.33 | 2nd |
| Strategic Transformation | 1 | 600 | 500 | 2.50 | Worst |
| **Portfolio Total** | **9** | **1,660** | **2,230** | **4.03** | — |

### Key Finding

✅ **Operational Transformation delivers the strongest financial return (6.00×).**

❌ **Strategic Transformation delivers the weakest return (2.50×).**

---

# Part 2 – Payments App Platform Analysis

## 1. Pipeline vs Platform Classification

| Offering | Classification | Rationale |
|-----------|---------------|-----------|
| Home Loans | Pipeline | Linear value chain from bank to borrower |
| Merchant Payments App | Platform | Connects merchants and consumers |
| SME Supplier-Lender Marketplace | Platform | Multi-sided lender ecosystem |
| Fixed Deposits | Pipeline | Traditional product sale model |

---

## 2. Platform Sides & Network Effects

### Platform Participants

1. Consumers
2. Merchants
3. Sahyadri Bank (Platform Owner)

### Same-Side Network Effects

As consumer adoption rises, peer-to-peer usability increases, attracting additional users.

### Cross-Side Network Effects

**Consumers → Merchants**

More users increase merchant incentive to accept the platform.

**Merchants → Consumers**

More merchant acceptance increases customer utility.

### Feedback Loop

```text
More Consumers
        ↓
More Merchants
        ↓
More Utility
        ↓
More Consumers
```

---

## 3. Metcalfe's Law Analysis

### Formula

\[
Network\ Value = n^2
\]

where:

- n = customer base (thousands)

| Quarter | Bank Customers (k) | Merchants (k) | Network Value | Rival Customers (k) | Rival Network Value | Value Ratio |
|----------|-------------------|---------------|---------------|---------------------|--------------------|------------|
| Q1 | 40 | 3.0 | 1,600 | 70 | 4,900 | 0.33 |
| Q2 | 55 | 4.5 | 3,025 | 80 | 6,400 | 0.47 |
| Q3 | 75 | 6.5 | 5,625 | 90 | 8,100 | 0.69 |
| Q4 | 100 | 9.0 | 10,000 | 100 | 10,000 | 1.00 |
| Q5 | 130 | 12.5 | 16,900 | 110 | 12,100 | 1.40 |
| Q6 | 170 | 17.0 | 28,900 | 120 | 14,400 | 2.01 |

### Findings

- Rival parity achieved in **Q4**
- Sahyadri surpasses rival in **Q5**
- Q6 valuation multiple reaches **2.01×**

### Correlation Results

| Entity | Correlation (Customers vs Merchants) |
|----------|----------|
| Sahyadri Bank | 0.999 |
| Rival | 1.000 |

**Note:** Correlation demonstrates association rather than definitive causation.

---

## 4. Ecosystem Driver Assessment

### Participants

1. Customers
2. Merchants
3. Sahyadri Bank
4. POS / Device Manufacturers
5. Regulators

### Capability Assessment

| Ecosystem Driver | Rating |
|------------------|----------|
| Brand Strength | Strong |
| Customer Experience | Partial |
| Relationship Ownership | Strong |
| Value Extraction | Partial |
| Destination Status | Partial |

---

## 5. Strategic Platform Recommendations

### Merchant Acquisition Subsidies
Accelerate onboarding through POS subsidies and reduced transaction fees.

### Value-Added Merchant Services
Provide:

- Inventory management
- Digital invoicing
- Working-capital financing

### Open Developer API Ecosystem
Enable third-party development and ecosystem innovation through open APIs.

---

# Part 3 – Domain Prioritisation & Zero-Based Redesign

## 1. Domain Evaluation Matrix

**Selection Threshold: 3.50**

| Domain | Value Score | Feasibility Score | Quadrant | Decision |
|----------|-----------|------------------|---------|----------|
| Loan Origination | 4.25 | 4.00 | High Value / High Feasibility | Priority #1 |
| First-Account Onboarding | 3.50 | 3.50 | High Value / High Feasibility | Priority #2 |
| Merchant Payments | 3.75 | 3.25 | High Value / Low Feasibility | Defer |
| Wealth Advisory | 3.00 | 3.50 | Low Value / High Feasibility | Low Priority |
| Collections | 2.50 | 3.75 | Low Value / High Feasibility | Low Priority |

### Selected Domain

🏆 **Loan Origination**

---

## 2. Domain Structure Classification

| Domain | Classification |
|----------|-----------|
| Loan Origination | Workflow / Process |
| First-Account Onboarding | Customer Journey |
| Merchant Payments | Workflow / Process |
| Wealth Advisory | Business Function |
| Collections | Workflow / Process |

---

## 3. Value-Lever Hierarchy

### Domain
Loan Origination

### Value Levers

#### Turnaround-Time Reduction
Faster disbursal and lower customer drop-offs.

#### Processing Cost Optimisation
Eliminates paperwork and manual re-entry.

#### Risk Mitigation
Advanced credit scoring through real-time data.

### Solution

**End-to-End Digital Loan Platform**

### Core Use Cases

- Online application portal
- Automated verification
- Digital sanction letters
- E-signature integration

---

## 4. Zero-Based Redesign

### Target Objective

Reduce loan processing time:

**12 Days → 6 Days (50% Reduction)**

| Step | Current State | Design Principle | Future State |
|--------|-------------|-----------------|--------------|
| 1 | Paper application form | Digitise | Self-service online application |
| 2 | Manual re-entry | Automate | Direct digital ingestion |
| 3 | Physical document checking | Integrate | API-driven verification |
| 4 | Physical sanction signature | Empower | Automated approval & e-sign |
| 5 | Manual disbursement call | Orchestrate | Automated disbursement |

---

# Part 4 – Board Dashboard, Business Case & Governance

## 1. Power BI DAX Measure

```DAX
3-Year Return per ₹ =
SUM(initiatives[annual_benefit_lakh]) * 3
/
SUM(initiatives[investment_lakh])
```

---

## 2. Portfolio KPI Dashboard

| KPI | Value |
|------|------|
| Total Investment | ₹1,660 lakh |
| Total Annual Benefit | ₹2,230 lakh |
| 3-Year Return per ₹ | 4.03 |

### Operational Transformation Only

| KPI | Value |
|------|------|
| Investment | ₹360 lakh |
| Annual Benefit | ₹720 lakh |
| 3-Year Return per ₹ | 6.00 |

---

## 3. Initiative Performance Matrix

| ID | Initiative | Investment (₹ Lakh) | Annual Benefit (₹ Lakh) | Return per ₹ | Status |
|----|------------|--------------------|-------------------------|-------------|--------|
| I1 | Digitise Branch Paperwork | 60 | 120 | 6.00 | 🟢 |
| I2 | Merchant Payments App | 250 | 400 | 4.80 | 🔴 |
| I3 | SME Cash-Flow Solution | 150 | 260 | 5.20 | 🟢 |
| I4 | Wealth & Insurance Marketplace | 600 | 500 | 2.50 | 🔴 |
| I5 | Digital Cheque Clearing | 30 | 90 | 9.00 | 🟢 |
| I6 | Customer-Service Chatbot | 40 | 70 | 5.25 | 🟢 |
| I7 | SME Supplier-Lender Marketplace | 300 | 350 | 3.50 | 🔴 |
| I8 | AI-Assisted Collections Reminders | 50 | 110 | 6.60 | 🟢 |
| I9 | Digital Loan Journey Rebuild | 180 | 330 | 5.50 | 🟢 |

---

## 4. Business Case Analysis – Initiative I9

### Problem Statement

The current loan process requires:

- Paper forms
- Manual re-keying
- Physical document checks
- Physical signatures

Resulting in a **12-day average turnaround time**.

### Solution

An integrated digital lending platform providing:

- Online applications
- API-based validation
- Automated decisions
- E-signature capability

### Technology Requirements

- e-KYC Integration
- Credit Bureau APIs
- Tax Database APIs
- Workflow Automation
- E-Sign Gateway

### Financial Analysis

| Metric | Value |
|----------|------|
| Investment | ₹180 lakh |
| Annual Benefit | ₹330 lakh |
| 3-Year Benefit | ₹990 lakh |
| Return Ratio | 5.50× |

### Stress Test Scenario

| Metric | Worst Case |
|----------|-----------|
| Investment (+30%) | ₹234 lakh |
| Annual Benefit (-30%) | ₹231 lakh |
| 3-Year Benefit | ₹693 lakh |
| Return Ratio | 2.96× |

### Recommendation

Launch a **90-day Proof-of-Concept (PoC)** before full deployment.

---

## 5. Agile Pod Governance Model

### Pod Structure (8 Members)

| Role | Count |
|--------|-------|
| Product Owner | 1 |
| Scrum Master | 1 |
| Software Engineers | 2 |
| UX/UI Designer | 1 |
| Data Engineer | 1 |
| Business Analysts / SMEs | 2 |

### Delivery Lifecycle

#### Discovery
- Product Owner
- Business Analysts
- UX/UI Designer

#### Proof of Concept / MVP
- Software Engineers
- Data Engineer
- Business Analyst

#### Production Deployment
- Full Pod

#### Change Management
- Product Owner
- Business Analyst
- UX/UI Designer

### Accountability Matrix

| Step | Owner |
|--------|-------|
| Problem Definition | Product Owner |
| Solution Design | Business Analyst / SME |
| Data & Technology Design | Software & Data Engineering Lead |
| Financial Case | Product Owner / Financial Analyst |
| Implementation Plan | Scrum Master |

---

# Final Recommendation

✅ Prioritise **Loan Origination (I9)** as the first transformation domain.

✅ Execute a **90-day Proof-of-Concept** before full-scale rollout.

✅ Move **First-Account Onboarding** into Wave 2.

✅ Focus initial investment on **Operational Transformation initiatives**, which deliver the strongest portfolio return (**6.00× per ₹ invested**).

✅ Delay high-cost platform and marketplace initiatives until operational efficiencies generate cash reserves and foundational digital capabilities are firmly established.

---
**Capstone Project | Digital Transformation Strategy & Platform Economics | Sahyadri Bank**
