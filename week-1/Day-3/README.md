# Salesforce Summer Program – Day 3

# Day 3 – Data Modeling and Business Logic in Salesforce

## Introduction
Day 3 focused on understanding how Salesforce stores and manages enterprise data using structured models. The learning included Objects, Fields, Records, Relationships, Formula Fields, and Validation Rules.

---

# 1. Difference Between App, Object, Record, and Field

| Concept | Description | Example |
|---|---|---|
| App | Collection of related tabs and functionalities | College Management App |
| Object | Database table storing related data | Student Object |
| Record | Single entry inside an object | Rahul Student Record |
| Field | Specific information inside a record | Email, Age |

---

# 2. Standard vs Custom Objects

| Standard Objects | Custom Objects |
|---|---|
| Pre-built by Salesforce | Created by users |
| Account, Contact | Student, Faculty |
| Common CRM usage | Organization-specific usage |
| Cannot be deleted | Can be customized |

## Explanation
Standard objects are provided by Salesforce for common business needs, while custom objects are created according to specific organizational requirements.

---

# 3. College Management System – Data Model

## Objects
- Student
- Faculty
- Course
- Department

---

## Relationships

### Department → Faculty
- One department can have many faculty members.
- Relationship Type: Lookup Relationship

### Department → Course
- One department can offer many courses.
- Relationship Type: Lookup Relationship

### Course → Student
- One course can contain many students.
- Relationship Type: Lookup Relationship

### Faculty → Course
- One faculty member can teach multiple courses.
- Relationship Type: Lookup Relationship

---

# Relationship Diagram

```text
Department
   |
   |--- Faculty
   |
   |--- Course
            |
            |--- Student
# 4. Formula Fields

## Formula Field 1 – Full Name

### Formula

```text
First_Name + " " + Last_Name
```

### Purpose
Automatically combines first name and last name.

### Why Automation?
Reduces manual errors and maintains consistency.

---

## Formula Field 2 – Remaining Seats

### Formula

```text
Total_Seats - Enrolled_Students
```

### Purpose
Shows available seats in a course.

### Why Automation?
Seats change frequently, so automation prevents mistakes.

---

## Formula Field 3 – Student Percentage

### Formula

```text
(Obtained_Marks / Total_Marks) * 100
```

### Purpose
Calculates student percentage automatically.

### Why Automation?
Saves time and avoids manual calculation errors.

---

# 5. Validation Rules

## Validation Rule 1 – Email Cannot Be Empty

### Problem Prevented
Prevents incomplete student records.

---

## Validation Rule 2 – Student Age Cannot Be Negative

### Problem Prevented
Stops invalid age entries.

---

## Validation Rule 3 – Course Seats Cannot Exceed Limit

### Problem Prevented
Avoids overbooking of courses.

---

# 6. Reflection – Why Structured Data Matters

Companies need structured data because business information is interconnected. Random spreadsheets create duplication, inconsistency, and difficulty in managing large-scale operations.

## Structured Systems Provide

- Better accuracy
- Faster reporting
- Easier automation
- Improved security
- Better scalability

Enterprise systems like Salesforce organize data efficiently using objects, fields, records, and relationships.

---

# Reflective Questions

## 1. Why can’t companies manage everything using Excel sheets?

Excel sheets become difficult to manage when data grows large and interconnected.

---

## 2. Why are relationships important between objects?

Relationships connect related business data and reduce duplication.

---

## 3. What problems happen if data is inconsistent?

Inconsistent data causes reporting errors and incorrect decisions.

---

## 4. Why should repetitive calculations be automated?

Automation improves speed, accuracy, and efficiency.

---

## 5. Why should invalid data be blocked early?

It maintains data quality and prevents business problems.

---

## 6. Why is Salesforce called a metadata-driven platform?

Salesforce applications are built using metadata and configuration instead of traditional coding.
