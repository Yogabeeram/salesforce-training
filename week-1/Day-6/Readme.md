# Day 6 – SOQL and Apex Triggers

## What is SOQL?

SOQL (Salesforce Object Query Language) is used to retrieve data from Salesforce objects.

It helps developers:
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

# What is an Apex Trigger?

An Apex Trigger is code that runs automatically when records are inserted, updated, or deleted.

Triggers help automate business processes and event-driven actions.

---

# Trigger Events

- Before Insert
- After Insert
- Before Update
- After Update
- Before Delete
- After Delete

---

# Before Trigger

Before Triggers run before records are saved into the database.

They are mainly used for:
- Validation
- Updating values before save
- Preventing incorrect data

## Example

```java
trigger StudentBeforeTrigger on Student__c (before insert) {

    for(Student__c stu : Trigger.new) {

        if(stu.Age__c < 0) {

            stu.addError('Age cannot be negative');

        }

    }

}
```

This trigger prevents invalid age values.

---

# After Trigger

After Triggers run after records are saved into the database.

They are mainly used for:
- Sending notifications
- Updating related records
- External integrations

## Example

```java
trigger StudentAfterTrigger on Student__c (after insert) {

    for(Student__c stu : Trigger.new) {

        System.debug('Welcome Email Sent To: ' + stu.Name);

    }

}
```

This trigger automatically performs actions after record creation.

---

# Difference Between Flow and Trigger

| Flow | Apex Trigger |
|---|---|
| No-code automation | Code-based automation |
| Easier to build | Requires programming |
| Best for simple automation | Best for complex logic |
| Faster implementation | Advanced flexibility |

---

# Trigger Thinking – College Management System

## 1. After Student Registration → Send Welcome Email

### Trigger Event
After Insert

### Purpose
Automatically send welcome message after registration.

---

## 2. After Course Becomes Full → Notify Faculty

### Trigger Event
After Update

### Purpose
Notify faculty when no seats remain.

---

## 3. After Attendance Drops Below 75% → Send Warning

### Trigger Event
After Update

### Purpose
Alert students with low attendance.

---

## 4. After Fee Payment → Update Fee Status

### Trigger Event
After Update

### Purpose
Automatically mark fees as paid.

---

## 5. After Student Withdrawal → Increase Available Seats

### Trigger Event
After Delete

### Purpose
Update available course seats automatically.

---

# Query Thinking Examples

## Find all students in Course A

```sql
SELECT Name
FROM Student__c
WHERE Course__c = 'Course A'
```

---

## Find all courses handled by Faculty X

```sql
SELECT Name
FROM Course__c
WHERE Faculty__c = 'Faculty X'
```

---

## Find students with attendance below 75%

```sql
SELECT Name, Attendance__c
FROM Student__c
WHERE Attendance__c < 75
```

---

# Reflection – Why Enterprise Systems Need Event-Driven Behavior

Enterprise systems handle thousands of data changes daily.

Systems must automatically react to:
- Record updates
- User actions
- Business events
- Notifications

Triggers and automation help:
- Improve efficiency
- Reduce manual work
- Maintain consistency
- Increase productivity

Salesforce uses Flows and Apex Triggers to create intelligent enterprise systems.

---

# Reflective Questions

## 1. Why do systems need triggers?

Triggers help systems react automatically when database events occur.

---

## 2. Difference between polling and event-driven systems?

| Polling | Event-Driven |
|---|---|
| Continuously checks for updates | Reacts only when events occur |
| Slower | Faster |
| Less efficient | More efficient |

---

## 3. Why are database queries important?

Queries help retrieve required data quickly and efficiently.

---

## 4. When should Flows be preferred over Triggers?

Flows should be preferred for:
- Simple automation
- Faster implementation
- No-code solutions

---

## 5. What problems happen if automation logic becomes too complex?

Complex automation may:
- Reduce maintainability
- Increase errors
- Affect performance

---

## 6. Why should developers think carefully before automating actions?

Poor automation design can:
- Trigger unnecessary actions
- Reduce system efficiency
- Create maintenance problems

---

# Day 6 Learning Outcome

By the end of Day 6, I understood:
- What SOQL is
- How Salesforce retrieves data
- What Apex Triggers do
- Difference between Before and After Triggers
- How enterprise systems react automatically to data changes
```
