## Multi-Tenant Architecture in Salesforce

### 1. Why This Topic Is Important?

Before learning:

- Salesforce Objects
- Apex
- Flows
- Security
- Governor Limits

you must understand one fundamental concept:

```text
Multi-Tenant Architecture
```

Because almost every design decision in Salesforce comes from this architecture.

For example:

```text
Governor Limits

Shared Resources

Platform Limits

Metadata Architecture

Automatic Upgrades
```

all exist because Salesforce is multi-tenant.

---

### 2. First Understand What a Tenant Means

A tenant means:

```text
A customer using a software system
```

Example:

```text
Infosys

TCS

Wipro

Accenture
```

If all four companies use Salesforce:

```text
Infosys = Tenant

TCS = Tenant

Wipro = Tenant

Accenture = Tenant
```

Each organization is called a tenant.

---

### 3. What is Single-Tenant Architecture?

Let's first understand the easier model.

Imagine a company purchases software and infrastructure exclusively for itself.

Architecture:

```text
Company A
     ↓
Dedicated Server
     ↓
Dedicated Database
     ↓
Dedicated Application
```

No other customer uses those resources.

This is called:

```text
Single-Tenant Architecture
```

---

### 4. Apartment vs Independent House Analogy

Single Tenant:

```text
Independent House

Entire Property Belongs To One Family
```

Resources:

```text
Kitchen

Water

Electricity

Parking
```

are not shared.

Everything belongs to one owner.

---

### 5. Single-Tenant Example

Suppose Infosys builds its own CRM.

Architecture:

```text
Infosys CRM Server

Infosys Database

Infosys Application
```

No resource sharing exists.

---

### 6. Problems with Single-Tenant Systems

If every customer requires:

```text
Dedicated Hardware

Dedicated Database

Dedicated Maintenance Team

Dedicated Upgrades
```

cost becomes very high.

Managing thousands of customers becomes difficult.

---

## What is Multi-Tenant Architecture?

### 7. Definition

Multi-Tenant Architecture means:

```text
Multiple Customers
        ↓
Share Same Infrastructure
        ↓
But Data Remains Isolated
```

This is exactly how Salesforce operates.

---

### 8. Apartment Building Analogy

Imagine:

```text
One Apartment Building
```

contains:

```text
Apartment 101

Apartment 102

Apartment 103

Apartment 104
```

All residents share:

```text
Building Structure

Water Supply

Electricity Infrastructure

Security

Elevators
```

But each apartment has private:

```text
Furniture

Documents

Personal Belongings
```

This is multi-tenancy.

Shared infrastructure.

Private data.

---

### 9. Salesforce Multi-Tenant Model

Imagine:

```text
Infosys Org

TCS Org

Wipro Org

Accenture Org
```

All use Salesforce.

Internally:

```text
Same Salesforce Infrastructure
```

But:

```text
Infosys cannot access TCS data

TCS cannot access Wipro data
```

Data remains isolated.

---

### 10. High-Level Salesforce Architecture

```text
Tenant A
Tenant B
Tenant C
Tenant D
      ↓
Salesforce Platform
      ↓
Shared Infrastructure
      ↓
Shared Database Layer
      ↓
Data Centers
```

Multiple customers use the same platform.

---

## How Salesforce Keeps Data Separate?

### 11. The Big Question

If everyone shares the same platform:

```text
How does Salesforce know which record belongs to which company?
```

Answer:

Every record is associated with an Organization (Org).

---

### 12. What is an Org?

An Org means:

```text
A Salesforce Environment
belonging to a customer
```

Example:

```text
Infosys Org

TCS Org

Wipro Org
```

Each customer receives its own Org.

---

### 13. Record Ownership Concept

Imagine database contains:

```text
Account:
ABC Technologies

Owner:
Infosys Org
```

Another record:

```text
Account:
XYZ Corp

Owner:
TCS Org
```

Salesforce always knows:

```text
Which Org Owns Which Data
```

Therefore isolation is maintained.

---

## Metadata Driven Architecture

### 14. Another Important Concept

Salesforce does not create separate software copies for every customer.

Instead it uses:

```text
Metadata
```

to customize behavior.

---

### 15. Example

Infosys creates:

```text
Custom Object:
Project
```

TCS creates:

```text
Custom Object:
Employee Skill
```

Both customizations exist.

But Salesforce does not create two separate CRM applications.

Instead metadata defines:

```text
How Each Org Behaves
```

---

### 16. Why Metadata Is Powerful?

Because Salesforce can support:

```text
Thousands Of Organizations
```

using:

```text
Single Platform

Single Code Base
```

while allowing customization.

---

## Why Governor Limits Exist?

### 17. Imagine No Limits

Suppose one company executes:

```text
1 Billion Database Queries
```

What happens?

Shared infrastructure becomes overloaded.

Other customers suffer.

---

### 18. Therefore Salesforce Introduces Governor Limits

Governor Limits protect shared resources.

Example:

```text
SOQL Limits

CPU Limits

Heap Limits

DML Limits
```

Purpose:

```text
Prevent One Tenant
From Consuming Everything
```

---

### 19. Real-Life Analogy

Apartment Building:

```text
Unlimited Water Usage
```

One apartment consumes everything.

Other apartments get nothing.

Solution:

```text
Usage Limits
```

Salesforce governor limits work similarly.

---

## Benefits of Multi-Tenant Architecture

### 20. Lower Cost

Infrastructure is shared.

Result:

```text
Lower Customer Cost
```

---

### 21. Automatic Upgrades

Salesforce upgrades platform.

Every customer automatically benefits.

Example:

```text
New Features

Security Fixes

Performance Improvements
```

No manual installation required.

---

### 22. Easy Scalability

Salesforce manages infrastructure growth.

Customer simply adds:

```text
Users

Records

Applications
```

without purchasing servers.

---

### 23. Better Maintenance

Customer focuses on:

```text
Business Logic

CRM Configuration

Automation
```

Salesforce manages:

```text
Infrastructure

Databases

Operating Systems
```

---

# Now Compare Salesforce with AWS

This is where many beginners get confused.

---

## 24. Is AWS Multi-Tenant?

Answer:

```text
Depends On How You Design It
```

AWS is not inherently multi-tenant like Salesforce.

AWS provides infrastructure.

You decide architecture.

---

## Salesforce vs AWS Core Difference

### 25. Salesforce

Salesforce provides:

```text
Ready CRM Platform
```

You simply configure and customize.

---

### 26. AWS

AWS provides:

```text
Infrastructure Building Blocks
```

You build applications yourself.

---

## Salesforce Architecture

### 27. Salesforce Layer

```text
Customer
     ↓
Salesforce CRM
     ↓
Salesforce Platform
     ↓
Shared Infrastructure
```

Salesforce manages everything below CRM.

---

## AWS Architecture

### 28. AWS Layer

```text
Customer
     ↓
Application
     ↓
Database
     ↓
Server
     ↓
Networking
     ↓
AWS Infrastructure
```

You manage many layers yourself.

---

## Example: Building CRM in AWS

### 29. What You Need

To build Salesforce-like CRM on AWS:

You must create:

```text
Frontend

Backend

Database

Authentication

Authorization

Monitoring

Logging

Backups

Deployment Pipeline
```

Everything.

---

### 30. Example AWS Architecture

```text
Users
   ↓

CloudFront
   ↓

Load Balancer
   ↓

EC2 / ECS
   ↓

Application
   ↓

RDS Database
   ↓

S3 Storage
```

You design and manage all of this.

---

## Multi-Tenancy in AWS

### 31. Can AWS Support Multi-Tenancy?

Yes.

But you must build it yourself.

Example:

```text
Tenant ID
```

added to tables.

Example:

```sql
customers
-----------
id
tenant_id
name
```

---

### 32. Data Isolation Example

Table:

```text
customer

id | tenant_id | name

1  | INFOSYS   | ABC

2  | TCS       | XYZ
```

Application code must ensure:

```text
Infosys only sees INFOSYS records

TCS only sees TCS records
```

You are responsible.

---

### 33. Salesforce Does This Automatically

Salesforce automatically provides:

```text
Org Isolation

Security

Authentication

Sharing

Role Hierarchy
```

Built into platform.

---

## Advanced Comparison

### 34. Infrastructure Ownership

| Area | Salesforce | AWS |
|----------|----------|----------|
| Servers | Salesforce | Customer |
| Database Management | Salesforce | Customer |
| CRM Features | Built-In | Must Build |
| Security Framework | Built-In | Must Configure |
| Multi-Tenancy | Native | Must Design |
| Upgrades | Automatic | Customer Responsible |
| Scaling | Automatic | Customer Configures |
| Governor Limits | Built-In | Customer Designs Controls |

---

### 35. Developer Perspective

Salesforce Developer focuses on:

```text
Business Logic

Apex

Flows

Lightning Components

Integrations
```

---

AWS Full Stack Developer focuses on:

```text
Infrastructure

Backend

Frontend

Database

Networking

Deployment

Monitoring
```

Much broader responsibility.

---

### 36. Enterprise Analogy

Salesforce:

```text
Rent Fully Furnished Office
```

Everything already exists.

You start working immediately.

---

AWS:

```text
Buy Empty Land
```

Then build:

```text
Building

Rooms

Furniture

Security

Electricity
```

More flexibility.

More responsibility.

---

## Salesforce Free Account Practical

### 37. Goal

Experience Multi-Tenant Architecture Practically.

---

### Step 1: Open Salesforce Developer Org

Login.

Observe:

```text
No Server Setup

No Database Setup

No Infrastructure Setup
```

Everything already exists.

---

### Step 2: Create Custom Object

Navigate:

```text
Setup
   ↓
Object Manager
   ↓
Create Custom Object
```

Create:

```text
Project
```

Save.

---

### Step 3: Create Records

Add several Project records.

Observe:

```text
Instant Database Storage
```

No database creation required.

---

### Step 4: Create Another Developer Org (Optional)

Create a second Salesforce Developer Org using another email.

Notice:

```text
Same Salesforce Platform

Different Org

Different Data
```

This demonstrates multi-tenancy.

---

### Step 5: Explore Sharing Settings

Navigate:

```text
Setup
   ↓
Sharing Settings
```

Observe built-in mechanisms for:

```text
Record Security

Ownership

Visibility
```

These are part of Salesforce's multi-tenant architecture.

---

## Interview Definition

### 38. Interview Answer

Multi-Tenant Architecture is a software architecture in which multiple customers (tenants) share the same application and infrastructure while maintaining complete logical separation and security of their data. Salesforce uses a metadata-driven multi-tenant architecture where all organizations share the same platform and infrastructure, while data isolation, security, customization, and scalability are handled automatically by the platform.
