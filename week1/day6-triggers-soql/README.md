# Salesforce Summer Program – Day 6
## SOQL and Apex Triggers

---

# Introduction

In Day 6, I learned how Salesforce stores, retrieves, and reacts to data changes using SOQL and Apex Triggers. I understood how enterprise systems automate actions based on events and how businesses use automation to reduce manual work, improve efficiency, and maintain accurate data.

---

# 1. What is SOQL?

SOQL (Salesforce Object Query Language) is the query language used in Salesforce to retrieve records from Salesforce objects.

It is similar to SQL, but it is specifically designed for Salesforce data structures and object relationships.

SOQL helps developers:
- Retrieve records
- Filter business data
- Access related objects
- Build automation
- Generate reports and dashboards

---

## Real-World Examples in College Management System

- Find all students enrolled in Data Science course
- Retrieve students with attendance below 75%
- Find faculty assigned to Computer Science department
- Display students with pending fee payments
- Retrieve all active courses in current semester

---

## Sample SOQL Queries

```sql
SELECT Name FROM Student__c
```

```sql
SELECT Name, Attendance__c
FROM Student__c
WHERE Attendance__c < 75
```

```sql
SELECT Name
FROM Course__c
WHERE Department__c = 'Computer Science'
```

---

# 2. What is an Apex Trigger?

An Apex Trigger is a piece of Apex code that runs automatically when records are inserted, updated, deleted, or restored in Salesforce.

Triggers are event-driven because they execute automatically whenever a specific database event occurs.

---

## Common Trigger Events

- Before Insert
- After Insert
- Before Update
- After Update
- Before Delete
- After Delete

---

## Why Apex Triggers are Important

Triggers help enterprise systems:
- Automate repetitive tasks
- Maintain data consistency
- Enforce business rules
- Update related records automatically
- Send notifications instantly
- Reduce manual effort

---

# 3. Difference Between Flow and Trigger

| Feature | Flow | Apex Trigger |
|---|---|---|
| Type | Declarative Automation | Programmatic Automation |
| Coding Required | No | Yes |
| Best For | Simple business automation | Complex business logic |
| Development Speed | Faster | Slower |
| Maintenance | Easier | Requires developers |
| Flexibility | Limited | Highly flexible |
| External API Support | Basic | Advanced |
| Performance | Good for standard tasks | Better for complex processing |

---

## My Understanding

Flows are useful when automation is simple and can be designed visually.

Triggers are preferred when:
- logic becomes complex,
- calculations are advanced,
- multiple related objects are involved,
- or external systems must be integrated.

---

# 4. Difference Between Before Trigger and After Trigger

| Before Trigger | After Trigger |
|---|---|
| Runs before data is saved | Runs after data is saved |
| Used for validation and updating values | Used for post-save actions |
| Faster because changes happen before save | Useful for creating related records |
| Record ID may not exist yet | Record ID becomes available |

---

## Before Trigger Example

Automatically calculate scholarship percentage before saving student information.

---

## After Trigger Example

Send welcome email after a new student registration is completed.

---

# 5. Trigger Use Cases (College Management System)

## 1. Student Registration Automation

### Event:
After a student record is inserted.

### Automatic Actions:
- Send welcome email
- Generate student ID
- Create portal account

### Business Benefit:
Improves onboarding process and reduces administrative work.

---

## 2. Attendance Warning System

### Event:
After attendance record is updated.

### Automatic Actions:
Send warning notification when attendance drops below 75%.

### Business Benefit:
Helps students improve attendance before exams.

---

## 3. Course Capacity Notification

### Event:
After new course enrollment is added.

### Automatic Actions:
Notify faculty when course capacity becomes full.

### Business Benefit:
Prevents over-enrollment and scheduling problems.

---

## 4. Fee Payment Confirmation

### Event:
After fee payment record is created.

### Automatic Actions:
- Generate payment receipt
- Send confirmation email
- Update payment status

### Business Benefit:
Improves financial transparency and automation.

---

## 5. Faculty Assignment Automation

### Event:
After course schedule is updated.

### Automatic Actions:
- Assign classrooms automatically
- Notify assigned faculty
- Update timetable records

### Business Benefit:
Reduces manual scheduling errors.

---

# 6. Flow vs Trigger Decision Thinking

| Scenario | Flow or Trigger? | Reason |
|---|---|---|
| Simple email notification | Flow | Easy visual automation |
| Updating related records | Flow | Standard business process |
| Complex fee eligibility calculation | Trigger | Requires advanced logic |
| External payment API integration | Trigger | Better API handling |
| Attendance warning notification | Flow | Simple condition-based logic |
| Scholarship eligibility processing | Trigger | Complex validation and calculations |

---

# 7. Query Thinking (Business Query Ideas)

## Student Queries
- Find all students enrolled in Artificial Intelligence course
- Find students with attendance below 75%
- Find students who have unpaid fees
- Find all final year Computer Science students

---

## Course Queries
- Find all available courses this semester
- Find courses with more than 100 enrolled students
- Find courses handled by Professor Ramesh

---

## Faculty Queries
- Find faculty teaching Machine Learning subjects
- Find faculty assigned to multiple departments
- Find faculty available for morning classes

---

# 8. Reflection Task
## Why Enterprise Systems Need Event-Driven Behavior

Enterprise systems manage thousands of records and business operations every day. Manual monitoring becomes impossible at large scale.

Event-driven systems allow software to react automatically whenever important events occur.

Examples:
- When payment is completed → receipt generated automatically
- When attendance becomes low → warning notification sent
- When course becomes full → faculty alerted immediately
- When customer places an order → inventory updates automatically

Without event-driven systems:
- Manual work increases
- Human errors become common
- Data inconsistency occurs
- Business operations slow down

Triggers and automation help organizations become faster, smarter, and more efficient.

---

