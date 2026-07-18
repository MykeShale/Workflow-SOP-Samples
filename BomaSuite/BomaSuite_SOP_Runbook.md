# Standard Operating Procedure (SOP): Maintenance Request Workflow

**System**: BomaSuite
**Audience**: Landlords, Managers, Caretakers & Technical Staff
**Last Updated**: 2026

## Purpose
To outline the standard procedures for receiving, triaging, and resolving tenant maintenance requests using the BomaSuite ticketing system.

## 1. Request Initiation & Triage
Tenants submit maintenance requests exclusively through the BomaSuite Tenant Portal.
* **Notification**: Staff with the `manager` or `caretaker` role receive an automated notification when a new ticket is submitted.
* **Triage**:
  1. Log into the BomaSuite Dashboard and navigate to **Maintenance** -> **Active Tickets**.
  2. Review the ticket details, including photos uploaded by the tenant.
  3. Determine the severity level (Emergency, High, Normal, Low).
  4. *Note: Tickets flagged by the system containing keywords like "flood", "fire", or "gas" are automatically escalated to Emergency status and page the `technical` staff.*

## 2. Vendor / Technical Staff Assignment
1. Open the ticket and click **Assign Staff/Vendor**.
2. Select the appropriate internal technical staff or external vendor.
3. The system automatically emails the assignee a work order containing the issue details, tenant contact info (with PII rules applied), and entry permissions.

## 3. Work Order Tracking
* **Status Updates**: Assignees are required to update the status (e.g., "Scheduled", "In Progress", "Completed") in their dashboard.
* **Tenant Visibility**: Status changes automatically update the tenant's view in their portal, reducing inbound "status update" phone calls. All state changes are tracked in the BomaSuite `audit_log`.

## 4. Completion and Invoicing
1. Once marked as "Completed", the ticket moves to the **Pending Review** queue.
2. Manager reviews vendor notes and final invoice amount.
3. Click **Close Ticket**.
4. The system automatically routes any required invoice line items to the next billing cycle.
