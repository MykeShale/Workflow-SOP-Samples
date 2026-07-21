# Process Maps: TawiLend Loan Management System

## Current-State Process (Manual Workflow)

### Phase 1: Intake & Approval
*In the legacy manual process, loan applications were heavily dependent on physical paperwork, manual data entry, and physical signatures.*

```mermaid
flowchart TD
    A[Applicant walks into branch] --> B[Fills out paper loan application]
    B --> C[Submits physical documents]
    C --> D[Officer enters data into Excel]
    D --> E{Manual Credit Check}
    E -->|Approved| F[Manager signs paper approval]
    E -->|Rejected| G[Mail rejection letter]
```

### Phase 2: Disbursement & Servicing
*Once approved, disbursement required manual bank transfers, and tracking payments relied entirely on manual updates to a master spreadsheet.*

```mermaid
flowchart TD
    F[Approved Loan] --> H[Finance initiates bank transfer]
    H --> I[Monthly tracking in spreadsheets]
    I --> J{Missed Payment?}
    J -->|Yes| K[Staff manually calls borrower]
    J -->|No| L[Mark paid in spreadsheet]
```

## Future-State Process (Automated System)

### Phase 1: Digital Intake & Automated Underwriting
*The new system provides a self-service portal for applicants and automates identity verification and initial credit scoring.*

```mermaid
flowchart TD
    A[Applicant registers on Portal] --> B[Completes digital app & uploads docs]
    B --> C[System auto-verifies identity & docs]
    C --> D{Automated Credit Engine}
    D -->|High Score| E[Auto-Approval via rules]
    D -->|Borderline| F[Flags for Manual Review]
    D -->|Low Score| G[Auto-Rejection & Email]
```

### Phase 2: Automated Disbursement & Servicing
*Approved loans are disbursed automatically via API, and the system handles payment scheduling, reminders, and collections tracking.*

```mermaid
flowchart TD
    E[Approved Loan] --> H[Automated Disbursement via API]
    H --> I[System auto-generates payment schedule]
    I --> J{Payment Due Date}
    J -->|Reminder| K[Auto-SMS/Email Reminder]
    J -->|Paid via Portal| L[Auto-reconciliation in Ledger]
    J -->|Missed| M[Auto-apply penalty & escalate]
```
