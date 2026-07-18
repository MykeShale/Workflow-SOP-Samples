# Standard Operating Procedure (SOP): Loan Origination & Approval

**System**: TawiLend Loan Management System
**Audience**: Loan Officers & Branch Managers
**Last Updated**: October 2023

## Purpose
To outline the standard procedures for reviewing, approving, and managing loan applications utilizing the new TawiLend automated portal.

## 1. Daily System Checks
* **Login**: Access the TawiLend Staff Dashboard at `staff.tawilend.com` using your SSO credentials.
* **Review Dashboard Alerts**: Check the "Action Required" widget for applications flagged for manual review or pending document verification.

## 2. Processing Flagged Applications
Applications that do not meet the criteria for Auto-Approval but pass the baseline checks are routed to the "Manual Review" queue.

1. Navigate to **Applications** -> **Pending Review**.
2. Select an application to view the consolidated applicant profile.
3. Review the **System Risk Assessment** score and the associated flags (e.g., "Income verification unclear").
4. Inspect uploaded documents via the built-in document viewer.
5. **Decision**:
   * Click **Approve** and enter the approved loan amount and interest rate.
   * Click **Request More Info** to send an automated email to the applicant specifying missing details.
   * Click **Reject** and select a standard rejection reason from the dropdown.

## 3. Monitoring Disbursements
Disbursements for approved loans are handled automatically by the system API at 4:00 PM daily.
* **Verification**: Branch Managers should review the **Daily Disbursement Report** generated at 4:30 PM.
* **Exceptions**: Any API failures will appear in the **Exceptions Queue**. Finance must manually retry or investigate these specific cases.

## 4. Collections & Arrears Management
The system automatically sends SMS/Email reminders 3 days before a payment is due and on the due date.
1. Navigate to **Collections** -> **Arrears Dashboard**.
2. Accounts 1-15 days overdue receive automated follow-ups. No manual action is needed.
3. For accounts 16+ days overdue, click **Assign to Agent**.
4. Log all communication attempts in the **Activity Log** section of the borrower's profile.
