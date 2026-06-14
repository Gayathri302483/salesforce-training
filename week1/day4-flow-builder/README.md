# Salesforce Summer Program – Day 4

Introduction
Today I learned about Salesforce Flow Builder and how businesses automate processes using no-code tools.

1. What is Flow Builder?
Flow Builder is a Salesforce automation tool used to automate business processes without writing code. It helps organizations create workflows visually using drag-and-drop elements.
Flow Builder can:
- Create records
- Update records
- Send emails
- Make decisions automatically
- Reduce manual work

2. Types of Flows
Screen Flow
Screen Flow interacts with users through screens and input forms. It is mainly used for guided processes where users enter information manually.
Example:
Student registration form.
Record Triggered Flow
Record Triggered Flow runs automatically when a record is created, updated, or deleted.
Example:
Sending attendance warning email automatically.


3. Automation Ideas for College Management System
1. Automatic Attendance Warning
If student attendance drops below 75%, a warning email is sent automatically.
Why useful:
Helps students improve attendance early.
2. Auto Classroom Allocation
Classrooms are assigned automatically based on student strength.
Why useful:
Reduces scheduling confusion.

3. Exam Hall Ticket Generation
Hall tickets are generated automatically after fee payment confirmation.
Why useful:
Speeds up exam preparation process.

4. Faculty Notification for Assignment Submission
Faculty receives notification after all students submit assignments.
Why useful:
Improves tracking efficiency.


5. Scholarship Eligibility Update
Scholarship eligibility updates automatically after marks calculation.
Why useful:
Reduces manual verification work.

4. Flow Diagram
Flow Process Chosen:
Automatic Attendance Warning System
Flow Logic:
1. Attendance record updated
2. System checks attendance percentage
3. Decision checks whether attendance is below 75%
4. Warning email is sent automatically
5. Process ends

Student Attendance Updated
        ↓
Check Attendance %
        ↓
Attendance < 75% ?
      /     \
    Yes      No
    ↓         ↓
Send Warning  End
Email

5. Manual vs Automated Process
Manual Process
Staff manually verifies fee payment and generates hall tickets for students.
Problems in Manual System
- Slow processing
- Higher chance of errors
- Extra workload
- Delays during busy periods
Automated Process Using Salesforce
Salesforce Flow automatically verifies payment status and generates hall tickets instantly.
Benefits
- Faster workflow
- Accurate information
- Better efficiency
- Reduced manual effort

6. Reflection – Why Automation Matters

Automation is important because businesses handle thousands of repetitive operations daily. Manual work consumes time and may create inconsistencies. Salesforce automation improves productivity, reduces errors, maintains consistency, and allows organizations to scale operations efficiently.

ce Flow Builder helps businesses automate workflows without coding. I also learned the importance of process automation in enterprise systems.
