# 🏢 Smart Elevator Control System – ER Diagram

## 📖 Overview

This project represents the **ER Diagram for a multi-building smart elevator control system** developed for large commercial infrastructures such as malls, airports, corporate towers, and residential complexes.

The system is designed to manage:

* Multiple buildings and floors
* Elevator operations across shafts
* Floor-level request handling
* Ride assignments and logs
* Elevator status monitoring
* Maintenance tracking


---

## 📷 ER Diagram

[ER Diagram](https://app.eraser.io/workspace/ymdG9v7XCNUNR81tF8HB)

this is the link of Eraser.io

---

## 🔄 System Workflow

```
User Request → Floor Request → Ride Assignment → Elevator Movement → Ride Log → Status Tracking
```

* Users generate requests from floors
* Requests are assigned to elevators
* Elevators execute rides across floors
* Ride details are stored for analytics
* Status and maintenance logs are tracked separately

---

## 🧱 Entities

* **Buildings** – Stores building information
* **Floors** – Represents floors within buildings
* **Shafts** – Physical elevator shafts
* **Elevators** – Elevator units assigned to shafts
* **Elevator_Floor_Map** – Maps elevators to multiple floors (M:N)
* **Floor_Requests** – User-generated requests from floors
* **Ride_Assignments** – Assigns requests to elevators
* **Ride_Logs** – Records completed rides
* **Elevator_Status_Logs** – Tracks dynamic elevator states
* **Maintenance_Logs** – Tracks maintenance history

---

## 🔗 Relationships

* One building → many floors
* One building → many elevators
* One shaft → one elevator
* One elevator → many floors (via mapping table)
* One floor → many requests
* One request → one assignment
* One elevator → many ride logs
* One elevator → many status logs
* One elevator → many maintenance records

---

## 🗝️ Key Design Decisions

* **Separation of static and dynamic data**

  * Elevator configuration is separate from ride and status logs

* **Many-to-many mapping (Elevator ↔ Floors)**

  * Allows flexible elevator coverage

* **Request → Assignment → Ride flow**

  * Ensures proper tracking of request lifecycle

* **Status tracking as logs (not attributes)**

  * Maintains history instead of overwriting

* **Maintenance tracking independent of elevator**

  * Preserves operational history

---

## 📊 Features Supported

* Multi-building elevator management
* Multiple elevators per building
* Multiple floors per building
* Floor request tracking
* Smart elevator assignment
* Ride history logging
* Elevator usage analytics
* Maintenance tracking and downtime management
* Real-time elevator status tracking

---

## ⚙️ Tech Stack

* ER Modeling Tool: **Eraser / dbdiagram**
* Design Type: **Relational Database Design**

---

## 🚀 Future Improvements

* Add user/passenger tracking
* Add priority request handling (VIP/emergency)
* Add AI-based elevator optimization
* Add real-time monitoring dashboard

---


If you found this useful, consider giving it a ⭐ on GitHub!
