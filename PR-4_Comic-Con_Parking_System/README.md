# 🚗 Comic-Con Parking System – ER Diagram

## 📖 Overview

This project represents the **ER Diagram for a multi-zone event parking system** (Comic-Con India venue).

The system is designed to manage:

* Vehicle entry and exit
* Parking spot allocation across zones and levels
* Reserved parking categories (VIP, staff, exhibitors, EV, etc.)
* Parking sessions and tickets
* Payment tracking and pricing

---

## 🔄 System Workflow

```
Vehicle → Parking Session → Spot Allocation → Exit → Payment → Ticket
```

* Vehicles enter the venue and are assigned a parking spot
* A **parking session** is created with entry time
* A **ticket** is issued for the session
* On exit, exit time is recorded
* Parking fee is calculated and stored in **payments**

---

## 🧱 Entities

* **Vehicles** – Stores vehicle details
* **Vehicle Categories** – Defines types (bike, car, SUV, EV, etc.)
* **Parking Zones** – Represents zones and levels
* **Parking Spots** – Individual parking slots
* **Spot Categories** – Reserved types (VIP, staff, EV, etc.)
* **Parking Sessions** – Tracks entry and exit of vehicles
* **Tickets** – Issued for each parking session
* **Payments** – Records parking charges and payment status
* **Pricing Rules** – Defines cost per vehicle category

---

## 🔗 Relationships

* One vehicle → many parking sessions
* One parking spot → many sessions over time (reuse supported)
* One zone → many parking spots
* One vehicle category → many vehicles and spots
* One session → one ticket
* One session → one payment
* One vehicle category → pricing rules

---

## 🗝️ Key Design Decisions

* **Parking sessions are separate from tickets**

  * Allows flexible tracking of entry/exit

* **Spot availability is NOT stored**

  * Derived from active sessions (real-time accurate)

* **Reserved parking handled via spot categories**

  * Supports VIP, staff, exhibitors, EV charging

* **Pricing handled separately**

  * Allows dynamic pricing per vehicle type

* **Spot reuse supported**

  * One spot can serve multiple vehicles over time

---

## 📊 Features Supported

* Multiple visits per vehicle across event days
* Multi-zone and multi-level parking
* Reserved parking categories
* Real-time parking availability tracking
* Ticket-based entry system
* Payment tracking per session
* Dynamic pricing

---

## ⚙️ Tech Stack

* ER Modeling Tool: **Eraser / dbdiagram**
* Design Type: **Relational Database Design**

---

## 🚀 Future Improvements

* Add EV charging session tracking
* Add booking/reservation system for VIP parking
* Add dynamic surge pricing
* Add entry gate / exit gate tracking

---


## ⭐ Support

If you found this useful, consider giving it a ⭐ on GitHub!
