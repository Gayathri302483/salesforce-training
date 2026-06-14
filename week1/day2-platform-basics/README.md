Day 2 - Salesforce Platform Basics

What is Salesforce Platform?
Salesforce is a cloud-based CRM platform used by companies to manage customers, sales, services, and business processes. It helps organizations store data, automate work, and build applications without managing servers.
The platform provides tools like Apps, Objects, Tabs, Automation, Reports, APIs, and Apex for development and customization.

App
An App in Salesforce is a collection of related tabs and objects used for a specific business purpose.
Example:
Sales App contains Accounts, Contacts, Leads, and Opportunities.

Object
An Object is used to store data in Salesforce. It is similar to a table in a database.
Examples:
Account object stores company details
Contact object stores customer details
Objects contain records and fields.

Tab
A Tab is the user interface used to access objects and records in Salesforce.
Example:
The Account tab opens all Account records.
Tabs help users navigate easily inside the application.

CRM Concepts in Salesforce
CRM concepts like Account, Contact, and Opportunity are available as standard objects in Salesforce.
Account stores company or customer information
Contact stores individual customer details
Opportunity stores sales deals or business opportunities
These objects are available inside Salesforce Apps and users access them through Tabs.

Configuration vs Coding

Configuration (No Code)
Configuration is used when requirements can be completed using Salesforce tools without programming.
Examples:
1. Creating validation rules
2. Building flows and automation
Configuration is faster and easier for simple business requirements.

Coding (Apex)
Coding is used when business logic becomes complex and cannot be handled using configuration.
Examples:
1. Integrating external payment systems
2. Creating complex approval or calculation logic
Developers use Apex and APIs for advanced customization.

Hospital Management System Design
App Name

Hospital Management App
Objects

Patient
Stores patient details like name, age, disease, and contact number.

Doctor
Stores doctor information like specialization and availability.

Appointment
Stores appointment details between patients and doctors.

Medical Record
Stores diagnosis, prescriptions, and treatment history.

Billing
Stores payment and billing information.

User Interaction

 Receptionists create patient records and appointments.
 Doctors view patient history and update medical records.
 Admin manages doctors, billing, and hospital operations.
 Patients can view appointment details and reports.




