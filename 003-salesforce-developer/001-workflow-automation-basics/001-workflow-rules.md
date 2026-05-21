## Workflow Rules in Salesforce

### 1. Why Do We Need Automation?

Before understanding Workflow Rules, we first need to understand the problem they solve.

Imagine a company where sales representatives create customer records every day.

Whenever a new customer record is created, certain actions must happen:

- An email should be sent to the manager.
- A follow-up task should be created.
- Some fields should be updated automatically.
- Another team should be notified.

If employees perform these actions manually every time:

- Work becomes slow.
- Human errors increase.
- Employees may forget important tasks.
- Business processes become inconsistent.

To solve this problem, Salesforce provides automation tools.

Automation means:

> Let Salesforce perform repetitive business tasks automatically without requiring a user to perform them manually.

Example:

Whenever an Opportunity becomes Closed Won, automatically notify the Finance Team.

Instead of a sales representative sending an email manually, Salesforce can do it automatically.

This concept is called:

**Business Process Automation**

---

### 2. What Is a Workflow Rule?

A Workflow Rule is one of Salesforce's automation features.

#### Definition

A Workflow Rule is a declarative automation tool that automatically performs predefined actions when specified conditions are met.

In simple words:

> IF something happens, THEN Salesforce automatically performs an action.

Think of it as:

```text
IF Condition is True
THEN Perform Action
```

---

### 3. Real-Life Example of a Workflow Rule

Suppose your company has a process:

Whenever a Lead becomes qualified, the Sales Manager must be notified.

Without automation:

1. Sales Representative updates Lead.
2. Sales Representative manually sends email.
3. Manager receives email.

With Workflow Rule:

```text
Condition:
Lead Status = Qualified

Action:
Send Email Alert
```

Process becomes:

```text
Lead Updated
      ↓
Condition Evaluated
      ↓
Condition True
      ↓
Email Sent Automatically
```

No manual effort is required.

---

### 4. Components of a Workflow Rule

Every Workflow Rule consists of two major parts:

#### Part A: Criteria (Condition)

Criteria tells Salesforce:

> When should this workflow execute?

Examples:

```text
Opportunity Amount > 100000
```

```text
Lead Status = Qualified
```

```text
Case Priority = High
```

Salesforce continuously checks whether these conditions are satisfied.

---

#### Part B: Actions

Actions tell Salesforce:

> What should happen after the condition becomes true?

Examples:

```text
Send Email
```

```text
Update Field
```

```text
Create Task
```

```text
Send Data to External System
```

So the complete workflow looks like:

```text
IF Condition
THEN Execute Action
```

---

### 5. On Which Objects Can Workflow Rules Be Created?

Workflow Rules can be created on both standard and custom objects.

Examples of standard objects:

- Account
- Contact
- Lead
- Opportunity
- Case
- Campaign

Examples of custom objects:

- Student
- Employee
- Project
- Leave Request
- Invoice

Any object that supports business automation can use Workflow Rules.

---

### 6. Example Using a Lead Object

Suppose your company receives leads from its website.

Business requirement:

Whenever a lead comes from the website, notify the sales team.

Workflow configuration:

```text
Object:
Lead
```

```text
Condition:
Lead Source = Website
```

```text
Action:
Send Email Alert
```

Process:

```text
Website Lead Created
          ↓
Workflow Evaluates Condition
          ↓
Condition True
          ↓
Email Sent To Sales Team
```

---

### 7. Workflow Rule Evaluation Criteria

Salesforce needs to know:

> When should the workflow check the condition?

For this purpose Salesforce provides Evaluation Criteria.

There are three evaluation options.

---

### 8. Evaluation Option 1 — Created

The workflow executes only when the record is created.

Example:

```text
Lead Created
```

Salesforce checks the condition once.

After that, it never evaluates the workflow again for that record.

#### Example

Condition:

```text
Lead Source = Website
```

Lead Creation:

```text
Lead Source = Website
```

Result:

```text
Condition True
↓
Workflow Executes
```

Later if the lead is edited:

```text
Lead Status Changed
```

Workflow will NOT execute again.

Because evaluation was configured as:

```text
Created
```

---

### 9. Evaluation Option 2 — Created and Every Time It's Edited

The workflow executes:

- When record is created
- Every time record is updated

#### Example

Workflow Condition:

```text
Status = Qualified
```

Initial Record:

```text
Status = New
```

Result:

```text
Condition False
```

No action occurs.

Later user updates:

```text
Status = Qualified
```

Result:

```text
Condition True
↓
Workflow Executes
```

Later user updates another field:

```text
Phone Number Changed
```

Condition is still:

```text
Status = Qualified
```

Result:

```text
Condition True
↓
Workflow Executes Again
```

This option can sometimes create duplicate actions because the workflow executes every time the record is edited while the condition remains true.

---

### 10. Evaluation Option 3 — Created and Edited to Subsequently Meet Criteria

This is the most commonly used evaluation option.

The workflow executes only when the condition changes from:

```text
False → True
```

#### Example

Workflow Condition:

```text
Status = Qualified
```

Initially:

```text
Status = New
```

Condition Result:

```text
False
```

No action occurs.

User updates record:

```text
Status = Qualified
```

Condition Result:

```text
True
```

Transition:

```text
False → True
```

Workflow executes.

Later user edits another field:

```text
Email Updated
```

Condition Result:

```text
True
```

Transition:

```text
True → True
```

Workflow does NOT execute again.

This prevents duplicate emails, duplicate tasks, and duplicate updates.

---

### 11. Types of Workflow Actions

Workflow Rules can perform four major actions.

#### 1. Email Alert

Automatically sends emails.

Example:

```text
Opportunity Stage = Closed Won
```

Action:

```text
Send Email To Finance Team
```

Process:

```text
Opportunity Closed Won
           ↓
Workflow Rule
           ↓
Email Alert
           ↓
Finance Team Receives Email
```

---

#### 2. Field Update

Automatically updates field values.

Example:

Condition:

```text
Case Priority = High
```

Action:

```text
Escalation Status = Yes
```

Before:

```text
Priority = High
Escalation Status = No
```

After Workflow:

```text
Priority = High
Escalation Status = Yes
```

No user interaction is required.

---

#### 3. Task Creation

Automatically creates tasks.

Example:

Condition:

```text
Lead Status = Qualified
```

Action:

```text
Create Follow-up Call Task
```

Result:

Sales Representative automatically receives a task:

```text
Call Customer
Due Tomorrow
```

No manual task creation is required.

---

#### 4. Outbound Message

Used for integrations.

Salesforce automatically sends information to an external application.

Example:

```text
Order Approved
```

Action:

```text
Send Order Information To ERP System
```

Process:

```text
Salesforce
     ↓
Workflow Rule
     ↓
Outbound Message
     ↓
External System
```

This communication happens automatically.

---

### 12. Immediate Actions

Immediate actions execute as soon as the workflow condition becomes true.

Example:

Condition:

```text
Case Priority = High
```

Action:

```text
Send Email Alert
```

Timeline:

```text
Condition Met
      ↓
Action Executes Immediately
```

No waiting period exists.

---

### 13. Time-Dependent Actions

Sometimes actions should occur after a specific time period.

Workflow Rules support time-based actions.

Example:

Business Requirement:

If a lead is not contacted within three days, create a reminder task.

Workflow Configuration:

```text
Lead Created
```

Action:

```text
After 3 Days
Create Follow-Up Task
```

Timeline:

```text
Day 1
Lead Created

      ↓

Day 3
Task Created Automatically
```

This is called a:

**Time-Dependent Workflow Action**

---

### 14. Complete Real Business Example

Let us build a complete workflow.

#### Business Requirement

Whenever a Lead becomes Qualified:

1. Notify Sales Manager.
2. Create Follow-Up Task.
3. Update Review Status.

---

#### Step 1: Select Object

```text
Lead
```

---

#### Step 2: Define Criteria

```text
Status = Qualified
```

---

#### Step 3: Select Evaluation Criteria

```text
Created and Edited to Subsequently Meet Criteria
```

---

#### Step 4: Configure Actions

##### Action 1

Email Alert:

```text
Notify Sales Manager
```

##### Action 2

Task Creation:

```text
Follow-Up Call
```

##### Action 3

Field Update:

```text
Review Status = Pending
```

---

#### Complete Process Flow

```text
Sales Representative Updates Lead
                 ↓
Status = Qualified
                 ↓
Workflow Evaluates Condition
                 ↓
Condition True
                 ↓
Email Sent To Manager
                 ↓
Task Created
                 ↓
Review Status Updated
```

Everything happens automatically.

---

### 15. Workflow Rules in Salesforce Order of Execution

Whenever a record is saved, Salesforce executes several internal processes.

A simplified version is:

```text
Record Saved
      ↓
Validation Rules
      ↓
Workflow Rules
      ↓
Workflow Actions
      ↓
Additional Processing
```

Important point:

Workflow Rules execute only after the record successfully passes validation.

If validation fails, workflow rules never run.

---

### 16. Limitations of Workflow Rules

Workflow Rules are considered an older Salesforce automation technology.

They support only limited actions.

Supported actions:

- Email Alert
- Field Update
- Task Creation
- Outbound Message

Not supported:

- Creating records
- Deleting records
- Complex decision making
- Loops
- Advanced branching
- Multi-step business processes
- Rich integrations
- Reusable automation logic

Because of these limitations Salesforce introduced more advanced automation tools.

---

### 17. Workflow Rules vs Process Builder vs Flow

#### Workflow Rules

Characteristics:

- Old automation technology
- Simple automation
- Limited actions
- Easy to configure

Best for:

- Basic business requirements

---

#### Process Builder

Characteristics:

- More powerful than Workflow Rules
- Supports additional actions
- Can create records
- Supports multiple criteria

Current Status:

Process Builder is being phased out by Salesforce.

---

#### Flow

Characteristics:

- Most powerful automation platform
- Supports complex business logic
- Can create, update, and delete records
- Supports loops and decisions
- Supports integrations
- Supports user screens
- Supports reusable automation

Current Salesforce Recommendation:

> Use Flow for all new automation development.

---

### 18. Why Is Salesforce Moving Away from Workflow Rules?

Workflow Rules work well for simple requirements.

However modern businesses require:

- Complex approvals
- Multiple decision paths
- Integrations
- Dynamic processing
- Advanced automation

Workflow Rules cannot handle these efficiently.

Therefore Salesforce's strategic automation platform is:

**Salesforce Flow**

New projects should generally use Flow instead of Workflow Rules.

---

### 19. Interview Definition

A Workflow Rule is a declarative Salesforce automation feature that automatically triggers actions such as Email Alerts, Field Updates, Task Creation, and Outbound Messages when specified criteria are met. It follows an IF-THEN logic model and is considered a legacy automation tool, with Salesforce Flow being the recommended automation solution for modern implementations.

---

### 20. Summary

A Workflow Rule consists of four major parts:

1. Object
2. Criteria
3. Evaluation Criteria
4. Actions

Workflow can perform four actions:

- Email Alert
- Field Update
- Task Creation
- Outbound Message

Workflow actions can be:

- Immediate
- Time-Based

Workflow Rules are an older automation technology and are gradually being replaced by Salesforce Flow for new implementations because Flow provides significantly more power and flexibility.
