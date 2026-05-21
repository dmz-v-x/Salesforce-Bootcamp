## Customer Lifecycle 

### 1. What is Customer Lifecycle?

Customer Lifecycle is the complete journey of a customer from the moment they first show interest in a company until they become a loyal customer and continue doing business with the company.

In simple words:

Customer Lifecycle = Entire journey from Stranger → Customer → Repeat Customer

Every CRM system, including Salesforce, is designed to manage this lifecycle.

---

### 2. Why Should We Learn Customer Lifecycle First?

Before learning:

- Leads
- Accounts
- Contacts
- Opportunities
- Cases
- Sales Cloud
- Service Cloud

you must understand the customer lifecycle because all Salesforce objects exist to support different stages of this lifecycle.

---

### 3. Complete Customer Lifecycle Overview

```text
Unknown Person
       ↓
Marketing Campaign
       ↓
Lead
       ↓
Qualification
       ↓
Lead Conversion
       ↓
Account + Contact + Opportunity
       ↓
Sales Process
       ↓
Closed Won
       ↓
Customer
       ↓
Support & Service
       ↓
Repeat Purchases
       ↓
Loyal Customer
```

---

### 4. Real Company Example

Suppose there is a software company called:

CloudTech Solutions

They sell CRM software to businesses.

A company named:

ABC Technologies

is looking for a CRM solution.

Let's follow the entire lifecycle.

---

## Phase 1: Awareness Stage

### 5. Customer Does Not Know About Us Yet

Initially:

ABC Technologies does not know CloudTech Solutions exists.

In Salesforce there is no record yet.

```text
Salesforce Database

No Lead
No Contact
No Account
No Opportunity
```

The person is still a stranger.

---

### 6. Marketing Creates Awareness

CloudTech runs:

- Facebook Ads
- LinkedIn Ads
- Google Ads
- Email Campaigns
- Webinars

ABC Technologies sees an advertisement.

For the first time they become aware of the company.

```text
Stranger
    ↓
Aware of Company
```

Still no CRM record exists.

---

## Phase 2: Lead Generation Stage

### 7. Customer Shows Interest

A manager from ABC Technologies visits the website.

He fills a form:

```text
Name: Rahul Sharma
Company: ABC Technologies
Email: rahul@abc.com
Phone: 9876543210

Interested In:
CRM Software Demo
```

Now interest is shown.

---

### 8. Salesforce Creates a Lead

The submitted form automatically creates a Lead.

Lead Record:

```text
Lead

Name:
Rahul Sharma

Company:
ABC Technologies

Email:
rahul@abc.com

Status:
Open
```

Now Salesforce starts tracking this potential customer.

---

### 9. Why Lead Exists?

At this stage we do not know:

- Is customer serious?
- Does customer have budget?
- Is customer decision maker?
- Will customer buy?

Therefore we store them as a Lead.

Lead = Potential Customer

Not yet verified.

---

## Phase 3: Lead Qualification Stage

### 10. Sales Representative Reviews Lead

Sales representative receives the lead.

Salesperson calls Rahul.

Questions asked:

```text
What company do you work for?

How many employees?

What CRM are you currently using?

Budget available?

Decision maker?
```

---

### 11. Lead Gets Qualified

Salesperson learns:

```text
Company:
ABC Technologies

Employees:
500

Budget:
Available

Decision Maker:
Yes

Requirement:
Immediate
```

Good lead.

Sales team decides to proceed.

---

### 12. Why Qualification Matters?

Many leads are not real opportunities.

Examples:

```text
Student doing research

Fake submission

No budget

Wrong phone number

No actual requirement
```

Sales team filters these out.

Only qualified leads move forward.

---

## Phase 4: Lead Conversion Stage

### 13. Lead Conversion

Salesperson clicks:

Convert Lead

This is one of the most important actions in Salesforce.

---

### 14. What Happens During Lead Conversion?

One Lead becomes three records.

```text
Lead
 ↓
Converted Into

Account
Contact
Opportunity
```

---

### 15. Account Creation

Account represents:

Business or Organization

Example:

```text
Account

ABC Technologies
```

Account = Company

---

### 16. Contact Creation

Contact represents:

Person working at company

Example:

```text
Contact

Rahul Sharma
```

Contact = Individual Person

---

### 17. Opportunity Creation

Opportunity represents:

Potential Sales Deal

Example:

```text
Opportunity

CRM Implementation Project

Value:
₹10,00,000
```

Opportunity = Money-making deal

---

## Phase 5: Sales Process Stage

### 18. Opportunity Moves Through Stages

Sales team starts working on opportunity.

Typical stages:

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

### 19. Needs Analysis

Salesperson understands requirements.

Example:

```text
Need:
CRM for 500 employees

Modules:
Sales
Support
Reports
Automation
```

Opportunity progresses.

---

### 20. Proposal Stage

Company sends quotation.

Example:

```text
Software License:
₹8,00,000

Implementation:
₹2,00,000

Total:
₹10,00,000
```

Proposal sent.

---

### 21. Negotiation Stage

Customer negotiates.

Example:

```text
Need discount

Need additional training

Need extra support
```

Discussion continues.

---

## Phase 6: Deal Closure Stage

### 22. Closed Won

Customer accepts proposal.

Contract signed.

Opportunity status:

```text
Closed Won
```

This means:

Sale completed successfully.

Revenue generated.

---

### 23. Customer Is Now Official Customer

Before:

```text
Lead
```

Now:

```text
Customer
```

Company begins using product.

---

## Phase 7: Service & Support Stage

### 24. Customer Faces Issue

Suppose customer reports:

```text
Unable to access reports
```

Support ticket created.

In Salesforce Service Cloud this becomes:

Case

---

### 25. Case Management

Support team handles issue.

```text
Case Created
      ↓
Assigned
      ↓
Investigated
      ↓
Resolved
      ↓
Closed
```

Customer receives support.

---

### 26. Why Service Is Important?

Bad support causes:

- customer dissatisfaction
- contract cancellation
- negative reviews

Good support increases retention.

---

## Phase 8: Customer Retention Stage

### 27. Building Long-Term Relationship

Company continues:

- support
- training
- account management
- product updates

Customer remains happy.

---

### 28. Upselling

Company offers more products.

Example:

Customer currently uses:

```text
Sales Cloud
```

Company offers:

```text
Service Cloud
Marketing Cloud
Analytics
```

Customer purchases more products.

Revenue increases.

---

### 29. Renewal

Subscription expires after one year.

Sales team contacts customer.

Customer renews contract.

Relationship continues.

---

## Phase 9: Loyal Customer Stage

### 30. Loyal Customer

Customer is satisfied.

Benefits:

- renews contracts
- buys more products
- refers other customers
- gives positive feedback

Lifecycle reaches maturity.

---

## Complete Demo Timeline

### 31. End-to-End Example

```text
Rahul sees advertisement
           ↓
Visits website
           ↓
Submits form
           ↓
Lead Created
           ↓
Sales Call
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
Proposal Sent
           ↓
Negotiation
           ↓
Closed Won
           ↓
Customer Created
           ↓
Support Cases
           ↓
Renewal
           ↓
Upsell
           ↓
Loyal Customer
```

---

## Salesforce Free Account Practical

### 32. Goal

Simulate complete customer lifecycle yourself.

---

### Step 1: Open Sales App

```text
App Launcher
    ↓
Sales
```

---

### Step 2: Create Lead

Navigate:

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

Email:
rahul@abc.com
```

Save.

---

### Step 3: Qualify Lead

Pretend:

```text
Budget Available
Requirement Exists
Decision Maker
```

Lead is qualified.

---

### Step 4: Convert Lead

Open Lead.

Click:

```text
Convert
```

Observe Salesforce creates:

```text
Account
Contact
Opportunity
```

automatically.

---

### Step 5: Open Opportunity

Update stages one by one:

```text
Prospecting

Qualification

Proposal

Negotiation
```

Save after each change.

---

### Step 6: Mark Closed Won

Final stage:

```text
Closed Won
```

Save.

You have completed a sale.

---

### Step 7: Create Support Case (Optional)

If Cases tab exists:

```text
Cases
   ↓
New
```

Create:

```text
Issue:
Unable to Login
```

Save.

This simulates customer support.

---

### Step 8: Review All Records

Observe:

```text
Lead
↓
Account
↓
Contact
↓
Opportunity
↓
Case
```

This is the actual customer lifecycle managed by Salesforce.
