## Approval Process in Salesforce — Complete Beginner Explanation (From Scratch)

### 1. Why Do We Need an Approval Process?

Before understanding Approval Processes, let's first understand the business problem they solve.

Imagine an employee wants to take leave for 10 days.

Should the employee be allowed to approve their own leave request?

Obviously not.

The request should first be reviewed by a manager.

Similarly, in a company:

- A discount above 20% may require manager approval.
- A large expense claim may require finance approval.
- A contract may require legal approval.
- A purchase request may require director approval.
- A loan application may require multiple levels of approval.

Without a structured approval mechanism:

- Employees might bypass rules.
- Unauthorized decisions could be made.
- Auditing becomes difficult.
- Business policies become inconsistent.

To solve this problem, Salesforce provides the **Approval Process** feature.

---

### 2. What Is an Approval Process?

#### Definition

An Approval Process is a Salesforce automation feature that allows records to be submitted for approval and routed through one or more approvers before a final decision is made.

In simple words:

> An Approval Process is a mechanism that allows records to be reviewed and approved or rejected by authorized users.

Think of it as:

```text
Record Created
       ↓
Submitted For Approval
       ↓
Approver Reviews
       ↓
Approve or Reject
       ↓
Final Outcome
```

---

### 3. Real-Life Example

Suppose a sales representative creates an Opportunity.

Company policy states:

```text
Discount > 25%
```

must be approved by the Sales Manager.

Without Approval Process:

```text
Sales Rep
    ↓
Manually emails manager
    ↓
Manager replies
    ↓
Sales Rep updates record
```

Messy and difficult to track.

With Approval Process:

```text
Opportunity Created
        ↓
Submitted For Approval
        ↓
Sales Manager Receives Request
        ↓
Approve or Reject
        ↓
Salesforce Updates Record
```

Everything is tracked automatically.

---

### 4. What Can Be Submitted for Approval?

Any object can participate in an Approval Process.

Examples:

#### Standard Objects

- Opportunity
- Case
- Lead
- Contract
- Quote

#### Custom Objects

- Leave Request
- Purchase Request
- Expense Claim
- Loan Application
- Vendor Approval

Example:

```text
Leave Request Object
```

Employee submits leave request.

Manager approves or rejects it.

---

### 5. Key Terminologies in Approval Process

Before learning the configuration steps, we must understand some important terms.

---

### 6. Submitter

The Submitter is the user who submits the record for approval.

Example:

```text
Employee submits leave request
```

Employee is the:

```text
Submitter
```

---

### 7. Approver

The Approver is the person responsible for reviewing the request.

Example:

```text
Manager reviews leave request
```

Manager is the:

```text
Approver
```

Approver can:

- Approve
- Reject
- Reassign

the request.

---

### 8. Approval Request

When a record enters the approval process, Salesforce creates an approval request.

Example:

```text
Leave Request Submitted
```

Salesforce sends request to manager:

```text
Please review Leave Request #123
```

This request appears in:

- Approver's email
- Salesforce notifications
- Approval work items

---

### 9. Approval Steps

An Approval Process can contain one or more approval levels.

Example:

```text
Employee
      ↓
Manager Approval
      ↓
Director Approval
      ↓
Finance Approval
```

Each level is called an:

```text
Approval Step
```

---

### 10. Approval Process Structure

Every Approval Process contains:

1. Entry Criteria
2. Initial Submission Actions
3. Approval Steps
4. Approval Actions
5. Rejection Actions
6. Final Approval Actions
7. Final Rejection Actions

We will study each one individually.

---

### 11. Entry Criteria

Entry Criteria determines:

> Which records are allowed to enter the approval process?

Example:

```text
Discount Percentage > 25%
```

Only opportunities meeting this condition can be submitted.

Examples:

```text
Amount > 100000
```

```text
Leave Days > 5
```

```text
Expense Amount > 50000
```

If criteria is not satisfied:

```text
Approval Process Not Started
```

---

### 12. Initial Submission Actions

These actions execute immediately after a record is submitted for approval.

Example:

Employee submits leave request.

Salesforce automatically:

```text
Update Status = Pending Approval
```

or

```text
Send Email To Manager
```

or

```text
Lock Record
```

These are called:

```text
Initial Submission Actions
```

---

### 13. Why Does Salesforce Lock the Record?

After submission:

The record is usually locked.

Purpose:

Prevent unauthorized changes while approval is in progress.

Example:

```text
Expense Claim Submitted
```

If employee modifies amount after submission:

Approval becomes meaningless.

Therefore Salesforce locks the record.

Example:

```text
Submitted
     ↓
Record Locked
     ↓
Waiting For Approval
```

---

### 14. Approval Steps

Approval Steps define:

> Who should approve the record?

Example:

```text
Step 1
Manager Approval
```

or

```text
Step 1
Team Lead Approval

Step 2
Manager Approval

Step 3
Director Approval
```

Each step must be completed before proceeding to the next step.

---

### 15. How Salesforce Determines the Approver

Approvers can be determined in multiple ways.

#### Option 1: Specific User

Example:

```text
Sales Manager
```

Always receives the approval request.

---

#### Option 2: Record Owner's Manager

Example:

```text
Employee submits request
```

Salesforce automatically finds:

```text
Employee's Manager
```

and sends approval request.

---

#### Option 3: Role-Based Approver

Example:

```text
Finance Manager Role
```

Whoever belongs to that role receives the request.

---

#### Option 4: Queue

Approval request can be assigned to a queue.

Any queue member can process it.

---

### 16. Approval Actions

When an approver clicks Approve, Salesforce executes approval actions.

Example:

Manager approves leave request.

Salesforce automatically:

```text
Status = Approved
```

or

```text
Send Confirmation Email
```

or

```text
Create Follow-Up Task
```

These actions are called:

```text
Approval Actions
```

---

### 17. Rejection Actions

If the approver rejects the request:

Salesforce executes rejection actions.

Example:

```text
Status = Rejected
```

or

```text
Send Rejection Email
```

or

```text
Notify Employee
```

These actions are called:

```text
Rejection Actions
```

---

### 18. Final Approval Actions

When all approval steps are completed successfully:

Salesforce executes Final Approval Actions.

Example:

```text
Status = Approved
```

```text
Unlock Record
```

```text
Send Approval Notification
```

```text
Create Contract
```

Example Flow:

```text
Step 1 Approved
       ↓
Step 2 Approved
       ↓
Final Approval Reached
       ↓
Final Approval Actions Execute
```

---

### 19. Final Rejection Actions

If approval process ultimately ends in rejection:

Salesforce executes Final Rejection Actions.

Example:

```text
Status = Rejected
```

```text
Unlock Record
```

```text
Notify Requestor
```

```text
Send Email Notification
```

---

### 20. Example: Leave Request Approval Process

Let's build a complete example.

#### Business Requirement

Any leave request longer than 5 days requires manager approval.

---

#### Step 1: Employee Creates Leave Request

```text
Leave Days = 10
```

Status:

```text
Draft
```

---

#### Step 2: Submit for Approval

Employee clicks:

```text
Submit For Approval
```

---

#### Step 3: Entry Criteria Check

Criteria:

```text
Leave Days > 5
```

Result:

```text
10 > 5
```

Condition is true.

Approval process starts.

---

#### Step 4: Initial Submission Actions

Salesforce:

```text
Status = Pending Approval
```

```text
Lock Record
```

```text
Send Email To Manager
```

---

#### Step 5: Manager Reviews Request

Manager receives notification.

Options:

```text
Approve
```

or

```text
Reject
```

---

#### Step 6A: If Approved

Salesforce executes:

```text
Status = Approved
```

```text
Unlock Record
```

```text
Send Confirmation Email
```

---

#### Step 6B: If Rejected

Salesforce executes:

```text
Status = Rejected
```

```text
Unlock Record
```

```text
Notify Employee
```

---

### 21. Multi-Level Approval Example

Consider a purchase request.

Company policy:

```text
Amount > ₹1,00,000
```

requires multiple approvals.

Process:

```text
Employee
      ↓
Manager Approval
      ↓
Finance Approval
      ↓
Director Approval
      ↓
Approved
```

If any approver rejects:

```text
Approval Process Ends
```

and record becomes rejected.

---

### 22. Approval Process Order of Execution

Simplified flow:

```text
Record Created
      ↓
Submit For Approval
      ↓
Entry Criteria Checked
      ↓
Initial Submission Actions
      ↓
Record Locked
      ↓
Approval Steps
      ↓
Approve or Reject
      ↓
Final Approval/Rejection Actions
      ↓
Record Unlocked
```

---

### 23. Approval Process vs Workflow Rule

#### Workflow Rule

Purpose:

```text
Automatic Action
```

Example:

```text
If Amount > 100000
Send Email
```

No human decision required.

---

#### Approval Process

Purpose:

```text
Human Approval Required
```

Example:

```text
If Discount > 25%
Manager Must Approve
```

Human intervention is required.

---

### 24. Approval Process vs Flow

#### Approval Process

Designed specifically for:

- Approvals
- Rejections
- Record locking
- Approval routing

---

#### Flow

Designed for:

- General automation
- Complex logic
- Integrations
- Record creation
- User interaction
- Advanced business processes

Modern Salesforce projects often use:

```text
Flow + Approval Process
```

together.

---

### 25. Interview Definition

An Approval Process is a Salesforce automation feature that routes records through one or more approvers for review and decision-making. It allows authorized users to approve or reject records, supports record locking, multiple approval levels, automated notifications, and execution of actions based on approval or rejection outcomes.

---

### 26. Summary

Approval Process is used when:

- Human approval is required.
- Business policies require authorization.
- Multiple approval levels exist.
- Auditability and tracking are important.

Main Components:

1. Submitter
2. Approver
3. Entry Criteria
4. Initial Submission Actions
5. Approval Steps
6. Approval Actions
7. Rejection Actions
8. Final Approval Actions
9. Final Rejection Actions

Typical Flow:

```text
Record Created
      ↓
Submit For Approval
      ↓
Record Locked
      ↓
Approver Reviews
      ↓
Approve or Reject
      ↓
Final Actions Execute
      ↓
Record Unlocked
```

Common Use Cases:

- Leave Approval
- Expense Approval
- Discount Approval
- Purchase Approval
- Contract Approval
- Loan Approval
- Vendor Approval
