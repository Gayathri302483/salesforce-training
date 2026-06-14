# Salesforce Summer Program – Day 5

## Introduction

Today I learned why Salesforce uses Apex programming along with Flows and other no-code tools. I understood that declarative tools are useful for standard automation, but some business requirements need custom programming and advanced logic.

---

# 1. What is Apex?

Apex is the programming language used in Salesforce to build custom business functionality. It is mainly used when business requirements become too complex for normal configuration or Flow automation.

Using Apex, developers can:
- Create advanced automation
- Write custom business rules
- Perform database operations
- Connect Salesforce with external systems
- Process large amounts of records

Apex runs directly on the Salesforce platform and works similarly to Java.

---

# 2. Difference Between Flow and Apex

| Flow | Apex |
|---|---|
| Built using drag-and-drop | Written using code |
| Best for simple automation | Best for complex logic |
| Easier for admins | Requires programming knowledge |
| Faster to create | More flexible |
| Limited customization | Advanced customization possible |

---

# 3. Difference Between Configuration and Coding

| Configuration | Coding |
|---|---|
| Uses clicks and setup tools | Uses programming logic |
| Suitable for standard business processes | Suitable for complex requirements |
| Easy to maintain | More development effort needed |
| Less flexible | Highly flexible |

---

# 4. Real Examples Where Apex Is Needed

## 1. Online Fee Payment Integration

A college may use external payment applications like Razorpay or Stripe for collecting fees. Simple Flows are not always enough for secure API communication and response handling.

Apex can securely connect Salesforce with external payment systems and process payment responses automatically.

---

## 2. Scholarship Eligibility Calculation

Scholarship approval may depend on:
- Attendance percentage
- Previous semester marks
- Family income
- Reservation category
- Backlog history

Managing all these conditions inside a Flow becomes difficult and hard to maintain.

Apex handles complex calculations and conditions more efficiently.

---

## 3. Bulk Student Data Processing

During admissions, thousands of student records may be uploaded at once. Large-scale processing through Flow can affect performance and create limitations.

Apex supports bulk processing and handles large data operations more effectively.

---

# 5. Integrated College Management System Design

## CRM Usage

Salesforce CRM is used to manage the complete student admission and course management process.

The system stores:
- Student information
- Course details
- Faculty records
- Fee payment status
- Notifications and updates

---

## Objects Used

- Student
- Course
- Faculty
- Admission
- Payment

---

## Relationships

- One student can enroll in multiple courses
- Faculty members are assigned to courses
- Each student has payment records linked to their account

---

## Validation Rules

Validation rules help maintain proper data quality inside the system.

Examples:
- Student email should not be empty
- Phone number must contain valid digits
- Admission should not continue if seats are unavailable

---

## Formula Field Example

Remaining Seats Formula:

```text
Total Seats - Filled Seats
```

This formula automatically shows available seats for each course.

---

# 6. Flow Usage in the System

Flows are used for normal automation tasks such as:
- Sending admission confirmation emails
- Updating application status automatically
- Sending attendance warning notifications
- Sending fee reminder emails

These processes reduce manual work for college staff.

---

# 7. Apex Usage in the System

Apex is used for advanced business requirements such as:
- Scholarship eligibility calculation
- Payment gateway integration
- Bulk admission processing
- Advanced approval conditions

These operations require more flexibility than normal configuration tools.

---

# 8. Pseudocode Examples

## Example 1 – Seat Availability Check

```text
IF available seats = 0
THEN block admission
ELSE allow registration
```

---

## Example 2 – Attendance Warning

```text
IF attendance percentage < 75
THEN send warning notification to student
```

---

## Example 3 – Fee Payment Confirmation

```text
IF payment successful
THEN generate hall ticket
```

---

# 9. Reflection – Why Enterprise Systems Need Programming

Enterprise applications manage large amounts of data and business operations. Some processes are simple and can be automated using Flow, but many real business scenarios involve complicated rules, external systems, and high-volume processing.

Programming languages like Apex help organizations build scalable and flexible solutions that cannot be achieved using only clicks and configuration. Apex gives developers better control over business logic and allows Salesforce applications to support complex enterprise requirements efficiently.

---

