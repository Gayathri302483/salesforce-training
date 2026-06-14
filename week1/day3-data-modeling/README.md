Day 3 – Data Modeling

1. Difference Between App, Object, Record, and Field
App
An app is a collection of tabs, objects, and features designed for a particular business process.
Object
An object stores a specific type of data in Salesforce. It is similar to a table in a database.
Record
A record is a single row of information inside an object.
Field
A field stores individual pieces of data inside a record.

2. Standard vs Custom Objects
Standard Objects
Standard objects are already available in Salesforce.
Examples:
- Account
- Contact
- Lead
- Opportunity
Custom Objects
Custom objects are created based on organization requirements.
Examples:
- Student
- Faculty
- Department
- Course

3. College Management System Data Model
Objects
- Student
- Faculty
- Course
- Department
- Enrollment

Relationships
Department → Student
One department can contain many students.
Department → Faculty
One department can contain many faculty members.
Faculty → Course
One faculty member can teach multiple courses.
Student ↔ Course
Students can enroll in multiple courses and one course can contain multiple students.  
This relationship is managed using the Enrollment object.
Relationship Types

| Relationship | Type |
|---|---|
| Student → Department | Lookup |
| Faculty → Department | Lookup |
| Course → Faculty | Lookup |
| Enrollment → Student | Lookup |
| Enrollment → Course | Lookup |
Diagram

```text
Department
   |
   |---- Faculty
   |
   |---- Student
   |
   |---- Course
              |
              |---- Enrollment
                          |
                          |---- Student
```


4. Formula Fields

Full Name
Combines first name and last name automatically.

Why automatic calculation is useful
It avoids manual typing and keeps names consistent.

Remaining Seats
Calculates available seats after student enrollments.

Why automatic calculation is useful
It helps admins quickly know seat availability.

Percentage
Calculates percentage using obtained marks and total marks.

Why automatic calculation is useful
It reduces calculation mistakes and saves time.

5. Validation Rules

Email Cannot Be Empty
Problem prevented
Prevents saving student records without contact information.
Age Cannot Be Negative
Problem prevented
Stops invalid age values from entering the system.
Course Capacity Limit
Problem prevented
Prevents adding students beyond course capacity.

6. Why Structured Enterprise Data Matters
Structured data helps organizations manage information in an organized way. It allows businesses to connect related records, generate reports, reduce duplicate data, and improve decision making.
Using structured systems is more efficient than maintaining random spreadsheets because data becomes easier to search, update, and analyze.
