# Process Maps: BomaSuite Property Management

## Current-State Process (Manual Workflow)

### Phase 1: Tenant Onboarding
*Historically, onboarding involved physical application forms, manual background checks, and in-person meetings for lease signing.*

```mermaid
flowchart TD
    A[Prospective Tenant tours property] --> B[Given paper rental application]
    B --> C[Returns application with deposit check]
    C --> D[Caretaker manually runs background check]
    D --> E{Approved?}
    E -->|Yes| F[Landlord prints lease agreement]
    E -->|No| G[Caretaker calls to reject]
```

### Phase 2: Move-In & Rent Collection
*Lease signing required in-person coordination, and rent was collected as physical checks or cash, necessitating bank runs and spreadsheet entry.*

```mermaid
flowchart TD
    F[Approved Tenant] --> H[In-person meeting to sign lease]
    H --> I[Tenant moves in]
    I --> J[Tenant mails/drops off rent]
    J --> K[Manager deposits cash at bank]
    K --> L[Manual entry into accounting spreadsheet]
```

## Future-State Process (Automated System)

### Phase 1: Digital Onboarding & Leasing
*Onboarding is now initiated via email invite, allowing tenants to set up profiles, sign leases digitally, and pay initial deposits online.*

```mermaid
flowchart TD
    A[Prospective Tenant tours property] --> B[Manager creates Tenant invite in system]
    B --> C[System emails Magic Link]
    C --> D[Tenant completes profile online]
    D --> E[System auto-generates digital Lease]
    E --> F[Tenant signs digitally via e-Signature]
```

### Phase 2: Automated Rent Collection & Billing
*The system natively integrates with M-Pesa to capture payments instantly, automatically reconciling the ledger and generating monthly invoices.*

```mermaid
flowchart TD
    F[Signed Lease] --> G[Tenant pays deposit & rent via M-Pesa]
    G --> H[BomaSuite C2B integration captures payment]
    H --> I[System auto-reconciles ledger & updates Dashboard]
    I --> J[System auto-generates monthly rent & water invoices]
```
