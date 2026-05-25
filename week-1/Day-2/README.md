# Salesforce Day 2 – Platform Basics

---

# 1. What is Salesforce Platform?

Salesforce Platform is a cloud-based platform that helps businesses manage customer relationships, automate business processes, store data, and build custom applications.

Salesforce works completely on the cloud, so users can access it from anywhere using the internet. It follows a multi-tenant architecture where multiple organizations securely share the same infrastructure.

The platform provides:
- Configuration tools (clicks without coding)
- Development tools (Apex, APIs, Lightning Components)

This allows both administrators and developers to build business solutions efficiently.

---

# 2. CRM Concepts Inside Salesforce Platform

CRM concepts like Account, Contact, Lead, and Opportunity are represented as Objects inside Salesforce.

These objects work together inside Apps to help businesses manage customer data and sales activities.

## Example Flow

Lead → Contact → Opportunity → Customer

## Explanation

- Lead represents a potential customer
- Contact stores verified customer details
- Opportunity tracks business deals
- Customer represents a successful relationship

This workflow helps businesses manage communication, sales, and customer relationships efficiently.

---

# 3. What is an App in Salesforce?

An App in Salesforce is a collection of related tabs, objects, reports, dashboards, and tools designed for a specific business purpose.

Apps help users organize work efficiently by grouping required functionalities together.

## Examples
- Sales App
- Service App
- Marketing App

## Sales App Contains
- Accounts
- Contacts
- Opportunities
- Reports
- Dashboards

## Advantages of Apps
- Easy navigation
- Better organization
- Improved productivity
- Faster access to data

---

# 4. What is an Object in Salesforce?

An Object in Salesforce is similar to a database table used to store information.

Objects contain:
- Fields (Columns)
- Records (Rows)

## Types of Objects

### Standard Objects
Predefined objects provided by Salesforce.

#### Examples
- Account
- Contact
- Opportunity
- Lead

### Custom Objects
Objects created according to business requirements.

#### Examples
- Student
- Faculty
- Library Book
- Patient

Objects help organizations store and manage data efficiently.

---

# 5. What is a Tab in Salesforce?

A Tab is a user interface component that allows users to access objects, records, reports, dashboards, and applications easily.

Tabs appear in the navigation menu inside Salesforce.

## Examples
- Accounts Tab
- Contacts Tab
- Opportunities Tab

## Benefits of Tabs
- Quick navigation
- Better user experience
- Easy access to records
- Organized interface

---

# 6. Difference Between App and Object

| Feature | App | Object |
|---|---|---|
| Definition | Collection of related tools and objects | Database table used to store data |
| Purpose | Organizes business processes | Stores records and information |
| Contains | Tabs, Objects, Dashboards | Fields and Records |
| Example | Sales App | Account Object |

---

# 7. What is Multi-Tenant Architecture?

Multi-tenant architecture means multiple organizations share the same Salesforce infrastructure securely.

In Salesforce:
- One platform serves multiple customers
- Data remains secure and isolated
- All users receive updates automatically

## Advantages
- Cost effective
- Automatic updates
- Scalable
- Secure

This is one of the major reasons Salesforce is cloud-based and highly popular.

---

# 8. Configuration vs Coding

## What is Configuration?

Configuration means building functionality in Salesforce using clicks instead of code.

### Configuration Tools
- Validation Rules
- Flow Builder
- Process Builder
- Reports and Dashboards
- Page Layouts

## When to Use Configuration?
- Simple business requirements
- Faster development
- Easy maintenance
- No coding required

---

## What is Coding?

Coding is used when complex business logic cannot be implemented using configuration tools.

Salesforce developers use:
- Apex
- Lightning Web Components (LWC)
- Visualforce
- APIs

## When to Use Coding?
- Advanced business logic
- External integrations
- Real-time processing
- Complex automation

---

# 9. Real System Thinking – College Management System

## App Name
College Management App

---

## Standard Objects
- Account
- Contact

---

## Custom Objects
- Student
- Faculty
- Course
- Attendance
- Fees
- Examination

---

# 10. User Interaction With the System

## Admin
- Manage student records
- Manage fees
- Generate reports

## Faculty
- Update attendance
- Upload marks
- Manage courses

## Students
- View attendance
- Check marks
- Access course details

---

# 11. Modules Completed

## Agentforce 360 Platform Basics
- Platform overview
- Apps and objects
- Salesforce navigation
- Architecture basics

## Agentforce 360 Platform Development Basics
- Configuration vs coding
- Apex overview
- Development process
- APIs and integrations

## Salesforce Development Basics
- Development workflow
- Playground setup
- Practical exercises

---



# Conclusion

Day 2 provided a deeper understanding of Salesforce Platform architecture, application structure, objects, tabs, multi-tenant architecture, and configuration versus coding concepts. It also introduced real-world system design thinking using Salesforce applications.
