## Apex in Salesforce — Complete Step-by-Step Explanation

### 1. What Is Apex?

Apex is Salesforce's programming language.

Just as:

- Java applications are written using Java
- Node.js applications are written using JavaScript/TypeScript
- Python applications are written using Python

Salesforce applications are written using **Apex** when custom business logic is required.

In simple words:

> Apex is Salesforce's server-side programming language used to implement custom business logic inside the Salesforce platform.

Salesforce itself is built on a platform that already provides many features without coding:

- Database
- Authentication
- Security
- User management
- Forms
- Reports
- Dashboards
- Automation

However, sometimes business requirements become too complex for clicks-based tools. In those situations, developers write Apex code.

---

### 2. Why Was Apex Created?

Before understanding Apex, let's understand the problem.

Suppose a company wants:

- Whenever an Opportunity closes
- Send data to an external ERP
- Create multiple custom records
- Perform calculations
- Update related records

This logic may be too complex for declarative tools.

Salesforce therefore provides Apex so developers can implement advanced business requirements.

Apex exists to:

- Add custom business logic
- Automate complex processes
- Integrate with external systems
- Process large amounts of data
- Build APIs
- Extend Salesforce capabilities

---

### 3. What Type of Language Is Apex?

Apex is:

- Object-Oriented
- Strongly Typed
- Case-Insensitive (mostly)
- Server-Side
- Multi-Tenant Aware

It looks very similar to Java.

Example:

```apex
public class HelloWorld {

    public static void sayHello() {
        System.debug('Hello World');
    }

}
```

If you know Java, Apex feels very familiar.

Common Java concepts available in Apex:

- Classes
- Objects
- Methods
- Constructors
- Interfaces
- Inheritance
- Polymorphism
- Collections

---

### 4. What Does "Server-Side Language" Mean?

Apex always runs on Salesforce servers.

The code does not execute inside the browser.

Example:

User clicks:

```text
Create Order
```

Browser sends request →

Salesforce server executes Apex →

Database updated →

Response returned to browser.

Flow:

```text
User
 ↓
Browser
 ↓
Salesforce Server
 ↓
Apex Executes
 ↓
Database
 ↓
Response Returned
```

Therefore Apex is backend programming.

---

### 5. What Problems Can Apex Solve?

Apex can:

#### Validate Data

Example:

```text
Loan amount cannot exceed ₹10,00,000
```

Apex can enforce this rule.

---

#### Perform Calculations

Example:

```text
Calculate commission
Calculate tax
Calculate discount
Calculate bonus
```

---

#### Update Related Records

Example:

```text
Opportunity Closed
↓
Automatically update Account
↓
Automatically create Invoice
```

---

#### Integrate External Systems

Example:

```text
Salesforce
     ↔
SAP
     ↔
Oracle
     ↔
Payment Gateway
     ↔
ERP
```

Apex can send and receive data through APIs.

---

#### Create Complex Automation

Example:

```text
Lead Created
↓
Check Lead Score
↓
Assign Territory
↓
Create Follow-Up Task
↓
Send Email
↓
Notify Manager
```

All can be implemented using Apex.

---

### 6. Where Does Apex Live?

Apex code is stored inside Salesforce metadata.

Not inside:

- EC2
- Kubernetes
- VM
- Traditional application server

Instead:

```text
Salesforce Org
 ├── Objects
 ├── Fields
 ├── Flows
 ├── Validation Rules
 ├── Apex Classes
 ├── Apex Triggers
 └── Lightning Components
```

Apex becomes part of the Salesforce organization.

---

### 7. What Is an Apex Class?

An Apex class is a container that contains logic.

Example:

```apex
public class DiscountService {

    public static Decimal calculateDiscount(
        Decimal amount
    ) {
        return amount * 0.10;
    }

}
```

Think of a class as:

```text
Folder
 └── Business Logic
```

Inside classes we write methods.

---

### 8. What Is an Apex Method?

A method performs a task.

Example:

```apex
public static void sendEmail() {

}
```

Method purpose:

```text
Input
 ↓
Processing
 ↓
Output
```

Examples:

- Calculate commission
- Create invoice
- Send email
- Validate customer
- Call external API

---

### 9. What Is an Apex Trigger?

Trigger is code that automatically executes when records change.

Example:

```text
Record Inserted
Record Updated
Record Deleted
```

Trigger automatically runs.

Example:

```text
Opportunity Closed
↓
Automatically Create Invoice
```

Apex Trigger handles this.

---

### 10. Why Do We Need Triggers?

Without triggers:

```text
User must manually execute code
```

With triggers:

```text
Database Event Occurs
↓
Code Runs Automatically
```

Examples:

- New Lead created
- Account updated
- Opportunity closed
- Contact deleted

All can automatically start Apex logic.

---

### 11. What Is SOQL?

SOQL stands for:

**Salesforce Object Query Language**

It is Salesforce's query language.

Similar to SQL.

Example SQL:

```sql
SELECT Name
FROM Customer
```

Equivalent SOQL:

```apex
SELECT Name
FROM Account
```

SOQL allows Apex to retrieve records from Salesforce.

---

### 12. What Is SOSL?

SOSL stands for:

**Salesforce Object Search Language**

Purpose:

Search across multiple objects.

Example:

```text
Search "John"
```

Salesforce searches:

- Account
- Contact
- Lead
- Opportunity

simultaneously.

Think:

```text
SOQL → Query specific object

SOSL → Global search across objects
```

---

### 13. How Apex Interacts with Salesforce Database

Suppose:

```text
Account Record Exists
```

Apex can:

#### Create

```apex
insert accountRecord;
```

---

#### Read

```apex
SELECT Id, Name
FROM Account
```

---

#### Update

```apex
update accountRecord;
```

---

#### Delete

```apex
delete accountRecord;
```

These are called DML operations.

---

### 14. What Is DML?

DML means:

**Data Manipulation Language**

Operations:

- Insert
- Update
- Delete
- Upsert
- Undelete

Example:

```apex
insert account;
update account;
delete account;
```

Used for modifying Salesforce records.

---

### 15. What Is a Governor Limit?

This is one of the most important Apex concepts.

Salesforce is a multi-tenant platform.

Meaning:

Many customers share Salesforce infrastructure.

Example:

```text
Company A
Company B
Company C
Company D
```

All use Salesforce servers.

To prevent one customer from consuming all resources, Salesforce imposes limits.

These limits are called:

**Governor Limits**

Examples:

- Maximum SOQL queries
- Maximum CPU time
- Maximum heap memory
- Maximum DML operations

If code exceeds limits:

```text
Exception Thrown
Transaction Fails
```

---

### 16. Why Are Governor Limits Important?

Imagine:

```text
Developer writes infinite loop
```

Without limits:

```text
Entire Salesforce server affected
```

With governor limits:

```text
Bad code stopped immediately
```

Thus Salesforce remains stable for everyone.

---

### 17. What Is a Transaction?

A transaction is a complete unit of work.

Example:

```text
Create Account
Create Contact
Create Opportunity
```

Either:

```text
All succeed
```

or

```text
All fail
```

This ensures data consistency.

---

### 18. What Is an Apex Execution Flow?

Example:

User clicks:

```text
Convert Lead
```

Flow:

```text
User Action
↓
Trigger Executes
↓
Validation Rules Execute
↓
Flows Execute
↓
Apex Executes
↓
Database Updated
↓
Commit Transaction
```

Salesforce follows a specific execution order.

---

### 19. Where Can Apex Be Used?

Apex can be used in:

#### Triggers

```text
Automatic record processing
```

---

#### Classes

```text
Business logic
```

---

#### REST APIs

```text
Expose custom APIs
```

---

#### Batch Jobs

```text
Large-scale processing
```

---

#### Scheduled Jobs

```text
Run every night
Run every week
Run every month
```

---

#### Queueable Jobs

```text
Background processing
```

---

#### Future Methods

```text
Asynchronous processing
```

---

#### Lightning Components

```text
LWC
↓
Call Apex
↓
Get Data
```

---

### 20. Apex and Lightning Web Components (LWC)

Very common architecture:

```text
LWC (Frontend)
      ↓
Apex Class
      ↓
Salesforce Database
```

Example:

```text
User clicks Search
↓
LWC calls Apex
↓
Apex runs SOQL
↓
Records returned
↓
Displayed in UI
```

This is one of the most common patterns in Salesforce development.

---

### 21. Real-World Example

Suppose an insurance company uses Salesforce.

Requirement:

```text
Whenever Policy Status = Approved
```

System should:

1. Create customer account
2. Create policy record
3. Generate invoice
4. Notify finance team
5. Send email to customer
6. Notify external ERP

This workflow is difficult using only clicks-based tools.

Apex can handle all of it.

Flow:

```text
Policy Approved
      ↓
Apex Trigger
      ↓
Business Logic Class
      ↓
Invoice Creation
      ↓
Email Sending
      ↓
ERP API Call
      ↓
Success
```

---

### 22. Apex vs Flow

| Feature | Flow | Apex |
|----------|----------|----------|
| Coding Required | No | Yes |
| Beginner Friendly | Yes | No |
| Complex Logic | Limited | Excellent |
| Integrations | Basic | Advanced |
| Performance Control | Limited | High |
| Reusability | Moderate | High |
| Testing | Minimal | Required |
| Enterprise Scale | Good | Excellent |

General guideline:

```text
Simple Automation
        ↓
Use Flow

Complex Logic
        ↓
Use Apex
```

---

### 23. Apex Testing

Salesforce requires Apex tests before deployment.

Developers write:

```apex
@isTest
private class AccountTest {

}
```

Purpose:

- Verify logic works
- Prevent bugs
- Ensure deployment quality

Salesforce generally requires:

```text
At least 75% code coverage
```

before deploying Apex to production.

---

### 24. Apex in One Diagram

```text
                Salesforce User
                        │
                        ▼
                  Lightning UI
                        │
                        ▼
                 Apex Controller
                        │
        ┌───────────────┼───────────────┐
        ▼               ▼               ▼
     SOQL          Business Logic      APIs
        ▼               ▼               ▼
   Salesforce DB   Calculations     External Systems
        │               │               │
        └───────────────┼───────────────┘
                        ▼
                     Response
```

### 25. Final Summary

Apex is Salesforce's server-side programming language used to implement custom business logic that cannot be easily achieved using declarative tools such as Flows, Validation Rules, or Approval Processes.

Using Apex, developers can:

- Create custom business logic
- Build automation
- Query Salesforce data using SOQL
- Modify data using DML
- Integrate external systems through APIs
- Create triggers that run automatically on record changes
- Build scalable enterprise applications
- Support Lightning Web Components
- Process large datasets asynchronously
- Implement advanced security and validation logic

In a Salesforce project, Apex is essentially the primary backend programming language used by Salesforce developers.
