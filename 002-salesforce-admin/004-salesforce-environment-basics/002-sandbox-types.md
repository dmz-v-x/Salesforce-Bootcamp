## Salesforce Sandbox Types

### 1. What Is a Sandbox?

A Sandbox is a **copy of a Salesforce Production Org** used for:

- Development
- Testing
- Training
- UAT (User Acceptance Testing)
- Integration testing
- Performance testing

without affecting real business users or real business operations.

Think of a Sandbox as a **safe practice copy of Production**.

---

### 2. Why Do Sandboxes Exist?

Imagine a company's Production Org contains:

```text
Customers: 500,000
Leads: 2,000,000
Orders: 1,500,000
Revenue Data
Invoices
Contracts
```

Now imagine a developer wants to:

- Create a Flow
- Modify Apex code
- Change Page Layouts
- Deploy a new feature

Would it be safe to do directly in Production?

No.

A mistake could:

- Delete records
- Break automation
- Cause revenue loss
- Prevent users from working

Therefore Salesforce provides Sandboxes.

---

### 3. Real World Analogy

Imagine constructing a new bridge.

Engineers don't immediately modify the real bridge.

Instead they create:

```text
Blueprint
Prototype
Model
Testing Environment
```

Only after successful testing do they touch the real bridge.

Salesforce follows exactly the same idea.

```text
Production
      ↓
 Sandbox
      ↓
 Development
      ↓
 Testing
      ↓
 Deployment
      ↓
 Production
```

---

### 4. What Actually Gets Copied?

A Sandbox can contain two major things:

#### Metadata

Configuration and application structure.

Examples:

- Objects
- Fields
- Flows
- Validation Rules
- Apex Classes
- Triggers
- Lightning Pages
- Reports
- Dashboards

---

#### Data

Actual records.

Examples:

- Accounts
- Contacts
- Opportunities
- Cases
- Custom Object Records

---

### 5. What Is Metadata?

Metadata means:

The blueprint of your Salesforce application.

Example:

Object:

```text
Student
```

Fields:

```text
Name
Age
Email
```

Validation Rule:

```text
Age > 0
```

Flow:

```text
Send Welcome Email
```

All of this is metadata.

---

### 6. What Is Data?

Data means actual records.

Example:

```text
Student:
Name = John
Age = 20
Email = john@example.com
```

Another record:

```text
Student:
Name = Sarah
Age = 21
Email = sarah@example.com
```

These records are data.

---

### 7. Major Sandbox Types

Salesforce provides four primary sandbox types:

```text
1. Developer Sandbox
2. Developer Pro Sandbox
3. Partial Copy Sandbox
4. Full Sandbox
```

These differ mainly in:

- Storage
- Data availability
- Testing capability
- Refresh frequency
- Cost

---

## Type 1 — Developer Sandbox

### 8. What Is a Developer Sandbox?

Developer Sandbox is the smallest sandbox type.

It contains:

```text
Metadata = YES
Data = NO (except setup/configuration data)
```

It is mainly used by individual developers.

---

### 9. What Gets Copied?

Copied:

- Objects
- Fields
- Apex
- Flows
- Validation Rules
- Page Layouts
- Permission Sets

Not copied:

- Business records
- Accounts
- Contacts
- Opportunities
- Cases

---

### 10. Storage Capacity

Traditionally:

```text
200 MB Data
200 MB Files
```

(Exact limits may vary by Salesforce edition.)

Very small.

Suitable only for development.

---

### 11. Typical Use Cases

#### Apex Development

```text
Write Trigger
Test Trigger
Debug Trigger
```

---

#### Flow Development

```text
Create Flow
Activate Flow
Test Flow
```

---

#### LWC Development

```text
Build Components
Test UI
Debug
```

---

### 12. Advantages

- Fast refresh
- Lightweight
- Easy to manage
- Ideal for developers

---

### 13. Limitations

- Very little storage
- No real business data
- Cannot perform realistic testing

---

## Type 2 — Developer Pro Sandbox

### 14. What Is Developer Pro Sandbox?

Developer Pro Sandbox is similar to Developer Sandbox but provides much larger storage.

Think:

```text
Developer Sandbox
      +
More Storage
      =
Developer Pro Sandbox
```

---

### 15. What Gets Copied?

Copied:

```text
Metadata
```

Not copied:

```text
Business Data
```

Just like Developer Sandbox.

---

### 16. Storage Capacity

Traditionally:

```text
1 GB Data
1 GB Files
```

Much larger than Developer Sandbox.

---

### 17. Why Use It?

Useful when developers need:

- Large test datasets
- Integration testing
- Complex development

without requiring actual production records.

---

### 18. Example

Suppose you're building:

```text
Customer Portal
```

You create:

```text
50,000 Test Customers
```

A normal Developer Sandbox may fill quickly.

Developer Pro handles larger volumes.

---

## Type 3 — Partial Copy Sandbox

### 19. What Is Partial Copy Sandbox?

Partial Copy Sandbox contains:

```text
Metadata
+
Selected Production Data
```

This is the first sandbox type that can contain actual production records.

---

### 20. How Does It Work?

Salesforce uses something called a Sandbox Template.

Template specifies:

```text
Copy Accounts
Copy Contacts
Copy Opportunities
```

or

```text
Copy Cases
Copy Custom Objects
```

Only selected data is copied.

---

### 21. Storage Capacity

Typically:

```text
Up to 5 GB Data
```

(Subject to edition and licensing.)

---

### 22. Example

Production contains:

```text
500,000 Accounts
2,000,000 Contacts
```

You don't need everything.

Template may copy:

```text
10,000 Accounts
20,000 Contacts
```

into Partial Copy Sandbox.

---

### 23. Why Is This Useful?

Because many tests require realistic data.

Examples:

#### Flow Testing

```text
Real Customers
Real Opportunities
```

---

#### UAT

Business users can test features using familiar records.

---

#### Integration Testing

External systems often require realistic datasets.

---

### 24. Advantages

- Realistic testing
- Faster than Full Sandbox
- Lower storage requirements
- Good balance of cost and functionality

---

### 25. Limitations

- Not all production data
- Limited storage
- Not suitable for large-scale performance testing

---

## Type 4 — Full Sandbox

### 26. What Is a Full Sandbox?

Full Sandbox is a complete replica of Production.

It copies:

```text
Metadata
+
All Records
+
All Files
+
Attachments
+
Documents
```

Everything.

---

### 27. Real World View

Production:

```text
Accounts
Contacts
Cases
Opportunities
Files
Flows
Apex
Reports
Dashboards
```

Full Sandbox:

```text
Accounts
Contacts
Cases
Opportunities
Files
Flows
Apex
Reports
Dashboards
```

Almost identical copy.

---

### 28. Why Is It Powerful?

Testing becomes extremely realistic.

Everything behaves exactly like Production.

---

### 29. Typical Uses

#### User Acceptance Testing

Users verify:

```text
Will this feature work in Production?
```

---

#### Regression Testing

Check whether new changes break existing functionality.

---

#### Integration Testing

Validate:

```text
ERP
SAP
External APIs
Middleware
Marketing Platforms
```

---

#### Performance Testing

Measure behavior with:

```text
Millions of Records
```

---

### 30. Advantages

- Most realistic environment
- Complete testing
- Best deployment validation
- Supports large-scale testing

---

### 31. Limitations

- Expensive
- Longer refresh times
- Large storage consumption

---

## Sandbox Refresh

### 32. What Is Refresh?

Refresh means:

```text
Delete Current Sandbox Content
↓
Create Fresh Copy
From Production
```

---

### 33. Why Refresh?

Production changes constantly.

New:

- Objects
- Fields
- Records
- Users
- Configurations

A refresh synchronizes sandbox with production.

---

### 34. Example

Production:

```text
New Field:
Customer Priority
```

Sandbox:

```text
Field Missing
```

Refresh copies latest metadata and data.

---

## Typical Refresh Intervals

### 35. Developer Sandbox

Usually:

```text
1 Day
```

Can be refreshed frequently.

---

### 36. Developer Pro Sandbox

Usually:

```text
1 Day
```

---

### 37. Partial Copy Sandbox

Usually:

```text
5 Days
```

---

### 38. Full Sandbox

Usually:

```text
29 Days
```

Because copying huge amounts of data takes time and resources.

---

## Hands-On Example — Sandbox Lifecycle

### 39. Step 1

Production Org exists.

```text
Production
```

---

### 40. Step 2

Admin creates Developer Sandbox.

```text
Production
    ↓
Developer Sandbox
```

---

### 41. Step 3

Developer builds:

```text
Student Object
Student Flow
Student Trigger
```

---

### 42. Step 4

Changes are tested.

---

### 43. Step 5

Changes move to:

```text
Partial Copy
```

for UAT.

---

### 44. Step 6

Business users test.

---

### 45. Step 7

Changes move to:

```text
Full Sandbox
```

for final validation.

---

### 46. Step 8

Deployment to Production.

```text
Developer Sandbox
      ↓
Partial Copy
      ↓
Full Sandbox
      ↓
Production
```

---

## Enterprise Development Flow

### 47. Typical Large Company Setup

```text
Production
│
├── Full Sandbox
│
├── Partial Copy Sandbox
│
├── Developer Sandbox A
│
├── Developer Sandbox B
│
├── Developer Sandbox C
│
└── Developer Pro Sandbox
```

Each developer works independently while protecting Production.

---

## Sandbox Comparison Table

| Feature | Developer | Developer Pro | Partial Copy | Full |
|----------|----------|----------|----------|----------|
| Metadata | Yes | Yes | Yes | Yes |
| Production Data | No | No | Partial | Full |
| Storage | Small | Medium | Large | Production Sized |
| Development | Excellent | Excellent | Good | Good |
| UAT | Poor | Limited | Excellent | Excellent |
| Integration Testing | Limited | Good | Very Good | Excellent |
| Performance Testing | No | No | Limited | Excellent |
| Refresh Speed | Fast | Fast | Medium | Slow |
| Cost | Lowest | Higher | Higher | Highest |

---

## Final Mental Model

Think of Salesforce Sandbox Types like this:

```text
Developer Sandbox
=
Personal Coding Workspace

Developer Pro Sandbox
=
Large Personal Workspace

Partial Copy Sandbox
=
Realistic Testing Environment

Full Sandbox
=
Complete Production Replica
```

As you move from:

```text
Developer
    ↓
Developer Pro
    ↓
Partial Copy
    ↓
Full
```

you gain:

- More storage
- More production data
- Better testing capability
- Higher realism

which is why enterprise Salesforce teams typically use multiple sandbox types together throughout the development and deployment lifecycle.
