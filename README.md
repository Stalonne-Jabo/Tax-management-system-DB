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
- *Taxpayer (Individual or Company): Submits tax forms, makes payments, views status*.
- *Tax Authority(Tax Officer): Receives processed forms, conducts audits, generates reports, manages compliance*.
- *Payment: Facilitates online tax payments*.
- *System Database(Tax Management System): Processes forms, validates data, generates assessments, records payments, provides notifications*.
  
#### BPMN Diagram

![Conceptual Diagram](https://github.com/Stalonne-Jabo/photos/blob/main/BPMN%20Diagram.png)

### MIS Functions Supported:
- *Decision Support: Real-time dashboards for revenue analysis*.
- *Transaction Processing: Secure tax filing and payment recording*.
- *Audit Trail: Tracks all user and system interactions*.
  
## PHASE III: Logical Model Design.

#### Tasks and Deliverables:

1. Entity-Relationship (ER) Model: Identify and define entities, attributes, primary keys (PKs), and foreign keys (FKs).
2. Relationships & Constraints: Establish relationships (one-to-one, one-to-many, many-to-many) and apply constraints (NOT NULL, UNIQUE, CHECK, DEFAULT).
3. Normalization: Ensure 3rd Normal Form (3NF) is achieved.
4. Handling Data Scenarios: Validate model handles real-world tax scenarios.
5. Presentation & Feedback: Well-documented and clearly labeled model.
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
  
  #### ERD Diagram
  
 ![Conceptual Diagram](https://github.com/Stalonne-Jabo/photos/blob/main/ERD%20Diagram.png)

## PHASE IV: Pluggable Database Creation and Naming

 ![Conceptual Diagram](https://github.com/Stalonne-Jabo/photos/blob/main/pluggable%20creation.jpg)

## PHASE V: Table implementation and Data insertion
![Conceptual Diagram](https://github.com/Stalonne-Jabo/photos/blob/main/table.jpg,https://github.com/Stalonne-Jabo/photos/blob/main/table1.jpg,)
## PHASE VI: Database interaction and Transactions
*This function calculates tax due based on the declaration and the applicable tax rate.*
![Conceptual Diagram](https://github.com/Stalonne-Jabo/photos/blob/main/function.jpg)

*This procedure submits a declaration and logs the status in the audit log.*
![Conceptual Diagram](https://github.com/Stalonne-Jabo/photos/blob/main/procedure.jpg)

*The package that organizes your procedures and functions for the Tax Management System.*
![Conceptual Diagram](https://github.com/Stalonne-Jabo/photos/blob/main/pkg.jpg)

*The package body that Provides reusable and modular code, Improves performance through persistent memory of package state and Groups related logic together.*
![Conceptual Diagram](https://github.com/Stalonne-Jabo/photos/blob/main/pkg%20body.jpg,https://github.com/Stalonne-Jabo/photos/blob/main/body.jpg)

## PHASE VII: Advanced Database Programming and Auditing
*The auditing logic using triggers and the AuditLog table to track user activity (who did what, when, and whether it was allowed or denied).*
![Conceptual Diagram](https://github.com/Stalonne-Jabo/photos/blob/main/trg.jpg)

*This advanced database programming phase significantly enhances the Tax Management System's security and aligns with its objectives by:

- **Enforcing Strict Compliance**: This is crucial for maintaining data integrity and preventing unauthorized changes when direct oversight might be limited.
- **Automated Auditing**: This provides an immutable record of who attempted what, when, and whether it was allowed or denied.
- **Accountability and Traceability**: In case of discrepancies or security incidents, administrators can easily trace back the actions, identifying the source of any unauthorized attempts.
- **Deterrence**: The knowledge that all actions are logged and restrictions are in place acts as a strong deterrent against malicious or accidental data manipulation.
-**Operational Control**: This mechanism ensures that critical data is only modified during designated periods, reducing the risk of errors or fraudulent activities.*
