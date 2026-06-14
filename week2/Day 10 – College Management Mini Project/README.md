# Day 10 – College Management Mini Project

## System Overview

The College Management Mini Project is a Salesforce-based enterprise application designed to manage students, faculty, courses, and departments. The system integrates CRM concepts, automation, Apex programming, SOQL queries, triggers, validation rules, and Lightning Web Components (LWC) into one connected application.

The application allows students to register for courses, faculty to monitor attendance and course capacity, and administrators to manage departments and academic operations efficiently.

---

# CRM Concepts

## Main Objects

### Student

Stores student information.

Fields:

* Student Name
* Student ID
* Email
* Phone Number
* Attendance Percentage
* Department

### Faculty

Stores faculty details.

Fields:

* Faculty Name
* Email
* Subject Specialization
* Department

### Course

Stores course information.

Fields:

* Course Name
* Course Code
* Total Seats
* Filled Seats
* Remaining Seats
* Faculty Assigned

### Department

Stores department details.

Fields:

* Department Name
* Department Code
* Head of Department

---

# Data Model

## Relationships

* One Department can have many Students.
* One Department can have many Faculty members.
* One Faculty can teach many Courses.
* One Student can register for many Courses.
* One Course can contain many Students.

## Relationship Types

* Lookup Relationship
* Master-Detail Relationship

---

# Validation Rules

## Student Email Validation

* Email field must not be blank.

## Course Seat Validation

* Filled seats cannot exceed total seats.

## Attendance Validation

* Attendance percentage cannot be below 0 or above 100.

## Course Registration Validation

* Students cannot register for the same course multiple times.

---

# Formula Fields

## Remaining Seats

Formula:
Filled Seats - Total Seats

## Attendance Percentage

Formula based on:
Classes Attended / Total Classes

---

# Flows

## Course Registration Flow

* Triggered when student registers.
* Updates filled seats automatically.
* Sends confirmation email.

## Attendance Warning Flow

* Triggered when attendance falls below required percentage.
* Sends warning notification to student.

## Faculty Notification Flow

* Sends notification when course reaches full capacity.

---

# Apex Logic

## Eligibility Calculation

Apex class checks:

* Attendance percentage
* Course prerequisites
* Seat availability

## Bulk Operations

Apex handles:

* Bulk student registration
* Bulk attendance updates
* Bulk notifications

## SOQL Usage

SOQL queries are used to:

* Fetch registered students
* Retrieve faculty course assignments
* Display dashboard data

---

# Trigger Logic

## Course Full Trigger

When course seats become full:

* Trigger sends notification to faculty.

## Low Attendance Trigger

When attendance falls below minimum limit:

* Trigger generates alert record.

---

# LWC UI Screens

## Student Dashboard

Features:

* View registered courses
* Check attendance
* Receive notifications

## Faculty Dashboard

Features:

* View assigned courses
* Monitor student attendance
* Manage course capacity

## Registration Screen

Features:

* Course selection
* Seat availability display
* Registration confirmation

---

# Complete Data Flow

Student clicks Register →

LWC Registration Screen →

Validation Rules check data →

Flow automation starts →

Apex logic processes registration →

Trigger executes after record update →

Database stores records →

Notification email sent to student and faculty

---

# Architecture Thinking

Enterprise systems require:

## Frontend

Provides user interaction through dashboards and forms.

## Backend

Processes business logic and handles operations securely.

## Database

Stores and manages large amounts of structured data.

## Automation

Reduces manual work using flows and scheduled processes.

## Events and Triggers

Enable real-time system reactions and notifications.

All components work together to create scalable and efficient enterprise applications.

---

# Scaling Thinking

If 50,000 students use the system simultaneously, possible issues include:

## Performance Problems

* Slow dashboard loading
* Delayed queries

## Data Consistency Issues

* Duplicate registrations
* Conflicting updates

## Notification Problems

* Email delivery delays
* Event queue overload

## Security Risks

* Unauthorized data access
* Large-scale permission management

## Scalability Challenges

* Database optimization
* Governor limits
* Bulk data handling

---

# Reflection

After learning Salesforce, I realized that enterprise software systems are built using multiple connected layers rather than a single program.

Frontend interfaces, backend logic, databases, automation tools, triggers, and security models must work together carefully. Salesforce demonstrates how modular architecture improves scalability, maintainability, and reusability in real-world applications.

I also understood the importance of automation, event-driven systems, validation, and reusable UI components in enterprise application development.

---

