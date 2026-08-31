# ticket-booking-management
Movie Ticket Booking Management application built on Pega Platform for CineWave Entertainment.
# 🎬 Movie Ticket Booking Management

A **Pega-based Movie Ticket Booking Management application** developed for **CineWave Entertainment** to automate movie ticket booking requests, show availability, cost calculation, customer confirmation, booking processing, SLA monitoring, routing, and customer notifications.

---

## 📌 Overview

The Movie Ticket Booking Management Application provides a structured digital workflow for managing movie ticket booking requests.

The application replaces manual booking and communication processes with an automated Pega case management solution that allows booking requests to be processed efficiently from initiation to completion.

---

## 🎯 Project Objectives

The main objectives of this application are:

* Allow customers to submit movie ticket booking requests.
* Capture customer and booking information.
* Check movie show availability.
* Calculate the total booking cost.
* Obtain customer confirmation before processing.
* Process confirmed ticket bookings.
* Notify customers about booking status.
* Track booking cases throughout their lifecycle.
* Apply SLA monitoring to booking requests.
* Route priority bookings based on business rules.

---

## 🛠️ Technology

* **Pega Platform**
* **Pega App Studio**
* **Pega Blueprint**
* **Case Management**
* **Data Modeling**
* **Business Process Automation**
* **Workflow Design**
* **SLA Configuration**
* **Business Rules**

---

## 🔄 Case Lifecycle

The movie ticket booking case follows the following lifecycle:

```text
Customer Request
       ↓
Customer Confirmation
       ↓
Booking Processing
       ↓
Customer Notification
       ↓
Completion
```

### Case Stages

1. **Customer Confirmation**
   Captures and validates customer confirmation.

2. **Booking Processing**
   Processes the confirmed booking request and performs the required booking operations.

3. **Customer Notification**
   Sends the appropriate notification to the customer.

4. **Completion**
   Marks the booking case as completed after successful processing.

---

## ⭐ Key Features

* Movie ticket booking request management
* Customer information capture
* Show availability checking
* Booking cost calculation
* Customer confirmation
* Automated booking processing
* Customer notifications
* SLA monitoring
* Priority-based routing
* Manager Work Queue routing
* Booking status tracking
* Business rule-based automation

---

## 📊 Detailed Data Model

The application uses structured data entities to capture customer, booking, and show information.

| Data Type           | Field Name                             | Type                 | Description                                          |
| :------------------ | :------------------------------------- | :------------------- | :--------------------------------------------------- |
| **CustomerDetails** | `CustomerName`, `Email`, `Phone`       | Text / Email / Phone | Captures primary customer contact information        |
| **BookingDetails**  | `BookingID`, `SeatsCount`, `TotalCost` | Integer / Decimal    | Stores booking and transaction information           |
| **ShowDetails**     | `MovieName`, `ShowTime`, `TheatreName` | Text / Date-Time     | Tracks movie, theatre, and show schedule information |

### Data Relationships

The booking process connects the major data elements:

```text
CustomerDetails
      ↓
BookingDetails
      ↓
ShowDetails
      ↓
Movie Ticket Booking Case
```

This structured data model allows the application to maintain consistent booking information throughout the case lifecycle.

---

## 👤 User Stories Implemented

### US-001: Submit Movie Ticket Request

Captures customer details, target movie, and requested number of seats to create a movie ticket booking request.

### US-002: Check Show Availability

Validates the availability of seats for the requested movie and show time before proceeding with the booking.

### US-003: Calculate Booking Cost

Calculates the total ticket price based on the requested seats and applicable taxes and convenience fees.

---

## ⏱️ Service Level Agreements (SLA) & Routing Logic

The application uses SLA configuration to ensure booking requests are processed within the expected timeframe.

### SLA Configuration

| SLA Parameter | Configuration                                 |
| :------------ | :-------------------------------------------- |
| **Case Type** | Movie Ticket Booking                          |
| **Goal**      | 2 Hours                                       |
| **Deadline**  | 24 Hours                                      |
| **Purpose**   | Standard processing and escalation monitoring |

### SLA Behavior

* **Goal: 2 Hours** — The booking request is expected to reach the required processing milestone within 2 hours.
* **Deadline: 24 Hours** — If the booking remains unresolved beyond the configured deadline, it triggers escalation handling.

### Routing Logic

The application applies business rules to route booking requests based on priority.

```text
Booking Request
      ↓
Check Priority
      ↓
 ┌───────────────┬─────────────────┐
 ↓               ↓
VIP / High       Regular
Priority         Booking
 ↓               ↓
Manager Work     System Rules
Queue             ↓
 ↓             Auto-Processing
Manager Review
```

* **High-priority or VIP booking requests** are routed directly to the **Manager Work Queue**.
* **Regular booking requests** are handled through the configured system rules and automated processing.
* SLA monitoring ensures that pending requests can be identified and escalated when required.

---

## ⚙️ Business Rules

The application implements business rules to automate the booking process.

* Validate customer information.
* Validate movie and show details.
* Check show availability.
* Validate requested seat count.
* Calculate ticket cost.
* Include applicable taxes and convenience fees.
* Obtain customer confirmation before final processing.
* Route VIP/high-priority requests to the Manager Work Queue.
* Auto-process regular booking requests according to system rules.
* Trigger escalation when the SLA deadline is exceeded.
* Send customer notifications after booking processing.
* Update the booking case status throughout the lifecycle.

---

## 🤖 Process Automation

The Pega workflow automates the complete movie ticket booking journey.

### Automated Flow

**Request → Validation → Availability Check → Cost Calculation → Customer Confirmation → Booking Processing → Notification → Completion**

This automation reduces manual effort, improves process visibility, and provides a consistent booking experience.

---

## 🔔 Customer Notification

The application provides customer notifications as part of the booking workflow.

Notifications can be used to communicate important booking updates such as:

* Booking confirmation
* Booking processing status
* Successful completion
* Relevant case updates

---

## 🧩 Pega Capabilities Demonstrated

This project demonstrates practical implementation of:

* Pega App Studio
* Pega Blueprint
* Case Types
* Case Lifecycle
* Stages and Steps
* Data Modeling
* User Stories
* Business Rules
* Workflow Automation
* SLA Configuration
* Case Routing
* Work Queues
* Customer Notifications
* Business Process Automation

---

## 📋 Project Information

| Property             | Details                                |
| :------------------- | :------------------------------------- |
| **Application**      | Movie Ticket Booking Management        |
| **Organization**     | CineWave Entertainment                 |
| **Platform**         | Pega Platform                          |
| **Development Tool** | Pega App Studio                        |
| **Project Type**     | Individual Project                     |
| **Domain**           | Movie Ticket Booking / Case Management |

---

## 🎓 Skills Demonstrated

* Case Management
* Workflow Design
* Data Modeling
* Business Process Automation
* Business Rule Configuration
* SLA Management
* Case Routing
* Work Queue Management
* Customer Communication
* Pega App Studio
* Pega Blueprint

---

## 📈 Project Outcome

The Movie Ticket Booking Management application provides CineWave Entertainment with a structured and automated solution for handling movie ticket booking requests.

The solution integrates **data modeling, user stories, workflow automation, availability checking, cost calculation, customer confirmation, SLA monitoring, priority-based routing, booking processing, and customer notifications** into a single Pega case management workflow.

---

## 🚀 Project Status

**Completed**

The application has been developed and configured using **Pega App Studio and Pega Blueprint** according to the defined movie ticket booking requirements.

---

## 👨‍💻 Project Author

**Niranjan S**

**CSE – Individual Project**

---

## 📄 Repository

This repository contains the project resources and documentation for the **Movie Ticket Booking Management Application** developed for CineWave Entertainment.
