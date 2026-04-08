# 🏥 Clinic Management System – ER Diagram

## 📖 Overview

This repository contains the **Entity-Relationship Diagram (ERD)** for a modern clinic management system.

The design focuses on handling:

* Patient records
* Doctor & specialty management
* Appointment scheduling
* Consultations (visits)
* Diagnostic tests & reports
* Payment tracking

The goal is to create a **simple, scalable, and real-world clinic database design**.

---

## 🔄 Workflow

```
Patient → Appointment → Consultation → Tests → Reports → Payment
```

* Patients book appointments with doctors
* Appointments may result in consultations (visits)
* Doctors prescribe diagnostic tests during consultation
* Reports are generated after tests
* Payments are linked to consultations

---

## 🧱 Entities

* **Patients** – Stores patient information
* **Doctors** – Stores doctor details
* **Specialties** – Defines doctor domains
* **Appointments** – Booking system
* **Consultations** – Actual visits
* **Tests** – Diagnostic tests
* **Consultation_Tests** – Links tests to consultations
* **Reports** – Stores test results
* **Payments** – Billing information

---

## 🔗 Relationships

* One patient → many appointments
* One doctor → many appointments
* One appointment → zero or one consultation
* One consultation → many tests
* One test → many consultations (via junction table)
* One consultation test → one report
* One patient → many payments

---

## 🗝️ Key Design Decisions

* **Appointments and consultations are separate**

  * Not every appointment results in a visit

* **Consultation-based system**

  * All medical actions happen during consultation

* **Many-to-many test handling**

  * Implemented using `consultation_tests`

* **Reports linked to test instances**

  * Ensures accurate tracking

* **Payments linked to consultations**

  * Removes ambiguity in billing

---
## 🧩 Whiteboard / ER Diagram Link

You can also view the ER Diagram on the whiteboard:

🔗 **Whiteboard Link:**
[Open Diagram](https://app.eraser.io/workspace/ymdG9v7XCNUNR81tF8HB)

> If the link does not open, please check the README.md(main repo. file) or use the alternative diagram link provided there.
---

## 📊 ER Diagram

![ER Diagram](https://github.com/akshpatel-dev/Database-designs/blob/main/PR-3_Clinic_Appointment_and%20Diagnostics_Platform/Clinic%20Appointment%20and%20Diagnostics%20Platform%20ER_diagram.png)


---

## ⚙️ Tech Stack

* ER Modeling Tool: **Eraser / dbdiagram / any ER tool**
* Format: **Relational Database Design**

---

## ✅ Features Supported

* Multiple visits per patient
* Multiple patients per doctor
* Multiple tests per consultation
* Delayed report generation
* Clean and flexible billing system

---

## 🚀 Future Improvements

* Add prescription entity
* Add user authentication system
* Add clinic branches / multi-location support
* Add inventory for lab tests

---

## ⭐ If you like this project

Give it a star ⭐ and feel free to fork!
