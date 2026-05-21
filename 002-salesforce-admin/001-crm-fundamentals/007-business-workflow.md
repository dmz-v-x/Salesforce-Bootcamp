## Business Workflow

### 1. What is a Business Workflow?

A Business Workflow is a sequence of steps or activities that a business follows to complete a specific process from start to finish.

In simple words:

```text
Input
  ↓
Step 1
  ↓
Step 2
  ↓
Step 3
  ↓
Output
```

A workflow defines:

- what needs to happen
- when it should happen
- who should perform it
- what happens next

It ensures work is completed in a consistent and organized manner.

---

### 2. Simple Real-Life Example

Suppose you order food online.

The workflow looks like:

```text
Customer Places Order
          ↓
Restaurant Receives Order
          ↓
Food Prepared
          ↓
Delivery Partner Assigned
          ↓
Food Picked Up
          ↓
Food Delivered
```

This entire sequence is a workflow.

Every order follows the same process.

---

### 3. Why Do Companies Need Workflows?

Without workflows:

- employees work differently
- tasks are forgotten
- approvals are missed
- delays occur
- errors increase

Workflows ensure that everyone follows the same process.

Benefits:

- consistency
- automation
- accountability
- faster execution
- fewer mistakes

---

### 4. Key Components of a Workflow

Every workflow usually contains:

| Component | Description |
|------------|------------|
| Trigger | Event that starts the workflow |
| Steps | Activities performed |
| Decision Points | Conditions that determine next action |
| Participants | People or systems involved |
| Output | Final result |

---

### 5. Example Workflow Structure

```text
Trigger
   ↓
Action 1
   ↓
Decision
   ↓
Yes → Action 2
No  → Action 3
   ↓
Complete
```

Most business processes follow this pattern.

---

## Understanding Workflow Through a CRM Example

### 6. Lead Management Workflow

Suppose a customer submits a website inquiry.

Workflow:

```text
Website Form Submitted
          ↓
Lead Created
          ↓
Lead Assigned To Sales Rep
          ↓
Sales Call Scheduled
          ↓
Lead Qualified?
      ↓          ↓
     Yes         No
      ↓          ↓
Opportunity     Closed
Created
```

This is a Lead Management Workflow.

---

### 7. What Happens Without This Workflow?

Imagine 100 leads arrive daily.

Without workflow:

```text
No Assignment

No Follow-Up

No Tracking

Leads Lost
```

Company loses revenue.

With workflow:

```text
Automatic Assignment

Automatic Notifications

Automatic Follow-Ups

Better Conversion
```

---

## Business Workflow Example #1: Leave Approval Process

### 8. Employee Requests Leave

Workflow:

```text
Employee Applies Leave
           ↓
Manager Reviews Request
           ↓
Approve?
      ↓          ↓
     Yes         No
      ↓          ↓
Leave         Rejected
Approved
      ↓
HR Notified
```

---

### 9. Decision Point

Important part:

```text
Approve?
```

A workflow often contains decisions.

Depending on the answer:

```text
Different Path
```

is followed.

---

## Business Workflow Example #2: Purchase Approval

### 10. Purchase Request Workflow

Employee wants a laptop.

Workflow:

```text
Request Submitted
        ↓
Manager Approval
        ↓
Finance Approval
        ↓
Purchase Order Created
        ↓
Vendor Selected
        ↓
Laptop Purchased
```

This ensures proper control and approvals.

---

## Business Workflow Example #3: Customer Support Workflow

### 11. Support Workflow

Customer reports issue.

Workflow:

```text
Case Created
      ↓
Assigned To Agent
      ↓
Investigation
      ↓
Issue Resolved?
   ↓           ↓
 Yes          No
  ↓            ↓
Close Case   Escalate
```

This ensures no customer issue is ignored.

---

## Workflow vs Process

### 12. Important Difference

Many beginners confuse Process and Workflow.

| Process | Workflow |
|----------|----------|
| Bigger business objective | Sequence of tasks |
| High-level view | Detailed execution |
| Contains multiple workflows | Part of a process |
| Focus on outcome | Focus on activities |

---

### 13. Example

Business Process:

```text
Lead To Cash
```

Contains multiple workflows:

```text
Lead Assignment Workflow

Approval Workflow

Quote Workflow

Order Workflow

Payment Workflow
```

So:

```text
Process > Workflow
```

A process is larger than a workflow.

---

## Workflow in Salesforce

### 14. Why Salesforce Uses Workflows?

Businesses want Salesforce to perform repetitive work automatically.

Examples:

```text
Assign Leads

Send Emails

Create Tasks

Update Records

Request Approvals
```

Instead of employees doing everything manually.

---

### 15. Example Salesforce Workflow

Scenario:

A new Lead is created.

Workflow:

```text
Lead Created
      ↓
Assign To Salesperson
      ↓
Send Welcome Email
      ↓
Create Follow-Up Task
      ↓
Notify Manager
```

All actions can happen automatically.

---

## Before Automation

### 16. Manual Process

Salesperson must:

```text
Check New Lead
      ↓
Assign Lead
      ↓
Send Email
      ↓
Create Task
      ↓
Inform Manager
```

Time-consuming and error-prone.

---

## After Automation

### 17. Automated Workflow

```text
Lead Created
      ↓
System Executes Everything
```

Result:

```text
Faster

Consistent

Accurate

Scalable
```

---

## Workflow Automation in Salesforce

### 18. Traditional Workflow Rule

Historically Salesforce provided:

```text
Workflow Rules
```

for automation.

Workflow Rules could:

- send email alerts
- update fields
- create tasks
- send outbound messages

---

### 19. Modern Salesforce Approach

Today Salesforce recommends:

```text
Flow Builder
```

instead of Workflow Rules.

Flow Builder is much more powerful.

Most modern automation is built using:

```text
Salesforce Flows
```

---

### 20. Example Flow Workflow

Scenario:

```text
Opportunity Closed Won
```

Workflow:

```text
Opportunity Closed Won
           ↓
Create Welcome Task
           ↓
Send Customer Email
           ↓
Notify Account Manager
           ↓
Create Onboarding Record
```

All automatically.

---

## Real Enterprise Example

### 21. Employee Onboarding Workflow

New employee joins company.

Workflow:

```text
HR Creates Employee Record
           ↓
Manager Assigned
           ↓
Laptop Request Created
           ↓
Email Account Created
           ↓
Training Assigned
           ↓
Employee Activated
```

Large companies automate this entire workflow.

---

## Practical on Salesforce Free Account

### 22. Goal

Create your first business workflow using Salesforce Flow Builder.

---

### Step 1: Login to Salesforce Developer Org

Open your Developer Org.

---

### Step 2: Open Flow Builder

Navigate:

```text
Setup
   ↓
Flow
   ↓
New Flow
```

---

### Step 3: Select Record-Triggered Flow

Choose:

```text
Record-Triggered Flow
```

Click:

```text
Create
```

---

### Step 4: Select Object

Choose:

```text
Lead
```

Trigger:

```text
When Record Is Created
```

Meaning:

```text
Whenever New Lead Is Created
```

workflow starts automatically.

---

### Step 5: Add Action

Add:

```text
Create Task
```

Configure:

```text
Subject:
Follow Up New Lead

Status:
Not Started
```

---

### Step 6: Save Flow

Save:

```text
Lead Follow-Up Workflow
```

---

### Step 7: Activate Flow

Click:

```text
Activate
```

Flow is now live.

---

### Step 8: Test Workflow

Create a new Lead.

```text
Leads
   ↓
New
```

Save Lead.

---

### Step 9: Verify Result

Open:

```text
Tasks
```

Observe:

```text
Follow Up New Lead
```

task automatically created.

Your first business workflow is working.

---

## Advanced Practical

### 23. Build Lead Assignment Workflow

Goal:

```text
Lead Created
      ↓
Assign Owner Automatically
      ↓
Create Follow-Up Task
```

Build using Flow Builder.

This closely resembles real CRM automation.

---

## Real Salesforce Interview Perspective

### 24. Interview Definition

A Business Workflow is a predefined sequence of business activities and decisions that guide work from initiation to completion, ensuring consistency, efficiency, and automation across organizational processes.

