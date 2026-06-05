# Visitor Access Management System | ServiceNow

![ServiceNow](https://img.shields.io/badge/Platform-ServiceNow-green)
![App Engine Studio](https://img.shields.io/badge/Built%20With-App%20Engine%20Studio-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)

## Overview

The Visitor Access Management System is a custom ServiceNow application developed using App Engine Studio to streamline visitor registration, approval, check-in, and check-out processes.

The application automates visitor lifecycle management through workflow-driven approvals, audit logging, email notifications, reporting, and dashboard analytics.

---

## Business Problem

Organizations often rely on manual visitor management processes, making it difficult to:

* Track visitor entries and exits
* Maintain audit trails
* Notify stakeholders about approvals
* Monitor visitor activity
* Generate operational reports

This application digitizes the complete visitor management process.

---

## Key Features

### Visitor Request Management

* Visitor Registration
* Host Employee Assignment
* Visit Scheduling
* Status Tracking

### Approval Workflow

* Approve Visitor Requests
* Reject Visitor Requests
* Automatic Approver Tracking

### Visitor Tracking

* Check-In Management
* Check-Out Management
* Timestamp Recording

### Audit Logging

* Approval Logs
* Check-In Logs
* Check-Out Logs
* User Activity Tracking

### Email Notifications

* Automated Approval Notifications
* Dynamic Email Templates

### Reporting & Analytics

* Visitor Status Distribution
* Approved Visitors Report
* KPI Metrics

### Dashboard Monitoring

* KPI Cards
* Status Distribution Chart
* Recent Visitor Requests

---

## Application Workflow

```text
Submitted
    │
    ▼
Approved ─────► Rejected
    │
    ▼
Checked In
    │
    ▼
Checked Out
```

---

## Data Model

### Visitor Request Table

| Field           | Description                   |
| --------------- | ----------------------------- |
| Number          | Auto-generated request number |
| Visitor Name    | Visitor name                  |
| Visitor Email   | Visitor email                 |
| Visitor Company | Company name                  |
| Host Employee   | Employee being visited        |
| Visit Date      | Scheduled visit date          |
| State           | Current request status        |
| Approved By     | Approver reference            |
| Checked-In Time | Check-in timestamp            |

### Visitor Log Table

| Field           | Description                     |
| --------------- | ------------------------------- |
| Visitor Request | Related visitor request         |
| Action          | Approved / Check-In / Check-Out |
| Notes           | Action description              |
| Performed By    | User performing action          |
| Timestamp       | Activity timestamp              |

---

## Business Rules Implemented

### Create Visitor Log

Automatically creates visitor activity records when:

* Request Approved
* Visitor Checked In
* Visitor Checked Out

### Auto Populate Approver

Automatically stores the approver information when a request is approved.

### Check-In Time Capture

Automatically records visitor check-in timestamps.

---

## Custom UI Actions

| UI Action | Function                     |
| --------- | ---------------------------- |
| Approve   | Approves request             |
| Reject    | Rejects request              |
| Check In  | Marks visitor as checked in  |
| Check Out | Marks visitor as checked out |

---

## Notifications

### Visitor Request Approved

**Trigger Condition**

```text
State changes to Approved
```

**Notification Details**

* Visitor Name
* Request Number
* Visit Date
* Host Employee
* Current Status

---

## Reports

### Visitor Status Distribution

Pie chart showing:

* Submitted
* Approved
* Rejected
* Checked In
* Checked Out

### Approved Visitors Report

Displays all approved visitor requests.

### Visitor Activity Report

Displays visitor lifecycle activity.

---

## Dashboard

### Visitor Access Dashboard

#### KPI Cards

* Total Visitor Requests
* Approved Requests
* Checked-In Requests

#### Visualizations

* Visitor Status Distribution Chart

#### Lists

* Recent Visitor Requests

---

## Technologies Used

* ServiceNow
* App Engine Studio
* Business Rules
* UI Actions
* Notifications
* Reports
* Dashboards
* Platform Analytics
* Access Control Roles (ACLs)

---

## Testing Scenarios

Successfully tested:

* Visitor Request Creation
* Approval Workflow
* Rejection Workflow
* Check-In Process
* Check-Out Process
* Email Notifications
* Visitor Log Creation
* Dashboard Updates
* Report Generation

---

## Screenshots

### Application Overview

![Application Overview](screenshots/01-app-engine-overview.png)

### Visitor Request Form

![Visitor Request Form](screenshots/03-visitor-request-form.png)

### UI Action Buttons

![UI Actions](screenshots/04-ui-actions-buttons.png)

### Visitor Logs

![Visitor Logs](screenshots/06-visitor-log-table.png)

### Email Notifications

![Notifications](screenshots/07-email-notification.png)

### Dashboard

![Dashboard](screenshots/11-dashboard-overview.png)

---

## Project Outcome

The Visitor Access Management System successfully automates visitor handling operations through workflow automation, audit logging, reporting, dashboards, notifications, and role-based access controls.

The project demonstrates practical ServiceNow application development skills including:

* Data Modeling
* Business Rules
* Workflow Automation
* Reporting & Analytics
* Dashboard Development
* User Experience Customization

---

## Author

**Anirudh Mamilla**

ServiceNow Certified System Administrator (CSA) | ServiceNow Certified Application Developer (CAD) | AI & ML Enthusiast | Full Stack Developer

### Connect With Me

* GitHub: https://github.com/Perkywarcheif
* LinkedIn: https://www.linkedin.com/in/m-anirudh-898a68257/

### Certifications

* ServiceNow Certified System Administrator (CSA)
* ServiceNow Certified Application Developer (CAD)
* Salesforce Certified AI Associate
* AWS Certified AI Practitioner
* AWS Certified Cloud Practitioner
