
# Day 6 – SOQL and Apex Triggers

# What is SOQL?

SOQL (Salesforce Object Query Language) is used to retrieve data from Salesforce objects.

It is similar to SQL but designed specifically for Salesforce.

SOQL helps developers:
- Retrieve records
- Filter data
- Access related objects
- Generate reports
- Process business logic

---

# Why SOQL is Important

Enterprise systems store large amounts of data such as:
- Students
- Courses
- Faculty
- Attendance
- Fees

SOQL helps retrieve the required data efficiently.

Example uses:
- Find students with low attendance
- Retrieve course details
- Get pending fee records

---

# What is an Apex Trigger?

An Apex Trigger is code that executes automatically when data changes occur in Salesforce.

Triggers run:
- Before insert
- After insert
- Before update
- After update
- Before delete
- After delete

Triggers help automate event-driven business logic.

---

# Why Triggers Are Important

Enterprise systems must react automatically to events.

Examples:
- Send email after registration
- Notify faculty when course is full
- Alert students about low attendance

Triggers make systems responsive and intelligent.

---

# Difference Between Flow and Trigger

| Flow | Apex Trigger |
|---|---|
| No-code automation | Code-based automation |
| Easier to build | Requires programming |
| Best for simple automation | Best for complex logic |
| Limited flexibility | Highly flexible |
| Faster implementation | Advanced customization |

---

# Difference Between Before and After Trigger

| Before Trigger | After Trigger |
|---|---|
| Runs before record is saved | Runs after record is saved |
| Used for validations | Used for notifications |
| Modify record values | Perform related actions |
| Faster processing | Access final saved record |

---

# Trigger Thinking – College Management System

## 1. After Student Registration → Send Welcome Email

### Trigger Event
After Insert

### Why?
When a student record is created, the system automatically sends a welcome email.

---

## 2. After Course Becomes Full → Notify Faculty

### Trigger Event
After Update

### Why?
When remaining seats become zero, faculty receives notification.

---

## 3. After Attendance Drops Below 75% → Send Warning

### Trigger Event
After Update

### Why?
When attendance is updated and falls below minimum requirement, alert student.

---

## 4. After Fee Payment → Update Fee Status

### Trigger Event
After Update

### Why?
When payment is completed, fee status changes automatically.

---

## 5. After Student Withdraws → Increase Available Seats

### Trigger Event
After Delete or Update

### Why?
When a student leaves a course, available seats should increase automatically.

---

# Flow vs Trigger Thinking

| Scenario | Best Choice | Reason |
|---|---|---|
| Simple email notification | Flow | Easy no-code automation |
| Complex fee eligibility check | Apex Trigger | Requires advanced logic |
| Updating related records | Flow | Simple automation |
| External API integration | Apex Trigger | Requires programming |
| Multi-condition validations | Apex Trigger | Better flexibility |

---

# Query Thinking

## Query Examples

### 1. Find all students in Course A

Retrieve all student records enrolled in Course A.

---

### 2. Find all courses handled by Faculty X

Retrieve all courses assigned to a specific faculty member.

---

### 3. Find students with attendance below 75%

Retrieve all students whose attendance percentage is less than 75%.

---

### 4. Find students with pending fees

Retrieve all students whose fee status is unpaid.

---

### 5. Find courses with no available seats

Retrieve all courses where remaining seats equal zero.

---

# Reflection – Why Enterprise Systems Need Event-Driven Behavior

Enterprise systems manage thousands of operations daily.

Systems must automatically react to:
- Data changes
- User actions
- Business events
- Updates in records

Without event-driven behavior:
- Processes become slow
- Errors increase
- Manual work increases
- Productivity decreases

Triggers and automation help enterprise systems:
- Respond instantly
- Maintain consistency
- Improve efficiency
- Reduce human effort

Salesforce uses Flows and Apex Triggers to build intelligent business systems.

---

# Reflective Questions

## 1. Why do systems need triggers?

Triggers allow systems to respond automatically when data changes occur.

---

## 2. Difference between polling and event-driven systems?

| Polling | Event-Driven |
|---|---|
| Continuously checks for changes | Reacts only when events occur |
| Less efficient | More efficient |
| Slower response | Instant response |

---

## 3. Why are database queries important?

Queries help retrieve required data quickly and efficiently from large databases.

---

## 4. When should Flows be preferred over Triggers?

Flows should be preferred when:
- Logic is simple
- No coding is needed
- Faster implementation is required

---

## 5. What problems happen if automation logic becomes too complex?

Complex automation may:
- Become difficult to maintain
- Reduce performance
- Increase errors
- Create debugging difficulties

---

## 6. Why should developers think carefully before automating actions?

Poor automation design may:
- Cause incorrect actions
- Trigger unnecessary operations
- Reduce system efficiency

Developers should automate only meaningful and well-designed business processes.

---

# Day 6 Learning Outcome

By the end of Day 6, I understood:
- How Salesforce retrieves data using SOQL
- What Apex Triggers are
- How event-driven systems work
- Difference between Flow and Trigger
- Difference between Before and After Trigger
- How enterprise systems react automatically to data changes
```
