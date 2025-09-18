Automated Network Request Workflow in ServiceNow

This project delivers a fully automated process in ServiceNow to manage network-related service requests. It uses ServiceNow’s Service Catalog, Flow Designer, custom tables, and approval framework to simplify request submission, routing, and tracking.

📌 Introduction

Network-related requests (e.g., device provisioning, connectivity issues, or access to network resources) are common in organizations. Earlier, such requests were handled manually, often resulting in delays, miscommunication, and lack of visibility.

To solve this, the project introduces a self-service network request catalog item backed by automation to ensure:

Quick request intake.

Seamless routing and approval.

Automatic notifications.

Centralized visibility of request status.

🎯 Goals

Build a simple and intuitive Service Catalog form for network-related requests.

Automate backend processes including record creation, assignment, approvals, and notifications.

Minimize manual intervention and speed up resolution.

Maintain a transparent audit trail for compliance and tracking.

⚡ Highlights
1. Service Catalog Item

Created a catalog entry “Network Request.”

Used variable sets to capture key details:

Requester Profile → Name, Department, Email.

Network Requirements → Location, Device type, Purpose/Justification, Priority.

2. Dynamic UI Policies

Applied conditions to make forms responsive:

Extra description field becomes visible only if Device Type = Others.

Certain fields are auto-mandatory based on user choices.

3. Custom Table

Built u_network_database_table to store all submissions.

Important fields include:

Customer Address, Request Number, Requested For, Assignment Group, Status, Device Info, Updates Count, Assigned To, Enquiry Date, Customer Document.

4. Relationship with Approvals

Integrated the custom table with the sysapproval_approver table.

Added a related list on the form so approvals for each request are visible in one place.

5. Flow Designer Orchestration

Configured a flow to automate the entire lifecycle:

Capture Variables → Extract data from catalog submission.

Create Record → Store details in the custom table.

Notifications → Email sent automatically to requester & approver.

Approval Step → Ask for approval with Approve/Reject options.

Conditional Updates → Status field updated dynamically based on outcome.

✅ Outcome

With this solution:

Request submission is standardized and user-friendly.

Approvals and notifications happen without manual effort.

All network requests are stored in a single source of truth.

Employees and managers have real-time visibility into request status.
