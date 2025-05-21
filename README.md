# **Tax-management-system-DB**
*Oracle PL/SQL database project for tax processing and MIS monitoring*
## Project Information
#### Group E
#### Student ID: 27551
#### Student name: JABO Stalonne

#### Project Tittle: Tax Management System

## OVERVIEW
*This project involves the design and development of a Tax Management System using Oracle PL/SQL. It includes data modeling, ERD design, database creation, and monitoring using Oracle Enterprise Manager (OEM)*.

## Phase I: PROBLEM DEFINITION & PRESENTATION

### Problem Definition:
*Government institutions often struggle with efficient and transparent tax collection, filing, and tracking. Manual methods or disconnected systems lead to errors, fraud, and delayed reporting that leads to tax evasion.There is a need for a centralized, automated system to streamline these operations, improve data accuracy, and enhance transparency*.

### Context:
*This system will be used by Rwanda Revenue Authority (RRA) and tax-paying businesses to manage taxes like VAT, PAYE, corporate income tax to manage their tax obligations and by authorities to process filings, monitor compliance and generate reports. It will be accessible online and integrated with existing financial systems where applicable.*

### Target Users:

- *Tax officers*.
- *Business owners*.
- *Accountants*.
- *Auditors*.
- *Tax Advisors*.
  
### Project Goals:

- *Automate tax declaration and payment tracking*.
- *Improve accuracy in tax calculations and reports*.
- *Provide secure access to tax records*.
- *Enforce deadline compliance through triggers and validations*.
  
### Features
- *Taxpayer registration and management*
- *Filing of tax returns*
- *Secure payment processing*
- *Assignment of tax officers*
- *Automated notifications*
  
## PHASE II: Business Process Modeling (MIS) using BPMN Diagram.

### Scope:
*To automate the submission of tax forms, track payment status, and provide real-time updates to taxpayers and tax authorities*.
*Taxpayer registers → Declares tax → System calculates automatically → Validates payments → Generates reports*.

### Entities:
- *Taxpayer (Individual or Company):Submits tax forms, makes payments, views status*.
- *Tax Authority(Tax Officer):Receives processed forms, conducts audits, generates reports, manages compliance*.
- *Payment:Facilitates online tax payments*.
- *System Database(Tax Management System):Processes forms, validates data, generates assessments, records payments, provides notifications*.
- 
#### BPMN Diagram

![Conceptual Diagram](https://github.com/Stalonne-Jabo/photos/blob/main/BPMN%20Diagram.png)

### MIS Functions Supported:
- *Decision Support: Real-time dashboards for revenue analysis*.
- *Transaction Processing: Secure tax filing and payment recording*.
- *Audit Trail: Tracks all user and system interactions*.
  
## PHASE III: Logical Model Design.

Design an ERD including:
- *Company(taxpayer_id, name, type, TIN, email, phone)*.
- *TaxType(tax_type_id, name, rate, description)*.
- *Declaration(declaration_id, taxpayer_id, tax_type_id, amount, date_declared, status)*.
- *Payment/Tax to be paid(payment_id, declaration_id, amount_paid, payment_date)*.
- *TaxAudit(log_id, user_id, action_type, date_time, status)*.
- *Holiday/Terms(holiday_id, Holiday_name,holiday_date)*
Apply normalization to 3NF and enforce constraints:
- *NOT NULL, UNIQUE on TIN, etc....*
- *CHECK on positive amounts*.
## Database Tables

- *Company*.
- *Tax Type*.
- *Tax to be paid*.
- *Terms/holidays*.
- *Tax audit*.

Each table includes constraints such as primary keys, foreign keys, NOT NULL, UNIQUE, CHECK, and default values.

## Oracle Enterprise Manager (OEM)

### OEM has been set up for:

1. *Monitoring database instance*.
2. *Managing schema objects*.
3. *Viewing performance metrics*.

## Screenshots included under OEM_Screenshots
