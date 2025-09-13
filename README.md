# AI-Enabled Hospital & Pharmacy Management – Salesforce Healthcare System

## Project Overview
The **AI-Enabled Hospital & Pharmacy Management system** is a Salesforce-based solution designed to digitize and centralize hospital and clinic operations.
The goal is to streamline processes like appointment scheduling, medicine inventory management, billing, and patient history tracking, while providing real-time access to doctors, nurses, pharmacists, and administrators.

This system also leverages **AI-driven features** to:

Predict medicine stock requirements

Suggest alternatives for unavailable medicines

Track patient medicine usage & send refill reminders

Allow one-click auto-ordering of medicines when stock is about to run out

Optimize operational workflows

This ensures efficiency, proactive healthcare, and improved patient satisfaction.

---

## Phase 1: Problem Understanding & Industry Analysis

This phase focuses on analyzing current healthcare management challenges and laying the foundation for building an effective Salesforce solution.

### **Tasks in Phase 1**
1. Requirement Gathering  
2. Stakeholder Analysis  
3. Business Process Mapping  
4. Healthcare Use Case Research  
5. Review of Existing Solutions / AppExchange Exploration  

---

## 1️. Requirement Gathering

### **Problem Statement**
Currently, most hospitals and clinics rely on manual or disconnected processes:
1. Appointments scheduled via phone or manually on paper.
2. Medicine inventory tracked through spreadsheets, often leading to stockouts or expired medicines.
3. Billing is manual and error-prone, especially with insurance processing.
4. Patient reminders are inconsistent or nonexistent.
5. No system to proactively remind patients when their medicine stock is about to finish.
6. Administrators lack real-time dashboards for monitoring operations.

These issues lead to inefficiencies, delays, errors, and poor patient experience.

### **Solution**
A Salesforce-based centralized system to:  
-Manage **patients, doctors, nurses, and pharmacists profiles**.  
- Track **appointments, medicine inventory, and expiry**.  
- Automate **billing and insurance processing**.  
- Send **automatic reminders** to patients for appointments and medicine pickups.  
- Provide **dashboards and reports** for administrators.  
- Implement **role-based access** for different users.  
- Leverage **AI features** for:
    1. Predicting stock shortages.
    2. Suggesting alternative medicines.
    3. Calculating patient medicine consumption and sending refill notifications.
    4. Auto-placing refill orders when the patient clicks "Yes" on a reminder.

---

### **Functional Requirements**

| **Feature**                   | **Description** |
|--------------------------------|----------------|
| Patient Management             | Register and manage patient profiles, medical history, and prescriptions |
| Doctor Scheduling              | Doctors set availability and manage appointments |
| Appointment Booking            | Patients book appointments via Lightning Web Components (LWC) |
| Reminders                      | Automatic email/SMS reminders for appointments and medicine pickups |
| Medicine Inventory             | Add and track medicines, batch numbers, expiry dates, and stock levels |
| 🤖 AI-Powered Stock Prediction | Predicts medicine shortages and automatically creates purchase orders to prevent stockouts |
| 🔄 Alternative Medicine Suggestions | Suggests substitute medicines if the required stock is unavailable |
| 📲 AI Medicine Refill Reminder  | Tracks how much medicine a patient has, predicts when it will run out, sends reminders, and allows one-click refill ordering  |
| Billing & Insurance            | Calculate consultation + medicine cost and apply insurance policies |
| Dashboards & Reports           | Track visits, medicine usage, revenue, and cancellations |
| Security / Role Access         | Role-based permissions for Admin, Doctor, Nurse, Pharmacist, Patient |

---

### **Non-Functional Requirements**

| **Requirement**                | **Goal** |
|--------------------------------|----------|
| Scalability                     | Support multiple hospitals, doctors, and thousands of patients |
| Reliability & Availability      | Core features like appointment booking and reminders must be consistently operational |
| Security & Privacy              | Protect patient medical and billing data using Salesforce security features and role-based access |
| Performance                     | LWC pages and Apex processes should load quickly and execute efficiently |
| Usability / User Experience     | Intuitive interface, mobile-friendly design for easy access |
| Maintainability                 | Modular code and configurations for easy updates or extensions |
| Compliance                      | Adhere to healthcare regulations and data privacy standards (HIPAA or local equivalents) |

---

## 2️. Stakeholder Analysis

| **Stakeholder**        | **Role in System**                                   | **Access Level** |
|------------------------|-----------------------------------------------------|-----------------|
| Admin (Hospital Manager)| Oversees appointments, inventory, billing, reports | Full Access |
| Doctor                 | Manage schedule, view patients, approve urgent cases| Edit Access |
| Pharmacist             | Manage medicine inventory, handle stock alerts     | Edit Access |
| Nurse                  | Assist with patient check-in and updates           | Limited Edit Access |
| Patient                | Book appointments, view history & prescriptions, receive refill reminders    | Read/Write Own Data |

---

## 3️. Business Process Mapping

### **Current Manual Process**
1. Patients call or visit the hospital/clinic to book appointments.  
2. Medicine inventory is tracked manually; expired or low-stock medicines may be missed.  
3. Billing is done on paper, including consultation fees, pharmacy charges, and insurance claims.  
4. Appointment and medicine reminders are inconsistent or absent.  
5. Reports and analytics are compiled manually using spreadsheets.
6. Patients have to remember themselves to revisit the pharmacy when medicines run out.

### **Proposed Salesforce Process (AI-Enabled Hospital & Pharmacy Management)**

| **Action**                  | **Old Process**                    | **New Process (Salesforce)** |
|-------------------------------|-----------------------------------|------------------------------|
| Appointment Booking           | Phone calls or in-person visits   | Patients book via LWC; system prevents overlaps |
| Medicine Stock Monitoring     | Manual spreadsheets               | Real-time tracking; AI predicts low stock and sends alerts |
| Billing & Insurance           | Manual calculation and paperwork | Automated calculations via Salesforce; insurance rules applied |
| Reminders                     | Staff follow-ups                  | Automatic email/SMS reminders for appointments and medicine pickups |
| Reports / Analytics           | Monthly spreadsheet compilation   | Real-time dashboards for administrators and staff |
| Patient Access                | Delayed and indirect updates      | Real-time access through Salesforce portal or mobile app |
| Medicine Refill               | Patients manually revisit pharmacy | AI calculates usage, notifies patients, and allows one-click refill ordering |

---

## 4️. Industry-Specific Use Case Analysis

| **Platform / System**                | **Key Features**                                    | **Gap Identified** |
|-------------------------------------|---------------------------------------------------|------------------|
| Generic Hospital Management Systems  | Appointment scheduling, billing, basic inventory | Often not integrated end-to-end; limited predictive analytics |
| Pharmacy Inventory Software          | Stock tracking, batch and expiry management       | Lacks integration with appointments, billing, and patient history |
| Telemedicine Apps                     | Remote consultations, scheduling                  | Do not handle inventory, billing, or comprehensive patient data |
| Salesforce Health Cloud               | Patient management, analytics, appointments      | Too complex for smaller hospitals or clinics; expensive and broad |

**Why This Project Stands Out:**  
- Combines **appointments, inventory, billing, and patient history** in a single Salesforce platform.
- Includes AI-driven features: stock prediction, alternative medicine suggestions, and smart medicine refill reminders with auto-ordering.
- Lightweight, **user-friendly**, and specifically designed for **small to medium healthcare setups**.  
- Provides **real-time dashboards and automated reminders**, improving operational efficiency and patient experience.

---

## 5️. AppExchange Exploration

| **App Name**                     | **Key Features**                                | **Why Not Fully Suitable** |
|----------------------------------|-------------------------------------------------|----------------------------|
| Salesforce Health Cloud           | Patient management, appointments, analytics    | Too broad and complex for small hospitals or clinics; costly |
| MedTracker / Pharmacy Inventory Apps | Medicine stock tracking, batch & expiry management | Not integrated with appointment scheduling, billing, or patient history |
| Appointment Scheduling Apps       | Online booking and reminders                     | Lacks medicine inventory management and billing integration |
| Billing & Insurance Apps          | Automated billing and insurance processing      | Often standalone; no integration with patient history or inventory |

**Conclusion:**  
Existing AppExchange solutions either address only part of the problem or are too complex for smaller hospitals and clinics.
**AI-Enabled Hospital & Pharmacy Management** fills the gap by providing a **comprehensive, integrated Salesforce solution for appointments, inventory, billing, patient history, and AI-powered stock management + refill automation**.

---

## **Initial Scope**  
- Start with **one hospital or clinic** as a pilot.  
- Core modules: Patient Management, Doctor Scheduling, Appointment Booking, Medicine Inventory, Billing & Insurance, Reminders.  
- Roles included: Admin (Hospital Manager), Doctor, Nurse, Pharmacist, Patient.  
- AI features: 
    1. Stock prediction for critical items.
    2. Alternative medicine suggestions.
    3. Basic patient-level refill reminder and one-click reorder feature.
---

## **Future Scope / Enhancements**  
- Expand to **multiple hospitals and clinics** with centralized management.  
- Integrate **telemedicine** for remote consultations.  
- Implement **advanced AI features** for Demand forecasting and automated supplier-side stock replenishment when patients reorder..  
- Develop a **mobile app** for patients to book appointments, view prescriptions, and Get real-time medicine refill reminders & approve reorders instantly.  
- Integrate with **insurance portals** for real-time claim processing.  
- Add **analytics for hospital performance**, including revenue trends, patient satisfaction, and appointment efficiency.  
- Enable **multi-language support** for wider accessibility.

---

## Author
**Mitali Parthasarathi Anagolkar**  
B.Tech Computer Science Engineering  
📍 India  

<!-- Optional: add ERD diagrams or screenshots here -->
