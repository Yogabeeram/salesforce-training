# Day 4 – Salesforce Flow Builder

## What is Flow Builder?

Flow Builder is a Salesforce no-code automation tool used to automate business processes visually without writing programming code. It allows businesses to create workflows, automate repetitive tasks, update records automatically, send notifications, and guide users through screens using drag-and-drop components.

Flow Builder helps organizations:
- Reduce manual work
- Improve productivity
- Maintain consistency
- Save time
- Reduce human errors

It is widely used in enterprise systems for workflow automation.

---

# Why Automation Matters

Businesses perform many repetitive tasks daily such as:
- Sending emails
- Updating records
- Assigning approvals
- Generating IDs
- Sending reminders

Doing these tasks manually:
- Takes time
- Causes errors
- Reduces efficiency
- Creates inconsistency

Automation improves:
- Speed
- Accuracy
- Productivity
- Customer experience
- Business efficiency

Salesforce Flow Builder helps automate these processes without coding.

---

# Types of Flows in Salesforce

## 1. Screen Flow

Screen Flow is an interactive flow where users enter information through screens.

### Features:
- User interaction
- Forms and inputs
- Step-by-step guidance

### Example:
Student registration form.

---

## 2. Record-Triggered Flow

This flow runs automatically when records are:
- Created
- Updated
- Deleted

### Features:
- Fully automated
- No user interaction
- Real-time automation

### Example:
Automatically send email after student registration.

---

## 3. Scheduled Flow

Runs automatically at a scheduled time.

### Example:
Daily reminder emails for fee payments.

---

## 4. Autolaunched Flow

Runs in the background without screens.

### Example:
Updating student status automatically.

---

# Difference Between Screen Flow and Record-Triggered Flow

| Feature | Screen Flow | Record Triggered Flow |
|---|---|---|
| User Interaction | Required | Not Required |
| Execution | Manually started | Automatically triggered |
| Use Case | Forms and guided processes | Backend automation |
| Screens | Available | Not Available |
| Example | Admission Form | Auto Email Notification |

---

# Automation Ideas for College Management System

## 1. Auto Email After Student Registration

### Description
Automatically send confirmation email after registration.

### Benefits
- Instant communication
- Reduces manual work
- Improves student experience

---

## 2. Auto Generate Student ID

### Description
Generate unique student ID automatically after admission.

### Benefits
- Avoids duplicate IDs
- Saves administration time

---

## 3. Fee Deadline Reminder

### Description
Automatically send reminders before fee due dates.

### Benefits
- Improves fee collection
- Reduces missed payments

---

## 4. Notify Faculty When Course is Full

### Description
Send notification to faculty when course capacity reaches limit.

### Benefits
- Better course management
- Prevents overbooking

---

## 5. Auto Update Remaining Seats

### Description
Update available seats automatically after each registration.

### Benefits
- Real-time seat tracking
- Reduces errors

---

# Flow Design Thinking

## Selected Process:
Auto Email After Student Registration

---

# Flow Diagram

```text
[Student Registration Submitted]
                |
                v
      [Record Triggered Flow]
                |
                v
   [Check Student Email Exists?]
          /               \
        Yes                No
         |                  |
         v                  v
 [Send Confirmation]    [Stop Flow]
         |
         v
 [Update Status = Email Sent]
         |
         v
        End
# Manual vs Automated Process

## Process: Fee Payment Reminder

---

# Manual Process

1. Staff checks student fee records manually.
2. Staff prepares reminder messages.
3. Emails are sent individually.
4. Responses are tracked manually.

## Problems in Manual Process

- Time consuming
- Human errors
- Missed reminders
- Poor efficiency
- Increased workload
- Delays in communication

---

# Automated Process Using Salesforce

1. Scheduled Flow checks fee due dates automatically.
2. Reminder emails are generated automatically.
3. Notifications are sent instantly.
4. Records are updated automatically.

## Improvements After Automation

- Faster process
- Accurate reminders
- Saves staff effort
- Better productivity
- Improved consistency
- Reduced operational cost

---

# Reflection – Why Automation Matters

Companies automate repetitive business processes because automation:

- Saves time
- Reduces manual effort
- Improves accuracy
- Increases productivity
- Reduces operational cost
- Provides faster services
- Improves consistency

Automation is important in enterprise systems because organizations handle thousands of records and tasks daily. Manual management becomes difficult and inefficient. Salesforce Flow Builder allows businesses to automate workflows without coding, making process management easier and faster.

---

# Reflective Questions

## 1. Why do companies automate workflows?

Companies automate workflows to:
- Improve efficiency
- Reduce errors
- Save time
- Increase productivity
- Improve customer experience

---

## 2. What problems happen with manual processes?

Manual processes may cause:
- Delays
- Human errors
- Inconsistency
- High workload
- Reduced productivity

---

## 3. Difference between Screen Flow and Record Triggered Flow?

| Screen Flow | Record Triggered Flow |
|---|---|
| Requires user interaction | Runs automatically |
| Uses screens/forms | No screens involved |
| Started manually | Triggered by record changes |
| Used for guided processes | Used for backend automation |

---

## 4. Why is no-code automation powerful?

No-code automation allows non-programmers to create business workflows quickly using visual tools without writing code.

---

## 5. When should automation be avoided?

Automation should be avoided when:
- Processes change frequently
- Human judgment is required
- The process is very small/simple
- Decisions require personal interaction

---

## 6. How does automation improve consistency and productivity?

Automation follows predefined rules every time, ensuring:
- Consistent results
- Faster execution
- Reduced manual workload
- Better operational efficiency
