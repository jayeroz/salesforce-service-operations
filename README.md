# Service Operations Management System (Salesforce Project)

## Overview
I built a Salesforce-based Service Operations Management system to simulate how a company tracks service requests, assigns technicians, and monitors workload. The goal was to improve visibility, reduce manual work, and ensure accurate technician assignment.

---

## Business Scenario
Manual assignment of service requests lead to delays, uneven workload distribution, and incorrect technician assignments. There was also a risk of assigning technicians who are unavailable or lack the required skill set.

---

## Solution
I designed and implemented a custom Salesforce solution that automates technician assignment, enforces basic business logic, and provides reporting for operational visibility.

---

## System Design

### Custom Objects
- Service Request
- Technician

### Key Features
- Auto-generated Request ID
- Technician assignment via lookup relationship
- SLA tracking
- Status and Priority tracking

---

## Automation

### Auto Assign Technician (Flow)
A record-triggered flow automatically assigns an available technician when a new service request is created. This reduces manual effort and improves response time.

---

## Reports Created
- Service Requests by Status
- Requests by Technician
- Requests by Priority

---

## Dashboard

### Service Operations Overview
The dashboard provides a high-level view of:
- Request status distribution
- Technician workload
- Request priority breakdown

---

## Screenshots

### Service Request Object
Defines the central object used to track incoming service requests. This object captures key operational data such as request type, priority, SLA hours, and assigned technician, forming the foundation of the service management process.

![Service Request Object](assets/01_Service_Request_Object.png)

---

### Fields Configuration
Shows the structured fields used to manage and standardize service requests. Fields such as Status, Priority, Request Type, SLA Hours, and timestamps ensure consistent tracking, reporting, and performance measurement.

![Fields](assets/02_Service_Request_Fields.png)

---

### Technician Object
Represents service technicians, including their skill type and availability status. This object supports intelligent assignment logic by ensuring only qualified and available technicians are selected.

![Technician Object](assets/03_Technician_Object.png)

---

### Open Requests List View
Displays all active service requests that are not yet completed. This view helps prioritize daily workload and provides visibility into pending tasks requiring action.

![Open Requests](assets/05_List_View_Open_Requests.png)

---

### High Priority List View
Filters and highlights urgent service requests based on priority level. This ensures critical issues are addressed quickly and supports operational efficiency.

![High Priority](assets/06_List_View_High_Priority.png)

---

### Automation Flow (Auto-Assign Technician)
Demonstrates a record-triggered flow that automatically assigns an available technician based on predefined criteria. This reduces manual effort, improves response time, and ensures consistent assignment logic.

![Flow](assets/07_Flow_Auto_Assign.png)

---

### Service Operations Dashboard
Provides a high-level view of service request workload, distribution, and technician assignments. The dashboard enables quick insights into operational performance and supports data-driven decision-making.

![Dashboard](assets/08_Service_Dashboard.png)
---

## Enhancements Implemented

A validation rule was implemented to enforce proper technician assignment. The rule prevents users from assigning technicians who are either unavailable or do not match the required skill type of the service request. This enhancement ensures data integrity, enforces real-world business constraints, and reduces the risk of incorrect assignments.
This validation rule works alongside the automated assignment flow to ensure both automation and manual actions follow the same business rules.

---

## Skills Demonstrated
- Salesforce Data Modeling
- Process Automation (Flows)
- Reporting & Dashboards
- Business Logic Implementation
- System Design Thinking
