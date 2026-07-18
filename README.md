# SkyLution Workflow & SOP Samples

This repository contains real-world Standard Operating Procedures (SOPs), process maps, and client handover guides written for non-technical audiences. These documents are based on actual systems built for SkyLution clients, demonstrating the ability to translate complex technical workflows into actionable business operations documentation.

## Projects Included

### 1. TawiLend Loan Management System
A comprehensive SaaS platform for microfinance institutions to manage loan originations, approvals, and servicing.

**Deliverables:**
- [Standard Operating Procedure (SOP) / Runbook](./TawiLend/SOP_Runbook.md)
- [Client Handover Guide](./TawiLend/Client_Handover_Guide.md)

**Process Maps:**

*Current-State Process Map (Manual Process)*
```mermaid
flowchart TD
    A[Applicant walks into branch] --> B[Fills out paper loan application]
    B --> C[Submits physical documents]
    C --> D[Loan Officer manually enters data into Excel]
    D --> E{Manual Credit Check}
    E -->|Approved| F[Manager signs paper approval]
    E -->|Rejected| G[Mail rejection letter]
    F --> H[Finance initiates manual bank transfer]
    H --> I[Monthly tracking in spreadsheets]
    I --> J{Missed Payment?}
    J -->|Yes| K[Staff manually calls borrower]
    J -->|No| L[Mark paid in spreadsheet]
```

*Future-State Workflow (Automated System)*
```mermaid
flowchart TD
    A[Applicant registers on Member Portal] --> B[Completes digital application & uploads docs]
    B --> C[System auto-verifies identity & documents]
    C --> D{Automated Credit Scoring Engine}
    D -->|High Score| E[Auto-Approval via rules engine]
    D -->|Borderline| F[Flags for Manual Review by Officer]
    D -->|Low Score| G[Auto-Rejection & Email Notification]
    E --> H[Automated Disbursement via Payment API]
    F -->|Approved| H
    F -->|Rejected| G
    H --> I[System auto-generates payment schedule]
    I --> J{Payment Due Date Approaching}
    J -->|Reminder| K[Auto-SMS/Email Reminder Sent]
    J -->|Paid via Portal| L[Auto-reconciliation in Ledger]
    J -->|Missed| M[Auto-apply penalty & escalate to Collections Dashboard]
```

---

### 2. SkyLution Property Management System (BomaSuite)
An automated system for real estate managers to handle tenant onboarding, rent collection, and maintenance requests.

**Deliverables:**
- [Standard Operating Procedure (SOP) / Runbook](./BomaSuite/BomaSuite_SOP_Runbook.md)
- [Client Handover Guide](./BomaSuite/BomaSuite_Client_Handover_Guide.md)

**Process Maps:**

*Current-State Process Map (Manual Process)*
```mermaid
flowchart TD
    A[Prospective Tenant tours property] --> B[Given paper rental application]
    B --> C[Returns application with physical check for deposit]
    C --> D[Caretaker manually runs background check or references]
    D --> E{Approved?}
    E -->|Yes| F[Landlord prints lease agreement]
    E -->|No| G[Caretaker calls to reject]
    F --> H[In-person meeting to sign lease]
    H --> I[Tenant moves in]
    I --> J[Tenant mails or drops off monthly rent check/cash]
    J --> K[Manager physically deposits cash at bank]
    K --> L[Manual entry into accounting spreadsheet]
```

*Future-State Workflow (Automated System)*
```mermaid
flowchart TD
    A[Prospective Tenant tours property] --> B[Manager creates Tenant invite in BomaSuite]
    B --> C[System emails Magic Link to Tenant]
    C --> D[Tenant completes profile & sets up Portal Account]
    D --> E[System auto-generates digital Lease Agreement]
    E --> F[Tenant signs digitally via e-Signature API]
    F --> G[Tenant pays deposit & rent via M-Pesa]
    G --> H[BomaSuite C2B integration captures M-Pesa payment]
    H --> I[System auto-reconciles ledger & updates Landlord Dashboard]
    I --> J[System auto-generates monthly rent & water invoices]
```
