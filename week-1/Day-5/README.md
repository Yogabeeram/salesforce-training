
# Day 5 – Salesforce Apex Introduction

# What is Apex?

Apex is Salesforce’s programming language used to build custom business logic and advanced automation inside Salesforce.

It is similar to Java and helps developers:
- Create custom logic
- Handle complex automation
- Integrate external systems
- Perform database operations
- Build enterprise-level applications

Apex is used when Salesforce Flows or declarative tools are not enough.

---

# Why Salesforce Needs Programming

Salesforce provides many no-code tools like:
- Flow Builder
- Validation Rules
- Process Automation

However, some enterprise requirements are:
- Too complex
- Need advanced calculations
- Require integrations
- Need custom processing logic

In such cases, Apex programming is required.

---

# Difference Between Flow and Apex

| Flow | Apex |
|---|---|
| No-code automation | Code-based automation |
| Easy to build | Requires programming |
| Best for simple workflows | Best for complex logic |
| Faster development | More flexible |
| Limited customization | Full customization |

---

# Difference Between Configuration and Coding

| Configuration | Coding |
|---|---|
| Uses clicks and setup | Uses programming |
| Faster implementation | More development effort |
| Easy maintenance | Requires developers |
| Limited flexibility | Highly flexible |
| Suitable for standard logic | Suitable for complex logic |

---

# Integrated College Management System Design

## CRM

The College Management System acts as a CRM system that manages:
- Student admissions
- Course enrollment
- Faculty management
- Attendance
- Fee tracking

---

# Objects Used

## Student Object
Stores:
- Student Name
- Email
- Attendance
- Fee Status

## Course Object
Stores:
- Course Name
- Remaining Seats
- Faculty Assigned

## Faculty Object
Stores:
- Faculty Details
- Department
- Assigned Courses

---

# Relationships

| Relationship | Description |
|---|---|
| Student ↔ Course | Students enroll in courses |
| Faculty ↔ Course | Faculty teach courses |

---

# Validation Rules

## Example Validation

- Student email is mandatory
- Attendance cannot exceed 100%
- Fee amount cannot be negative

---

# Formula Example

## Remaining Seats Formula

Remaining Seats = Total Seats - Registered Students

This formula automatically updates available seats.

---

# Flow Automation

## Example Flow Automations

### 1. Auto Notification
Send email after student registration.

### 2. Fee Reminder
Automatically notify students before deadline.

### 3. Attendance Alert
Notify students if attendance drops below 75%.

---

# Apex Usage

Apex is used for:
- Advanced business logic
- Complex calculations
- External integrations
- Custom automation

---

# Real Examples Where Apex Is Needed

## 1. Complex Fee Calculation

### Example
Calculate:
- Scholarship discounts
- Late fees
- Tax calculations

### Why Flow is Not Enough
Complex multi-condition calculations become difficult in Flow.

---

## 2. Integration with External Payment System

### Example
Connect Salesforce with:
- Razorpay
- PayPal
- Banking APIs

### Why Apex is Needed
External API integration requires custom programming.

---

## 3. Advanced Eligibility Logic

### Example
Student eligible only if:
- Attendance > 75%
- No pending fees
- Required prerequisite course completed

### Why Apex is Needed
Complex conditional processing requires code-based logic.

---

# Pseudocode Examples

## Example 1 – Course Registration

```text
IF remaining seats = 0
THEN block registration
ELSE allow registration
```

---

## Example 2 – Attendance Notification

```text
IF attendance < 75%
THEN notify student
```

---

## Example 3 – Fee Reminder

```text
IF fee due date is near
THEN send reminder email
```

---

# Reflection – Why Enterprise Systems Need Programming

Enterprise systems cannot rely only on clicks and configuration because businesses often require:
- Complex business rules
- Advanced automation
- External integrations
- High flexibility
- Custom processing

Declarative tools are powerful for standard automation, but enterprise applications eventually require programming for scalability and customization.

Apex helps developers build enterprise-grade solutions beyond the limitations of no-code tools.

---

# Reflective Questions

## 1. Why is Apex needed if Salesforce already has Flows?

Apex is needed for:
- Complex logic
- Advanced calculations
- API integrations
- Custom automation

---

## 2. When should developers prefer no-code solutions?

Developers should prefer no-code solutions when:
- Logic is simple
- Faster development is needed
- Maintenance should be easier

---

## 3. What problems require custom programming?

Problems requiring programming include:
- Complex calculations
- Third-party integrations
- Advanced validations
- Large-scale processing

---

## 4. Why is business logic important in enterprise systems?

Business logic ensures:
- Correct process execution
- Rule enforcement
- Automation accuracy
- Efficient operations

---

## 5. Why should developers avoid unnecessary coding?

Unnecessary coding:
- Increases maintenance
- Adds complexity
- Reduces development speed

---

## 6. How does programming increase flexibility?

Programming allows:
- Full customization
- Advanced processing
- Integration capabilities
- Scalable enterprise solutions

---

# Day 5 Learning Outcome

By the end of Day 5, I understood:
- What Apex is
- Why Salesforce needs programming
- Difference between declarative and programmatic development
- How Apex connects with business logic
- When to use Flow vs Apex
- How enterprise systems combine automation and programming
```
