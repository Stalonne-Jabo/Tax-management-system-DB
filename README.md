# Tax-management-system-DB
Oracle PL/SQL database project for tax processing and MIS monitoring
## Project Information
#### Group E
#### Student ID: 27551
#### Student name: JABO Stalonne

#### Project Tittle: Tax Management System

## OVERVIEW
#### This project involves the design and development of a Tax Management System using Oracle PL/SQL. It includes data modeling, ERD design, database creation, and monitoring using Oracle Enterprise Manager (OEM).

## Phase I: PROBLEM DEFINITION & PRESENTATION

### Problem Definition:
Government institutions often struggle with efficient and transparent tax collection, filing, and tracking. Manual methods or disconnected systems lead to errors, fraud, and delayed reporting that leads to tax evasion.

### Context:
This system will be used by Rwanda Revenue Authority (RRA) and tax-paying businesses to manage taxes like VAT, PAYE, corporate income tax,etc.....

### Target Users:

- Tax officers
- Business owners
-Accountants
- Auditors
- Tax Advisors
  
### Project Goals:

- Automate tax declaration and payment tracking
- Improve accuracy in tax calculations and reports
- Provide secure access to tax records
- Enforce deadline compliance through triggers and validations
  
### Features
- Taxpayer registration and management
- Filing of tax returns
- Secure payment processing
- Assignment of tax officers
- Automated notifications
- 
## PHASE II: Business Process Modeling (MIS) using BPMN Diagram.

### Scope:
Taxpayer registers → Declares tax → System calculates automatically → Validates payments → Generates reports

### Entities:
- Taxpayer (Individual or Company)
- Tax Officer
- Tax Type (VAT, Income Tax,corporate tax, etc...)
- Declaration
- Payment
- System Database
- External Integrations (Banks, EBM)

### MIS Functions Supported:
- Decision Support: Real-time dashboards for revenue analysis
- Transaction Processing: Secure tax filing and payment recording
- Audit Trail: Tracks all user and system interactions

## Database Tables

- Taxpayer

- TaxReturn

- Payment

- TaxOfficer

- Notification

Each table includes constraints such as primary keys, foreign keys, NOT NULL, UNIQUE, CHECK, and default values.

## Oracle Enterprise Manager (OEM)

### OEM has been set up for:

1. Monitoring database instance

2. Managing schema objects

3. Viewing performance metrics

## Screenshots included under OEM_Screenshots
