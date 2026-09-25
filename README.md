# 🎫 Auto Ticket Classification using ServiceNow Flow Designer

## 📌 Project Overview

The **Auto Ticket Classification** project is a ServiceNow automation solution designed to automatically classify newly created IT incident tickets based on keywords in the ticket's short description.

In a typical IT helpdesk environment, support staff manually review incoming incidents, identify the issue type, and assign the appropriate category. This process can be time-consuming and may result in inconsistent classification.

This project uses **ServiceNow Flow Designer** to automate the classification process and reduce manual effort.

---

## 🎯 Problem Statement

An IT helpdesk receives multiple incident requests every day, such as:

- Hardware problems
- Network connectivity issues
- Software-related problems
- Laptop-related issues

Manually reviewing and categorizing each incident can be inefficient.

The objective of this project is to create an automated workflow that analyzes newly created incidents and assigns an appropriate category based on predefined keywords.

---

## 💡 Solution

A ServiceNow **Flow Designer** flow is created with the following process:

1. A new Incident record is created.
2. The Flow Designer is automatically triggered.
3. The flow checks the **Short Description** of the incident.
4. Keywords are evaluated using conditional logic.
5. The appropriate Incident Category is automatically assigned.
6. The classification is stored in the Incident record.

### Example

| Keyword / Issue | Automatically Assigned Category |
|---|---|
| Laptop | Hardware |
| Network | Network |
| Software | Software |

---

## 🛠️ Technologies Used

- **ServiceNow**
- **ServiceNow Personal Developer Instance (PDI)**
- **Flow Designer**
- **Incident Management**
- **Conditional Logic (If / Else If)**
- **ServiceNow Update Record Action**
- **GitHub**

---

## ⚙️ Flow Design

The flow is triggered whenever a new Incident is created.

### Flow Logic

```text
New Incident Created
        ↓
Check Short Description
        ↓
 ┌──────────────────────────────┐
 │ Contains "Laptop"?           │
 └──────────────────────────────┘
        ↓ Yes
 Category → Hardware

        ↓ No
 ┌──────────────────────────────┐
 │ Contains "Network"?          │
 └──────────────────────────────┘
        ↓ Yes
 Category → Network

        ↓ No
 ┌──────────────────────────────┐
 │ Contains "Software"?         │
 └──────────────────────────────┘
        ↓ Yes
 Category → Software


🔄 Flow Implementation

The Flow Designer consists of:

Trigger

Record Created

Table:

Incident [incident]
Conditions

The flow checks the Incident Short Description for specific keywords.

Examples:

Short Description contains "laptop"
        ↓
Category = Hardware
Short Description contains "network"
        ↓
Category = Network
Short Description contains "software"
        ↓
Category = Software
Action

The Update Record action is used to update the Incident's Category field.

🧪 Testing

The flow was tested using multiple Incident records.

Test Case 1 — Hardware Ticket

A laptop-related incident was created.

Input:

Short Description: Laptop is not working

Expected Result:

Category: Hardware

Result: ✅ Passed

Test Case 2 — Network Ticket

A network-related incident was created.

Input:

Short Description: Network connection problem

Expected Result:

Category: Network

Result: ✅ Passed

Test Case 3 — Software Ticket

A software-related incident was created.

Input:

Short Description: Software installation issue

Expected Result:

Category: Software

Result: ✅ Passed

📸 Project Screenshots
Flow Designer

The following screenshot shows the configured ServiceNow Flow Designer workflow.

Hardware Classification

Network Classification

Software Classification

📊 Test Results
Test Case	Input Type	Expected Category	Result
Test Case 1	Laptop Issue	Hardware	✅ Passed
Test Case 2	Network Issue	Network	✅ Passed
Test Case 3	Software Issue	Software	✅ Passed

All implemented test scenarios successfully produced the expected category.

🔐 Project Scope

This project demonstrates automated ticket classification using ServiceNow Flow Designer.

The current implementation focuses on keyword-based classification using the Incident Short Description.

The project can be extended to support more advanced classification rules and additional incident categories.

🚀 Future Enhancements

Possible future improvements include:

Add more ticket categories and keywords.
Implement Subcategory classification.
Use both Short Description and Description fields.
Automatically assign incidents to appropriate support groups.
Add automated email notifications.
Add priority assignment based on ticket keywords.
Implement more advanced classification using ServiceNow Predictive Intelligence.
Add additional test scenarios.
Improve classification accuracy using more detailed rules.
📚 What I Learned

Through this project, I gained practical experience with:

ServiceNow Personal Developer Instance
Incident Management
Flow Designer
Record-based triggers
Conditional logic
Update Record actions
Automated ticket classification
Testing and validation of ServiceNow workflows
GitHub project documentation
👥 Team

Project: Auto Ticket Classification using Flow Designer

Team Members
Shivam Singh — Team Lead
Allwin Vincent Raj Tj — Member
Vikram Singh Gahlot — Member
Chandan Kumar Singh — Member
🏁 Conclusion

The Auto Ticket Classification using Flow Designer project demonstrates how ServiceNow automation can be used to reduce manual effort in IT helpdesk operations.

By automatically analyzing newly created incident descriptions and assigning appropriate categories, the workflow provides a simple and practical approach to improving ticket classification.

The project was implemented and tested in a ServiceNow Personal Developer Instance (PDI) using Flow Designer.

🔗 Project Links

GitHub Repository:
https://github.com/codershivaa/Auto-Ticket-Classification--Servicenow/

ServiceNow:
The working implementation is hosted in a ServiceNow Personal Developer Instance (PDI).

⚠️ ServiceNow instance credentials and private access details are not included in this repository.

⭐ Project Status: Completed and Tested
