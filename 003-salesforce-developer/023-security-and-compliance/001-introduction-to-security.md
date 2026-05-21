## Security Fundamentals Introduction to Security

### 1. Learning Objective

Before learning Salesforce security features such as:

- Profiles
- Permission Sets
- Role Hierarchy
- Sharing Rules
- Shield Encryption
- MFA
- Audit Trails

we must first understand a much more fundamental question:

**What exactly are we trying to protect?**

Many beginners immediately jump into learning security features.

That is like learning how to use locks, CCTV cameras, alarms, and security guards without understanding:

- What building is being protected?
- What valuable things are inside?
- Who might try to access them?
- Why protecting them matters?

This chapter builds that foundation.

By the end, you will understand:

- What security actually means
- What information is
- What information security is
- Why companies spend millions on security
- Why Salesforce has an entire security architecture

---

### 2. What Is Security?

When people hear the word "security," they often think of:

- Passwords
- OTPs
- Fingerprints
- Security guards
- CCTV cameras

These are examples of security controls.

They are not security itself.

Security is a much broader concept.

A simple definition:

**Security is the practice of protecting valuable assets from unauthorized access, misuse, damage, theft, or destruction.**

Let's break this down.

Suppose you own:

- A house
- A car
- A bank account

These are valuable assets.

You don't want strangers to:

- Enter your house
- Drive your car
- Withdraw your money

So you add protection:

- Locks
- Keys
- Passwords
- PINs
- Security cameras

Those protections are security mechanisms.

The goal is simple:

> Allow authorized people to access something while preventing unauthorized people from accessing it.

This same idea applies to computer systems.

---

### 3. What Is an Asset?

Before discussing information security, we must understand the word asset.

An asset is anything valuable to an individual or organization.

Examples:

Physical assets:

- Building
- Laptop
- Mobile phone
- Server

Digital assets:

- Customer database
- Source code
- Employee records
- Financial reports
- CRM data

Business assets:

- Company reputation
- Intellectual property
- Contracts
- Sales pipeline

In modern companies, information is often more valuable than physical assets.

For example:

A laptop may cost:

```text
₹60,000
```

But the customer database stored inside might be worth:

```text
₹60 Crore
```

Losing the laptop is bad.

Losing the customer data could destroy the business.

---

### 4. What Is Information?

Now we reach one of the most important concepts.

Most people think information means:

- Documents
- Files
- Databases

But information is much broader.

Information is:

**Data that has meaning and value.**

Examples:

A random number:

```text
839274
```

By itself, it means nothing.

Now consider:

```text
Customer ID: 839274
```

Suddenly it has meaning.

It became information.

---

### 5. Examples of Information

A company stores thousands of pieces of information every day.

Customer information:

```text
Name
Email
Phone Number
Address
Purchase History
```

Employee information:

```text
Salary
Performance Reviews
Bank Account Details
Aadhar Number
PAN Number
```

Sales information:

```text
Leads
Accounts
Opportunities
Contracts
Revenue
```

Support information:

```text
Cases
Complaints
Issue History
Resolutions
```

All of this information has value.

And valuable information attracts threats.

---

### 6. Why Information Is Valuable

Imagine you own a company.

Which would hurt more?

Option A:

```text
One office chair gets stolen
```

Option B:

```text
Entire customer database gets stolen
```

Most businesses would choose Option B.

Why?

Because information powers the business.

Without information:

- Sales stops
- Marketing stops
- Support stops
- Operations stop

Information is the fuel of modern organizations.

This is why companies spend enormous amounts of money protecting it.

---

### 7. What Is Information Security?

Now combine everything we learned.

We know:

- Information is valuable
- Valuable things need protection

Therefore:

**Information Security is the practice of protecting information from unauthorized access, modification, disclosure, destruction, or disruption.**

Simplified:

> Information Security means protecting valuable business information.

The goal is to ensure:

- Right people can access information
- Wrong people cannot access information
- Information remains accurate
- Information remains available when needed

---

### 8. Real-World Example — Bank Account

Imagine your bank account.

Information stored by the bank:

```text
Account Number
Balance
Transactions
Personal Details
```

Security ensures:

You can:

```text
View account
Transfer money
Download statements
```

A stranger cannot:

```text
View balance
Transfer money
Modify records
```

If anyone could access everyone's bank account information:

The banking system would collapse.

This is information security in action.

---

### 9. Real-World Example — Hospital

A hospital stores:

```text
Patient Name
Medical Records
Prescriptions
Lab Reports
Diagnosis
```

Question:

Should every hospital employee see every patient's medical history?

No.

A receptionist may need:

```text
Patient Name
Appointment Information
```

But should not need:

```text
Psychiatric Reports
Medical History
Treatment Details
```

Information security ensures each employee only sees information necessary for their job.

---

### 10. Real-World Example — E-Commerce Company

An online shopping company stores:

```text
Customer Information
Orders
Payments
Addresses
Refund Requests
```

Different employees require different access.

Customer Support:

```text
Can see orders
Can see complaints
```

Finance Team:

```text
Can see payments
```

Warehouse Team:

```text
Can see shipping details
```

Not everyone needs access to everything.

Security controls determine who gets access.

---

### 11. Real-World Example — CRM System

Now let's move closer to Salesforce.

Suppose a company uses a CRM.

The CRM contains:

```text
Customers
Leads
Accounts
Opportunities
Cases
Contracts
Revenue Data
```

Question:

Should every employee in the company see every customer record?

Usually no.

Sales representatives should see:

```text
Their customers
Their opportunities
```

Managers may see:

```text
Entire team data
```

HR may not need access to sales opportunities at all.

The CRM contains valuable information.

Therefore the CRM must be secured.

---

### 12. Why Businesses Care About Security

Many beginners think security is only an IT concern.

In reality, security is a business concern.

Businesses care about security because security failures are expensive.

---

### 13. Financial Losses

Imagine hackers steal:

```text
Customer Database
```

Possible consequences:

- Regulatory fines
- Legal settlements
- Compensation payments
- Investigation costs
- Recovery costs

Losses may reach:

```text
Millions of dollars
```

from a single breach.

---

### 14. Loss of Customer Trust

Suppose a company leaks:

```text
Customer Names
Passwords
Credit Card Information
```

Customers may stop trusting the company.

Some consequences:

- Lost customers
- Negative publicity
- Reduced sales
- Brand damage

Trust is difficult to rebuild.

---

### 15. Operational Disruption

Imagine ransomware encrypts company systems.

Employees cannot access:

```text
CRM
Email
Documents
Customer Records
```

Business operations may stop completely.

Even a few hours of downtime can be extremely expensive.

---

### 16. Legal and Compliance Consequences

Many countries have laws protecting personal data.

Examples include:

- GDPR
- HIPAA
- PCI DSS
- Various privacy regulations

Organizations that fail to protect information may face:

- Audits
- Lawsuits
- Regulatory penalties

We will study these later in the compliance section.

---

### 17. Why Salesforce Security Exists

Now let's connect everything directly to Salesforce.

Salesforce stores some of the most valuable information in an organization.

Examples:

```text
Customers
Revenue
Contracts
Opportunities
Cases
Contacts
Employees
Business Processes
```

Without security:

A sales representative could:

```text
See everyone's deals
```

An intern could:

```text
Delete important records
```

A support agent could:

```text
View executive salary information
```

A malicious employee could:

```text
Export all customer data
```

This would be disastrous.

Therefore Salesforce provides a complete security architecture.

Examples include:

- Authentication
- MFA
- Profiles
- Permission Sets
- Role Hierarchy
- Sharing Rules
- Restriction Rules
- Shield Encryption
- Audit Trails
- Event Monitoring

Every one of these features exists for one reason:

**To protect valuable business information.**

---

### 18. A Simple Salesforce Example

Imagine a company with three employees.

Employee 1:

```text
Sales Representative
```

Employee 2:

```text
Sales Manager
```

Employee 3:

```text
HR Manager
```

Question:

Should HR see sales opportunities?

Probably not.

Question:

Should Sales Representative see executive salaries?

Definitely not.

Question:

Should Sales Manager see team opportunities?

Usually yes.

Salesforce security controls make these decisions possible.

The system ensures:

```text
Right User
      +
Right Information
      +
Right Time
      +
Right Permissions
```

while preventing unauthorized access.

---

### 19. Mental Model to Remember

Whenever you study any Salesforce security feature in the future, ask yourself:

1. What information are we protecting?

2. Who should access it?

3. Who should not access it?

4. What could happen if unauthorized access occurs?

5. Which Salesforce feature solves that problem?

This simple framework will help you understand every future security topic.

---

### 20. End-of-Chapter Summary

You should now understand:

- Security means protecting valuable assets
- Information is data that has meaning and value
- Information is often a company's most valuable asset
- Information Security protects information from unauthorized access, modification, disclosure, or destruction
- Businesses depend heavily on information
- Security failures cause financial, legal, operational, and reputational damage
- CRM systems contain highly valuable business information
- Salesforce security exists to protect customer and business data
- Every Salesforce security feature ultimately exists to control access to information
