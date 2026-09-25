# ServiceNow Auto Ticket Classification

## 📌 Project Overview

This project automates the classification of newly created Incident tickets in ServiceNow using Flow Designer.

The flow analyzes the **Short Description** of an incident and automatically assigns an appropriate **Category**.

## 🎯 Objective

To reduce manual ticket classification and automatically categorize incidents based on keywords in their short description.

## ⚙️ Technologies Used

- ServiceNow
- Workflow Studio / Flow Designer
- Incident Management
- Flow Logic
- Update Record Action

## 🔄 Workflow

Incident Created
        ↓
Read Short Description
        ↓
Check Ticket Type
        ↓
┌──────────────┬──────────────┬──────────────┐
│    Laptop    │     WiFi     │   Software   │
│      ↓       │      ↓       │       ↓      │
│   Hardware   │   Network    │   Software    │
└──────────────┴──────────────┴──────────────┘

## 🧠 Classification Rules

| Keyword | Category |
|---------|----------|
| laptop | Hardware |
| wifi | Network |
| software | Software |

## 🛠️ Flow Configuration

### Trigger
- Type: Record
- Event: Created
- Table: Incident [incident]

### Condition 1
- Short description contains `laptop`
- Category → Hardware

### Condition 2
- Short description contains `wifi`
- Category → Network

### Condition 3
- Short description contains `software`
- Category → Software

## 🧪 Testing

The flow was tested using newly created Incident records.

| Test Case | Input | Expected Result | Result |
|-----------|-------|-----------------|--------|
| 1 | Laptop is not working | Hardware | ✅ Passed |
| 2 | WiFi is not working | Network | ✅ Passed |
| 3 | Software is not working | Software | ✅ Passed |

## ✅ Project Status

Core automatic ticket classification has been successfully implemented and tested.

## 👨‍💻 Project Team
1. Shivam Singh(Captain)
2. Allwin Vincent Raj

## 📄 Project Type

ServiceNow Administrator Project
