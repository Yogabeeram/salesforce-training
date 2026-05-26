# Day 7 Notes – Testing, DX and Asynchronous Apex

# Why Testing Matters

Testing ensures:
- Reliability
- Correct functionality
- Bug prevention
- Safe deployments

Salesforce requires testing before deployment to production.

---

# Apex Testing

Apex test classes validate:
- Triggers
- Apex classes
- Business logic
- Database operations

---

# Example Test Class

```java
@isTest
private class StudentTestClass {

    @isTest
    static void testInsert() {

        Student__c stu = new Student__c(
            Name = 'John'
        );

        insert stu;

        System.assertEquals('John', stu.Name);

    }

}
```

---

# Asynchronous Apex

Asynchronous Apex runs processes in background.

Used for:
- Bulk emails
- Large data processing
- External integrations

---

# Queueable Apex Example

```java
public class QueueJobExample implements Queueable {

    public void execute(QueueableContext context) {

        System.debug('Async Job Running');

    }

}
```

---

# Salesforce DX

Salesforce DX is a modern developer workflow.

Benefits:
- Source-driven development
- Better collaboration
- GitHub integration
- Faster deployments

---

# Salesforce CLI

CLI is used for:
- Creating projects
- Deploying code
- Running tests
- Managing orgs

---

# Example CLI Commands

```bash
sf project generate --name CollegeSystem
```

```bash
sf org login web
```

```bash
sf apex run test
```

---

# Complete System Workflow

1. Student registers
2. Validation Rules check data
3. Flow sends confirmation
4. Trigger updates course count
5. Formula recalculates seats
6. Notifications are generated
7. Database stores records
8. Reports show analytics

---

# Important Test Cases

- Invalid email
- Duplicate registration
- Trigger execution
- Attendance calculation
- Course overbooking

---

# Key Learning

Enterprise systems require:
- Testing
- Automation
- Version control
- Structured workflows

Salesforce combines:
- Flows
- Triggers
- Validation Rules
- DX
- CLI

to create scalable enterprise applications.
```
