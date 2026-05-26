# Day 6 Notes – SOQL and Apex Triggers

# What is SOQL?

SOQL stands for Salesforce Object Query Language.

It is used to retrieve Salesforce data.

SOQL helps:
- Retrieve records
- Filter data
- Access related objects
- Process business information

---

# Example Queries

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
FROM Student__c
WHERE Fee_Status__c = 'Pending'
```

---

# What is SOSL?

SOSL stands for Salesforce Object Search Language.

It is used to search multiple objects together.

---

# DML Operations

DML operations include:
- Insert
- Update
- Delete

These operations manipulate Salesforce records.

---

# What is an Apex Trigger?

Apex Triggers are code that execute automatically when records change.

Trigger events include:
- Before Insert
- After Insert
- Before Update
- After Update
- Before Delete
- After Delete

---

# Before Trigger Example

```java
trigger StudentBeforeTrigger on Student__c (before insert) {

    for(Student__c stu : Trigger.new) {

        if(stu.Age__c < 0) {

            stu.addError('Age cannot be negative');

        }

    }

}
```

Purpose:
- Validation
- Prevent invalid records

---

# After Trigger Example

```java
trigger StudentAfterTrigger on Student__c (after insert) {

    for(Student__c stu : Trigger.new) {

        System.debug('Welcome Email Sent');

    }

}
```

Purpose:
- Notifications
- Related actions

---

# Flow vs Trigger

| Flow | Trigger |
|---|---|
| No-code | Programming |
| Simple automation | Complex automation |
| Easier | Flexible |

---

# Event-Driven Systems

Enterprise systems automatically react to:
- Data changes
- User activities
- Business events

Benefits:
- Faster automation
- Reduced manual work
- Better consistency

---

# Key Learning

Salesforce combines:
- SOQL
- DML
- Flows
- Apex Triggers

to build scalable enterprise applications.
```
