# 🏋️‍♂️ Online Fitness Coaching Platform – ER Diagram

## 📌 Overview

This project represents the **database design (ER Diagram)** for an online fitness coaching ecosystem where trainers/influencers manage clients digitally.

Unlike traditional gym systems, this platform focuses on:

* Online coaching
* Subscription-based plans
* Progress tracking
* Consultations & live sessions

---

## 🎯 Problem Statement

A fitness influencer starts with manual coaching via DMs and video calls. As their brand grows, they need a scalable platform to:

* Onboard clients
* Sell fitness programs
* Manage subscriptions
* Schedule consultations
* Track progress (weight, measurements, reports)
* Maintain regular check-ins

---

## 🧩 Key Features Supported

* 👤 Trainer & Client management
* 📦 Multiple fitness plans/programs
* 🔁 Subscription lifecycle tracking
* 📅 Session & consultation scheduling
* 📊 Progress tracking via check-ins
* 💬 Trainer feedback & notes
* 💳 Payment handling

---

## 🗂️ Entities Included

### 👥 Users

* Stores both trainers and clients using role-based design

### 🧑‍🏫 Trainer Profile

* Additional info like specialization, experience

### 🧑 Client Profile

* Stores fitness-related attributes (goal, height, etc.)

### 📦 Plans

* Coaching programs created by trainers

### 🔁 Subscriptions

* Tracks which client purchased which plan
* Includes start/end dates and status

### 💳 Payments

* Stores transaction details for subscriptions

### 📅 Sessions

* Consultation or live training sessions

### 📊 Check-ins

* Weekly progress updates submitted by clients

### 📏 Measurements

* Body stats linked to check-ins

### 📝 Trainer Notes

* Feedback provided by trainers on check-ins

### 🏋️ Workout & 🥗 Diet Plans

* Structured plan content linked to main plans

---

## 🔗 Relationships

* One **trainer → many plans**
* One **client → many subscriptions**
* One **plan → many clients**
* One **subscription → many payments, sessions, check-ins**
* One **check-in → measurements + trainer notes**

---

## 🧠 Design Decisions

* ✅ Unified **Users table** for scalability
* ✅ **Subscriptions as core entity** for lifecycle tracking
* ✅ Separation of **sessions vs check-ins**
* ✅ Progress tracking normalized (not inside user)
* ✅ Flexible plan types (consultation / coaching / self-guided)

---

## 🚀 How to Use

1. Clone the repository
2. Open the ER diagram image
3. Use the schema for:

   * Database implementation
   * Backend system design
   * Learning DBMS concepts

---

## 📌 Future Improvements

* Add messaging/chat system
* Add workout/diet detailed structures
* Add notifications & reminders
* Add analytics dashboard

---

## ⭐ If you found this helpful

Give it a star ⭐ and feel free to fork!
