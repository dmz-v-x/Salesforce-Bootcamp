## Apex Execution Context

### 1. What Is an Apex Execution Context?

An **Apex Execution Context** is the environment Salesforce creates whenever Apex code starts running.

Think of it as a temporary workspace created by Salesforce for a single execution of code.

Example:

```text
User clicks Save
        ↓
Salesforce creates Execution Context
        ↓
Apex code runs
        ↓
Execution completes
        ↓
Execution Context destroyed
```

The execution context exists only while the code is running.

---

### 2. Why Does Salesforce Create an Execution Context?

Suppose Salesforce did not create separate execution contexts.

Imagine:

```text
User A updates Account
User B creates Opportunity
User C converts Lead
```

All operations would share the same memory and resources.

Problems:

```text
Data corruption
Security issues
Incorrect results
Resource conflicts
```

Therefore Salesforce creates a separate execution context for every execution.

Each execution gets:

```text
Own memory
Own variables
Own governor limits
Own transaction
Own security information
```

---

### 3. Simple Real-World Analogy

Imagine a large examination hall.

```text
Student A → Desk A
Student B → Desk B
Student C → Desk C
```

Every student gets:

```text
Own answer sheet
Own pen
Own question paper
```

Students do not share desks.

Similarly:

```text
Execution Context A
Execution Context B
Execution Context C
```

Each execution gets its own isolated environment.

---

### 4. When Is an Execution Context Created?

Salesforce creates an execution context whenever Apex starts executing.

Examples:

#### User Action

```text
Button Click
```

---

#### Trigger Execution

```text
Account Created
```

---

#### Flow Calling Apex

```text
Flow
 ↓
Invocable Apex
```

---

#### REST API Request

```text
External System
 ↓
Apex REST Service
```

---

#### Batch Apex

```text
Scheduled Batch Job
```

---

#### Queueable Apex

```text
Background Job
```

---

#### Scheduled Apex

```text
Nightly Processing
```

Every one of these creates an execution context.

---

### 5. What Exists Inside an Execution Context?

Salesforce stores all runtime information inside the execution context.

Conceptually:

```text
Execution Context
│
├── Variables
├── Objects
├── Heap Memory
├── Call Stack
├── Governor Counters
├── User Information
├── Security Context
├── Transaction State
└── Database Operations
```

Everything required to execute Apex exists here.

---

### 6. Variables Inside Execution Context

Example:

```apex
String name = 'John';
Integer age = 25;
```

Runtime stores:

```text
name → John
age → 25
```

inside the execution context.

Visual:

```text
Execution Context

name = John
age = 25
```

When execution ends:

```text
Variables removed
Memory released
```

---

### 7. Objects Inside Execution Context

Example:

```apex
Account acc = new Account();
```

Runtime stores:

```text
Account Object
```

inside memory belonging to the execution context.

Visual:

```text
Execution Context
        │
        ▼
Account Object
```

No other execution can access this object.

---

### 8. Heap Memory

Heap memory stores:

```text
Objects
Collections
Strings
Lists
Maps
Sets
```

Example:

```apex
List<Account> accounts =
new List<Account>();
```

Memory allocated:

```text
Execution Context
      │
      ▼
Heap Memory
      │
      ▼
Account List
```

When execution finishes:

```text
Heap Cleared
```

---

### 9. Call Stack

Suppose:

```apex
MethodA()
```

calls:

```apex
MethodB()
```

which calls:

```apex
MethodC()
```

Runtime creates:

```text
Call Stack

MethodC
MethodB
MethodA
```

The execution context manages this stack.

As methods finish:

```text
MethodC removed
MethodB removed
MethodA removed
```

---

### 10. Governor Limits Are Stored Per Context

One of the most important concepts.

Salesforce initializes governor limit counters for every execution context.

Example:

```text
SOQL Queries Used
DML Statements Used
CPU Time Used
Heap Used
```

Visual:

```text
Execution Context

SOQL Count = 0
DML Count = 0
CPU Time = 0
```

As code executes:

```text
SOQL Count = 1
SOQL Count = 2
SOQL Count = 3
```

Salesforce continuously updates these counters.

---

### 11. Example of Governor Limits Inside Context

Code:

```apex
Account a =
[
 SELECT Id
 FROM Account
 LIMIT 1
];
```

Execution:

```text
Execution Context Created

SOQL Count = 0

Query Executes

SOQL Count = 1
```

The runtime tracks every operation.

---

### 12. User Information Inside Context

Every execution knows:

```text
Who initiated it
```

Example:

```text
User: John Smith
Profile: Sales User
Role: Sales Manager
```

Runtime stores:

```text
Current User Information
```

inside the execution context.

This helps Salesforce enforce security.

---

### 13. Security Context

Salesforce must determine:

```text
Can this user access Account?
Can this user update Opportunity?
Can this user see Salary field?
```

These permissions are maintained through the security context.

Visual:

```text
Execution Context
      │
      ▼
Security Context
      │
      ▼
Permissions
```

---

### 14. Transaction State

Every execution context belongs to a transaction.

Example:

```apex
Insert Account
Insert Contact
Update Opportunity
```

Runtime tracks:

```text
Pending Database Changes
```

inside the transaction state.

Nothing is permanently saved yet.

---

### 15. What Happens When an Error Occurs?

Suppose:

```apex
Insert Account
Insert Contact
Exception Occurs
```

Execution context detects:

```text
Transaction Failure
```

Salesforce performs:

```text
Rollback
```

Meaning:

```text
Account Removed
Contact Removed
```

Database returns to original state.

---

### 16. Execution Context Lifetime

Lifecycle:

```text
Execution Starts
      ↓
Execution Context Created
      ↓
Variables Created
      ↓
Code Executes
      ↓
Database Operations
      ↓
Commit / Rollback
      ↓
Execution Context Destroyed
```

It is temporary.

After completion nothing remains except committed database changes.

---

### 17. Multiple Users = Multiple Contexts

Suppose:

```text
User A creates Account
User B updates Contact
User C closes Opportunity
```

Salesforce creates:

```text
Execution Context #1

Execution Context #2

Execution Context #3
```

Each has:

```text
Own memory
Own variables
Own governor limits
Own transaction
```

They are isolated from one another.

---

### 18. Trigger Execution Context

Example:

```text
Account Inserted
```

Trigger fires.

Salesforce creates:

```text
Execution Context
      │
      ▼
Trigger Variables

Trigger.new
Trigger.old
Trigger.newMap
Trigger.oldMap
```

These special trigger variables exist only inside that trigger's execution context.

---

### 19. Batch Apex Execution Context

Suppose:

```text
5000 Records
```

Batch size:

```text
200
```

Salesforce processes:

```text
Batch 1 → Context 1

Batch 2 → Context 2

Batch 3 → Context 3
```

Each batch receives:

```text
Fresh governor limits
Fresh memory
Fresh transaction
```

This is why Batch Apex can process very large datasets.

---

### 20. Queueable and Future Contexts

When asynchronous jobs execute:

```text
Queueable Job
Future Method
Scheduled Job
```

Salesforce creates a completely new execution context.

Therefore:

```text
New Governor Limits
New Transaction
New Memory
```

This separation is extremely important in Salesforce architecture.

---

### 21. Complete Visualization

```text
User Clicks Save
        │
        ▼
Execution Context Created
        │
        ├── Variables
        ├── Objects
        ├── Heap Memory
        ├── Call Stack
        ├── Governor Counters
        ├── User Information
        ├── Security Context
        └── Transaction State
        │
        ▼
Apex Executes
        │
        ▼
Commit or Rollback
        │
        ▼
Execution Context Destroyed
```

### 22. Final Summary

An Apex Execution Context is the temporary runtime environment Salesforce creates whenever Apex code executes. It contains everything required for execution, including variables, objects, heap memory, call stack information, governor limit counters, current user details, security settings, and transaction state. Every user action, trigger execution, API request, Flow invocation, Batch Apex execution, Queueable job, or Scheduled Apex run gets its own isolated execution context. When execution completes, Salesforce commits or rolls back the transaction and destroys the execution context, releasing all memory and resources.
