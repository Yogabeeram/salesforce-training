# Day 7 – Testing, Asynchronous Apex, DX and CLI

# Why Testing Matters

Testing is important in enterprise systems because it ensures that business logic works correctly and prevents system failures.

Salesforce requires testing to:
- Prevent bugs
- Improve reliability
- Validate automation
- Maintain system stability
- Ensure safe deployments

Without proper testing:
- Incorrect data may be stored
- Automation may fail
- Business processes may break
- Users may experience errors

---

# What is Apex Testing?

Apex Testing is the process of testing Apex code using test classes.

Test classes verify:
- Triggers
- Classes
- Business logic
- Validations
- Database operations

---

# Example Apex Test Class

```java
@isTest
private class StudentTestClass {

    @isTest
    static void testStudentInsert() {

        Student__c stu = new Student__c(
            Name = 'John',
            Attendance__c = 85
        );

        insert stu;

        Student__c result = [
            SELECT Name
            FROM Student__c
            WHERE Name = 'John'
            LIMIT 1
        ];

        System.assertEquals('John', result.Name);

    }

}
```

This test verifies that student records are inserted correctly.

---

# What is Asynchronous Apex?

Asynchronous Apex allows processes to run in the background instead of executing immediately.

It is used for:
- Large operations
- Bulk processing
- Background jobs
- External integrations

---

# Why Async Processing is Important

Some operations take time and should not slow down users.

Async processing improves:
- Performance
- Scalability
- User experience
- System efficiency

---

# Examples of Async Processing

## 1. Sending Bulk Emails

Large email batches should run in background.

---

## 2. Large Report Generation

Generating reports for thousands of records takes time.

---

## 3. Data Synchronization

Syncing Salesforce with external systems should run asynchronously.

---

# Queueable Apex Example

```java
public class StudentQueueableJob implements Queueable {

    public void execute(QueueableContext context) {

        System.debug('Background Processing Started');

    }

}
```

This Queueable Apex job runs in the background.

---

# What is Salesforce DX?

Salesforce DX (Developer Experience) is a modern development workflow for Salesforce developers.

It helps teams:
- Manage source code
- Use version control
- Automate deployments
- Improve collaboration

---

# What is Salesforce CLI?

Salesforce CLI is a command-line tool used to manage Salesforce development from terminal or VS Code.

CLI helps developers:
- Create projects
- Deploy code
- Run tests
- Manage orgs
- Automate workflows

---

# Example CLI Commands

## Create Salesforce Project

```bash
sf project generate --name CollegeManagementSystem
```

---

## Authorize Org

```bash
sf org login web
```

---

## Deploy Source

```bash
sf project deploy start
```

---

## Run Apex Tests

```bash
sf apex run test
```

---

# Complete System Workflow – College Management System

## Step 1 – Student Registration

Student fills registration form.

---

## Step 2 – Validation Rules Check Data

Validation Rules verify:
- Email format
- Required fields
- Duplicate records

If invalid data exists, registration is blocked.

---

## Step 3 – Flow Sends Confirmation

After successful registration:
- Flow sends confirmation email
- Notification is generated automatically

---

## Step 4 – Trigger Updates Course Count

Apex Trigger automatically:
- Updates enrolled student count
- Checks course availability

---

## Step 5 – Formula Recalculates Remaining Seats

Formula Field calculates:

```text
Remaining Seats = Total Seats - Registered Students
```

---

## Step 6 – Platform Event Sends Notification

If course becomes full:
- Faculty receives notification
- Admin receives alert

---

## Step 7 – Database Stores Records

Salesforce database stores:
- Student details
- Course details
- Attendance
- Fee information

---

## Step 8 – Reports Show Analytics

Reports display:
- Student count
- Attendance analysis
- Pending fee reports
- Course statistics

---

# Important Test Cases

## 1. Invalid Email Validation

### Problem if Not Tested
Incorrect email addresses may be stored.

---

## 2. Duplicate Registration

### Problem if Not Tested
Students may register multiple times.

---

## 3. Course Overbooking

### Problem if Not Tested
Course capacity limits may fail.

---

## 4. Attendance Calculation

### Problem if Not Tested
Incorrect attendance percentages may appear.

---

## 5. Trigger Execution

### Problem if Not Tested
Automation actions may fail after record updates.

---

# Reflection – Why Enterprise Software Development Needs Structured Workflows

Enterprise systems are large and complex.

Professional workflows help teams:
- Manage source code
- Collaborate efficiently
- Track changes
- Prevent deployment issues
- Maintain software quality

GitHub, DX, and CLI provide:
- Version control
- Team collaboration
- Faster development
- Automated deployments
- Better project management

Structured workflows are essential for scalable enterprise development.

---

# Revision Questions

## 1. Why are tests important in enterprise systems?

Tests ensure reliability and prevent business failures.

---

## 2. What problems happen without testing?

Without testing:
- Bugs increase
- Automation fails
- Incorrect data is stored

---

## 3. Why is asynchronous processing useful?

It improves performance by running heavy tasks in background.

---

## 4. Difference between synchronous and asynchronous processing?

| Synchronous | Asynchronous |
|---|---|
| Runs immediately | Runs in background |
| User waits | User does not wait |
| Slower for heavy tasks | Better performance |

---

## 5. Why do developers use version control?

Version control helps track code changes and collaborate safely.

---

## 6. Why is GitHub important?

GitHub helps:
- Store code
- Track versions
- Collaborate with teams

---

## 7. Why is DX useful for teams?

DX provides:
- Source-driven development
- Better collaboration
- Automated workflows

---

## 8. How do Flows, Triggers and Validation Rules work together?

- Validation Rules verify data
- Flows automate simple processes
- Triggers handle advanced logic

Together they create intelligent enterprise systems.

---

## 9. Why should business logic be tested carefully?

Incorrect business logic can break enterprise operations.

---

## 10. Why is developer workflow important in large teams?

Structured workflows improve:
- Coordination
- Code quality
- Deployment safety

---

# Day 7 Learning Outcome

By the end of Day 7, I understood:
- Why testing matters
- What Asynchronous Apex is
- Why DX and CLI are important
- Professional Salesforce development workflow
- How all Salesforce concepts integrate together
```
