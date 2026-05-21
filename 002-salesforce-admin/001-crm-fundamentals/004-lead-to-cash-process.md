## Lead to Cash Process in Salesforce

### 1. What is Lead to Cash?

Lead to Cash (L2C) is the complete business process that starts when a potential customer first shows interest in a company's product or service and ends when the company receives payment from that customer.

In simple words:

```text
Potential Customer
        ↓
Lead
        ↓
Opportunity
        ↓
Quote
        ↓
Order
        ↓
Invoice
        ↓
Payment Received
        ↓
Cash
```

That is why it is called:

```text
Lead → Cash
```

The goal of the entire sales organization is to convert leads into actual revenue.

---

### 2. Why Do Companies Follow Lead to Cash Process?

Without a structured process:

- leads get lost
- sales opportunities are missed
- quotes are inconsistent
- orders are not tracked properly
- invoices are delayed
- payments are missed

Lead to Cash creates a standard process that every employee follows.

Benefits:

- better sales tracking
- faster deal closure
- accurate billing
- improved customer experience
- predictable revenue

---

### 3. Complete Lead to Cash Flow

```text
Lead
 ↓
Lead Qualification
 ↓
Lead Conversion
 ↓
Account
 ↓
Contact
 ↓
Opportunity
 ↓
Quote
 ↓
Negotiation
 ↓
Closed Won
 ↓
Order
 ↓
Invoice
 ↓
Payment
 ↓
Cash Received
```

Let's understand every stage in detail.

---

## Example Scenario

### 4. Company Example

Suppose there is a company:

```text
CloudTech Solutions
```

They sell CRM software.

A company named:

```text
ABC Technologies
```

needs CRM software for 500 employees.

We will follow this customer through the complete Lead to Cash journey.

---

## Stage 1: Lead Creation

### 5. Customer Shows Interest

Rahul Sharma from ABC Technologies visits CloudTech's website.

He fills a form:

```text
Name:
Rahul Sharma

Company:
ABC Technologies

Requirement:
CRM Software

Email:
rahul@abc.com
```

At this moment Salesforce creates:

```text
Lead
```

---

### 6. What is a Lead?

Lead represents:

```text
Potential Customer
```

The company knows someone is interested.

But it does not yet know:

- budget
- seriousness
- authority to purchase
- timeline

Therefore they remain a Lead.

---

## Stage 2: Lead Qualification

### 7. Sales Representative Contacts Lead

Salesperson calls Rahul.

Questions asked:

```text
What problem are you solving?

How many users?

Budget available?

Decision maker?

Implementation timeline?
```

---

### 8. Lead Qualification Result

Salesperson discovers:

```text
Company:
ABC Technologies

Users:
500

Budget:
₹10,00,000

Timeline:
Immediate

Decision Maker:
Yes
```

Lead is qualified.

---

### 9. Why Qualification Is Important?

Not every lead becomes a customer.

Examples of unqualified leads:

```text
Student researching

No budget

Fake information

Competitor inquiry

No actual requirement
```

Qualification prevents wasting sales effort.

---

## Stage 3: Lead Conversion

### 10. Lead Conversion

Salesperson clicks:

```text
Convert Lead
```

---

### 11. What Salesforce Creates

During conversion Salesforce creates:

```text
Account
Contact
Opportunity
```

---

### 12. Account

Account represents:

```text
ABC Technologies
```

Account = Company or Organization.

---

### 13. Contact

Contact represents:

```text
Rahul Sharma
```

Contact = Person working for company.

---

### 14. Opportunity

Opportunity represents:

```text
Potential Deal
```

Example:

```text
CRM Software Implementation

Value:
₹10,00,000
```

This is where sales activities are tracked.

---

## Stage 4: Opportunity Management

### 15. Opportunity Stages

The opportunity moves through various stages.

Example:

```text
Prospecting
 ↓
Qualification
 ↓
Needs Analysis
 ↓
Proposal
 ↓
Negotiation
 ↓
Closed Won
```

---

### 16. Needs Analysis

Sales team understands requirements.

Example:

```text
500 Users

Sales Management

Customer Support

Automation

Dashboards
```

Requirements are documented.

---

## Stage 5: Quote Creation

### 17. What is a Quote?

A Quote is a formal pricing document sent to the customer.

Example:

```text
CRM License:
₹8,00,000

Implementation:
₹1,50,000

Training:
₹50,000

Total:
₹10,00,000
```

---

### 18. Why Quotes Are Needed?

Customer wants:

- pricing
- products
- services
- terms and conditions

Quote provides all this information.

---

### 19. Salesforce Quote Process

Inside Salesforce:

```text
Opportunity
     ↓
Create Quote
```

Sales team generates official pricing.

---

## Stage 6: Negotiation

### 20. Customer Reviews Quote

Customer may ask:

```text
Need discount

Need extra support

Need longer contract

Need additional training
```

Negotiation begins.

---

### 21. Sales Team Updates Quote

Example:

Original:

```text
₹10,00,000
```

Negotiated:

```text
₹9,50,000
```

Updated quote is shared again.

---

## Stage 7: Deal Closure

### 22. Customer Accepts Proposal

Customer agrees.

Contract signed.

Opportunity status becomes:

```text
Closed Won
```

---

### 23. Meaning of Closed Won

It means:

```text
Customer agreed to purchase
```

Revenue is expected.

However cash has not yet been received.

This is a very important distinction.

---

## Stage 8: Order Management

### 24. What is an Order?

Order represents what customer officially purchased.

Example:

```text
500 CRM Licenses

Implementation Services

Training Package
```

---

### 25. Why Order Exists?

Quote shows:

```text
What customer may buy
```

Order shows:

```text
What customer actually purchased
```

---

### 26. Example Order

```text
Order Number:
ORD-1001

Customer:
ABC Technologies

Products:
500 Licenses

Amount:
₹9,50,000
```

---

## Stage 9: Invoice Generation

### 27. What is an Invoice?

Invoice is the bill sent to customer.

Example:

```text
Invoice Number:
INV-1001

Amount:
₹9,50,000

Due Date:
30 Days
```

---

### 28. Purpose of Invoice

Invoice requests payment from customer.

Without invoice:

Company cannot officially collect money.

---

## Stage 10: Payment Collection

### 29. Customer Makes Payment

Customer transfers money.

Example:

```text
Bank Transfer

Amount:
₹9,50,000
```

Payment received successfully.

---

### 30. Cash Is Received

Now company has actual revenue.

Lead-to-Cash process is complete.

```text
Lead
 ↓
Opportunity
 ↓
Quote
 ↓
Order
 ↓
Invoice
 ↓
Payment
 ↓
Cash
```

---

## Complete End-to-End Example

### 31. Complete Timeline

```text
Rahul visits website
          ↓
Lead Created
          ↓
Lead Qualified
          ↓
Lead Converted
          ↓
Account Created
          ↓
Contact Created
          ↓
Opportunity Created
          ↓
Needs Analysis
          ↓
Quote Sent
          ↓
Negotiation
          ↓
Closed Won
          ↓
Order Created
          ↓
Invoice Generated
          ↓
Customer Pays
          ↓
Cash Received
```

---

## Salesforce Objects Used in Lead to Cash

### 32. Important Objects

| Salesforce Object | Purpose |
|----------|----------|
| Lead | Potential customer |
| Account | Company |
| Contact | Person |
| Opportunity | Potential sale |
| Product | Item being sold |
| Price Book | Product pricing |
| Quote | Proposed pricing |
| Order | Confirmed purchase |
| Contract | Legal agreement |
| Asset | Purchased product |
| Invoice* | Billing document |
| Payment* | Money received |

\* Invoice and Payment are often handled through ERP systems such as SAP, Oracle, NetSuite, or specialized billing applications integrated with Salesforce.

---

## Where Salesforce Ends and ERP Begins

### 33. Real Enterprise Architecture

In many companies:

Salesforce handles:

```text
Lead Management

Opportunity Management

Quotes

Customer Relationship
```

ERP systems handle:

```text
Orders

Inventory

Invoices

Payments

Accounting
```

Example architecture:

```text
Salesforce
     ↓
SAP / Oracle ERP
     ↓
Invoice
     ↓
Payment
     ↓
Accounting
```

---

## Salesforce Free Account Practical

### 34. Goal

Simulate Lead-to-Cash up to the Opportunity stage.

Developer Org does not provide a full enterprise billing system, but you can practice most sales activities.

---

### Step 1: Open Sales App

```text
App Launcher
    ↓
Sales
```

---

### Step 2: Create Lead

```text
Leads
   ↓
New
```

Create:

```text
Name:
Rahul Sharma

Company:
ABC Technologies
```

Save.

---

### Step 3: Convert Lead

Open Lead.

Click:

```text
Convert
```

Observe:

```text
Account Created

Contact Created

Opportunity Created
```

---

### Step 4: Open Opportunity

Navigate:

```text
Opportunities
```

Open the newly created opportunity.

---

### Step 5: Update Stages

Move through:

```text
Prospecting

Qualification

Needs Analysis

Proposal

Negotiation
```

Save after each stage.

---

### Step 6: Mark Closed Won

Set:

```text
Stage = Closed Won
```

Save.

You have simulated a successful sale.

---

### Step 7: Enable Products and Quotes (Optional Advanced Exercise)

Using Setup:

```text
Setup
 ↓
Quote Settings
 ↓
Enable Quotes
```

Then:

```text
Create Product
 ↓
Create Price Book
 ↓
Add Product To Opportunity
 ↓
Generate Quote
```

This gives hands-on experience with the quote portion of the Lead-to-Cash process.
