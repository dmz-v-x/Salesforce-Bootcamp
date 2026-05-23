## Experience Cloud — Complete Understanding from Scratch

### 1. What is Experience Cloud?

Experience Cloud is Salesforce's platform for building external-facing websites, portals, communities, and digital experiences for people outside your organization.

In simple words:

```text
Sales Cloud
     → Used by Sales Employees

Service Cloud
     → Used by Support Employees

Experience Cloud
     → Used by External Users
```

External users can be:

```text
Customers

Partners

Distributors

Dealers

Suppliers

Students

Vendors

Members
```

---

### 2. Why Was Experience Cloud Created?

Think about a company.

Inside the company:

```text
Sales Team

Support Team

Managers

Admins
```

use Salesforce directly.

But what about:

```text
Customers

Partners

Dealers
```

They usually do NOT have direct access to the company's internal Salesforce organization.

Companies still need a way to:

```text
Share Information

Allow Self-Service

Provide Support

Collaborate
```

This is where Experience Cloud comes in.

---

### 3. The Core Idea

Without Experience Cloud:

```text
Customer Calls Support
       ↓
Waits For Agent
       ↓
Gets Answer
```

With Experience Cloud:

```text
Customer Opens Portal
       ↓
Searches Knowledge Article
       ↓
Finds Answer
       ↓
Problem Solved
```

No support agent required.

---

## 4. Real-World Example

Suppose Salesforce itself has customers.

Customer:

```text
ABC Technologies
```

wants to:

```text
View Support Cases

Create New Cases

Track Requests

Read Documentation
```

Instead of emailing support every time,

Salesforce can provide:

```text
Customer Portal
```

built using Experience Cloud.

---

# What Exactly Can We Build?

### 5. Experience Cloud Use Cases

You can build:

```text
Customer Portals

Partner Portals

Dealer Portals

Supplier Portals

Community Sites

Self-Service Portals

Membership Sites

Employee Portals

Learning Portals
```

All using Salesforce data.

---

## Customer Portal Example

### 6. Customer Self-Service Portal

Customer logs in.

Can:

```text
View Cases

Create Cases

Track Cases

Download Documents

View Orders

Access Knowledge Articles
```

without contacting support.

---

### 7. Customer Portal Architecture

```text
Customer
     ↓
Experience Cloud Site
     ↓
Salesforce Data
```

Customer interacts through portal.

Data remains in Salesforce.

---

## Partner Portal Example

### 8. Partner Collaboration

Suppose your company sells products through partners.

Partners need access to:

```text
Leads

Opportunities

Accounts

Sales Material

Reports
```

Experience Cloud can provide a partner portal.

---

### 9. Partner Portal Workflow

```text
Partner Login
       ↓
View Leads
       ↓
Update Opportunities
       ↓
Track Sales
```

All through portal.

---

## Dealer Portal Example

### 10. Automobile Company Example

Car manufacturer has:

```text
Thousands Of Dealers
```

Dealers need:

```text
Vehicle Information

Warranty Information

Order Status

Inventory Data
```

Experience Cloud portal can provide this.

---

## Supplier Portal Example

### 11. Supplier Collaboration

Suppliers can:

```text
Receive Purchase Orders

Submit Updates

Upload Documents

Track Deliveries
```

through Experience Cloud.

---

## Membership Portal Example

### 12. Educational Organization

Students can:

```text
Register

View Courses

Download Material

Track Progress
```

using an Experience Cloud site.

---

# Experience Cloud vs Sales Cloud

### 13. Important Difference

Sales Cloud is for internal sales teams.

Experience Cloud is for external users.

---

### 14. Comparison

| Sales Cloud | Experience Cloud |
|------------|------------|
| Internal Users | External Users |
| Sales Employees | Customers/Partners |
| Lead Management | Portal Access |
| Opportunity Management | Collaboration |
| Revenue Generation | Digital Experiences |
| CRM Operations | External Engagement |

---

### 15. Example

Salesperson:

```text
Uses Sales App
```

Customer:

```text
Uses Experience Cloud Portal
```

Both may access the same Salesforce data.

---

# Experience Cloud vs Service Cloud

### 16. Common Beginner Confusion

Service Cloud:

```text
Support Agent Uses Salesforce
```

Experience Cloud:

```text
Customer Uses Portal
```

---

### 17. Example

Without Experience Cloud:

```text
Customer Calls Agent
```

With Experience Cloud:

```text
Customer Creates Case Himself
```

through portal.

---

### 18. Relationship

Very often:

```text
Experience Cloud
      +
Service Cloud
```

work together.

---

Example:

```text
Customer Portal
      ↓
Create Case
      ↓
Case Stored In Service Cloud
      ↓
Support Agent Resolves Issue
```

---

# Components of Experience Cloud

## 19. Experience Site

Experience Site is the website users access.

Example:

```text
support.company.com
```

or

```text
partners.company.com
```

---

### 20. What Users See

Pages such as:

```text
Home

Cases

Knowledge

Orders

Documents

Profile
```

---

## 21. Experience Builder

Experience Builder is the visual tool used to create portals.

Think of it as:

```text
Website Builder
```

for Salesforce.

---

### 22. What Can Be Customized?

Examples:

```text
Pages

Navigation

Branding

Colors

Layouts

Components
```

without coding.

---

## 23. Templates

Salesforce provides templates.

Examples:

```text
Customer Service

Partner Central

Help Center
```

These accelerate development.

---

## 24. CMS (Content Management)

Experience Cloud can display:

```text
Articles

Images

Videos

Documents

Announcements
```

using Salesforce content management features.

---

# Security in Experience Cloud

### 25. Important Question

If external users access Salesforce data:

```text
How Is Security Maintained?
```

---

### 26. External Users

External users receive:

```text
Separate Login

Separate Permissions

Separate Access Rights
```

---

### 27. Example

Customer A:

```text
Can See Only His Cases
```

Customer B:

```text
Cannot Access Customer A Data
```

Security rules enforce isolation.

---

# Experience Cloud Architecture

### 28. High-Level Architecture

```text
Customer
Partner
Supplier
Dealer
      ↓

Experience Site
      ↓

Experience Cloud
      ↓

Salesforce Data
```

Portal is simply another way to access Salesforce information.

---

### 29. Internal and External View

```text
Salesperson
      ↓
Sales App
      ↓
Salesforce

Customer
      ↓
Experience Portal
      ↓
Salesforce
```

Same platform.

Different interfaces.

Different permissions.

---

# Is Experience Cloud a Screen Like Sales App?

### 30. Important Clarification

No.

Just like:

```text
Sales Cloud ≠ Sales App
```

and

```text
Service Cloud ≠ Service App
```

Similarly:

```text
Experience Cloud ≠ Experience Builder
```

---

### 31. Experience Cloud Is a Product

Experience Cloud includes:

```text
Experience Sites

Experience Builder

Templates

CMS

Authentication

External User Access

Portal Capabilities

Collaboration Features
```

---

### 32. Experience Builder Is Only One Tool

Experience Builder is used to build experiences.

It is NOT the entire Experience Cloud product.

---

# Who Uses Experience Cloud?

### 33. End Users

External users:

```text
Customers

Partners

Dealers

Suppliers
```

use portals daily.

---

### 34. Salesforce Admin

Admin configures:

```text
Sites

Users

Permissions

Pages

Navigation

Branding
```

---

### 35. Salesforce Developer

Developer builds:

```text
Custom Components

LWC

Apex

Integrations

Custom Pages
```

for portals.

---

### 36. Architect

Architect designs:

```text
Security Model

Authentication

Scalability

Data Access

Portal Architecture
```

---

# Practical on Salesforce Free Account

## 37. Goal

Create your first Experience Cloud site.

---

### Step 1: Open Setup

Navigate:

```text
Setup
```

Search:

```text
Digital Experiences
```

or

```text
All Sites
```

---

### Step 2: Enable Digital Experiences

If not enabled:

```text
Enable Digital Experiences
```

Save.

---

### Step 3: Open All Sites

Navigate:

```text
Setup
     ↓
All Sites
```

---

### Step 4: Create New Site

Click:

```text
New
```

Choose template:

```text
Customer Service

Help Center

Partner Central
```

---

### Step 5: Enter Information

Example:

```text
Site Name:
Customer Support Portal
```

Create site.

---

### Step 6: Open Experience Builder

Click:

```text
Builder
```

Observe:

```text
Page Designer

Components

Navigation

Theme Settings
```

---

### Step 7: Customize Homepage

Add:

```text
Text

Image

Knowledge Search
```

Save.

---

### Step 8: Publish Site

Click:

```text
Publish
```

Site becomes available.

---

### Step 9: Create External User (Advanced)

Create a contact.

Enable external user access.

Login through portal.

Observe:

```text
External User Experience
```

---

# Real Enterprise Example

### 38. Salesforce Customer Portal Example

Customer logs into portal.

Can:

```text
Open Support Cases

Track Existing Cases

Read Knowledge Articles

Download Documentation

View Account Information
```

All without contacting support.

---

### 39. Partner Portal Example

Partner logs into portal.

Can:

```text
View Leads

Manage Opportunities

Download Marketing Material

Track Revenue
```

using Experience Cloud.

---

# Experience Cloud Ecosystem Position

### 40. Where Does It Fit?

```text
Sales Cloud
      ↓
Internal Sales Teams

Service Cloud
      ↓
Internal Support Teams

Experience Cloud
      ↓
External Customers And Partners
```

---

### 41. Combined Architecture

```text
Customer
      ↓
Experience Cloud Portal
      ↓
Service Cloud Cases
      ↓
Support Agent

Partner
      ↓
Experience Cloud Portal
      ↓
Sales Cloud Opportunities
      ↓
Sales Team
```

Experience Cloud often acts as the bridge between external users and Salesforce data.

