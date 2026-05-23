## SaaS and Cloud Computing Basics in Context of Salesforce

### 1. Why Do We Need to Learn SaaS and Cloud Computing Before Salesforce?

To understand Salesforce properly, you must first understand:

```text
Cloud Computing
        ↓
SaaS
        ↓
Salesforce
```

Many beginners learn Salesforce objects and features without understanding where Salesforce actually runs.

Salesforce itself is a cloud-based SaaS application.

Therefore SaaS and Cloud Computing are foundation concepts.

---

### 2. What is Cloud Computing?

Cloud Computing means using computing resources over the internet instead of owning and managing them yourself.

These resources can include:

```text
Servers

Storage

Databases

Networking

Applications

Security Services
```

Instead of buying physical infrastructure, companies rent resources from cloud providers.

---

### 3. Traditional Computing (Before Cloud)

Suppose a company wants to build a CRM application.

Before cloud computing they had to buy:

```text
Servers

Hard Drives

Networking Equipment

Power Backup

Cooling Systems

Security Systems
```

Everything was installed inside company premises.

This is called:

```text
On-Premise Infrastructure
```

---

### 4. Traditional Infrastructure Example

```text
Company Office
      ↓

Physical Server Room

      ↓

CRM Application
```

Company is responsible for:

- purchasing hardware
- maintenance
- upgrades
- backups
- security
- disaster recovery

This becomes expensive.

---

### 5. Problems with Traditional Infrastructure

```text
High Cost

Maintenance Effort

Hardware Failures

Scaling Problems

Upgrade Complexity

Security Challenges
```

As businesses grew, these problems became larger.

---

### 6. Cloud Computing Solution

Instead of buying infrastructure:

```text
Company
     ↓
Internet
     ↓
Cloud Provider
```

Cloud provider manages infrastructure.

Company simply uses the resources.

---

### 7. Real-World Example

Think about electricity.

You don't build your own power plant.

You simply use electricity when needed and pay for usage.

Cloud computing works similarly.

```text
Need Computing?
      ↓
Use Cloud Resources
      ↓
Pay For Usage
```

No need to build data centers.

---

## What is a Cloud Provider?

### 8. Cloud Providers

Cloud providers own massive data centers.

They provide computing resources over the internet.

---

### 9. What is a Data Center?

A data center is a building filled with:

```text
Servers

Storage Systems

Networking Devices

Power Systems

Cooling Systems
```

Cloud providers own thousands of servers across the world.

---

### 10. Cloud Computing Architecture

```text
User
 ↓

Internet
 ↓

Cloud Provider Data Center
 ↓

Application
```

Users access applications through browsers or mobile devices.

---

## Main Benefits of Cloud Computing

### 11. No Hardware Purchase

Companies do not need to buy:

```text
Servers

Storage

Networking Equipment
```

Everything already exists in the cloud.

---

### 12. Scalability

Suppose today:

```text
100 Users
```

Tomorrow:

```text
100,000 Users
```

Cloud resources can scale much more easily than on-premise systems.

---

### 13. High Availability

Cloud providers operate multiple data centers.

If one server fails:

```text
Backup Infrastructure Takes Over
```

Applications remain available.

---

### 14. Automatic Updates

Cloud providers perform:

```text
Maintenance

Security Updates

Infrastructure Upgrades
```

Customers do not manage these activities.

---

### 15. Global Access

Users can access applications from:

```text
Office

Home

Mobile Phone

Different Countries
```

As long as internet access exists.

---

## Service Models of Cloud Computing

### 16. Three Main Cloud Models

```text
IaaS

PaaS

SaaS
```

You will encounter these frequently in Salesforce interviews.

---

## IaaS (Infrastructure as a Service)

### 17. What is IaaS?

Cloud provider gives infrastructure.

Customer manages everything else.

Provider gives:

```text
Virtual Machines

Storage

Networking
```

Customer installs:

```text
Operating System

Database

Application
```

---

### 18. Example of IaaS

Example:

```text
AWS EC2

Azure Virtual Machines

Google Compute Engine
```

You create servers and manage them yourself.

---

### 19. Responsibility in IaaS

Customer manages:

```text
Operating System

Patches

Applications

Databases
```

Cloud provider manages:

```text
Physical Hardware

Networking

Data Centers
```

---

## PaaS (Platform as a Service)

### 20. What is PaaS?

Cloud provider gives:

```text
Infrastructure

Operating System

Runtime Environment

Development Platform
```

Developers only focus on application development.

---

### 21. Example of PaaS

Examples:

- AWS Elastic Beanstalk
- Salesforce Heroku
- Google App Engine

Developer builds applications without managing servers.

---

### 22. Salesforce as PaaS

Salesforce provides:

```text
Database

Security

Authentication

Infrastructure

Development Platform
```

Developers create:

```text
Custom Objects

Apex

Flows

Lightning Components
```

without worrying about servers.

This capability is called:

```text
Salesforce Platform
```

---

## SaaS (Software as a Service)

### 23. What is SaaS?

SaaS means complete software delivered through the internet.

Users simply use the software.

They do not manage:

```text
Servers

Databases

Operating Systems

Infrastructure
```

Everything is handled by the provider.

---

### 24. SaaS Example

Examples:

- Google Workspace (Gmail, Docs, Sheets)
- Salesforce CRM
- File Storage & Sharing (Dropbox)
- E-commerce (Shopify)

Users simply log in and use the application.

---

### 25. Salesforce as SaaS

This is the most important concept.

When a company buys Salesforce CRM:

They simply:

```text
Open Browser
      ↓
Login
      ↓
Use CRM
```

They do not install:

```text
Servers

Databases

Operating Systems
```

Everything is already managed by Salesforce.

Therefore Salesforce is a SaaS product.

---

## Understanding Salesforce Through SaaS

### 26. Example Without Salesforce

Suppose company wants CRM.

Traditional approach:

```text
Buy Servers
      ↓
Install CRM Software
      ↓
Install Database
      ↓
Maintain Infrastructure
      ↓
Perform Backups
```

Complex and expensive.

---

### 27. Example With Salesforce

```text
Purchase Salesforce License
          ↓
Create Users
          ↓
Login Through Browser
          ↓
Start Using CRM
```

No infrastructure management.

---

### 28. Why Companies Love SaaS

Benefits:

```text
Fast Setup

Lower Cost

Automatic Upgrades

Security

Accessibility

Scalability
```

Companies focus on business instead of infrastructure.

---

## Multi-Tenant Architecture

### 29. Important Salesforce Concept

Salesforce uses:

```text
Multi-Tenant Architecture
```

This is frequently asked in interviews.

---

### 30. What is Multi-Tenancy?

Multiple customers share the same infrastructure.

Example:

```text
Company A

Company B

Company C
```

All use Salesforce.

But data remains isolated.

Think of it like an apartment building.

```text
Same Building

Different Apartments
```

Shared infrastructure.

Private data.

---

### 31. Benefits of Multi-Tenancy

```text
Lower Cost

Automatic Updates

Better Resource Usage

Easy Scaling
```

This is a major reason Salesforce can serve thousands of organizations efficiently.

---

## How Salesforce Fits Into Cloud Computing

### 32. Salesforce Cloud Stack

From customer perspective:

```text
Salesforce CRM
       ↓
SaaS
       ↓
Salesforce Platform
       ↓
Cloud Infrastructure
       ↓
Data Centers
```

Users normally interact only with the top layer.

---

### 33. What Does a Salesforce Admin Need to Manage?

Admin manages:

```text
Users

Roles

Profiles

Objects

Flows

Reports

Security Configuration
```

Admin does NOT manage:

```text
Servers

Operating Systems

Storage Hardware

Network Equipment
```

Salesforce handles those.

---

### 34. What Does a Salesforce Developer Need to Manage?

Developer manages:

```text
Apex

Lightning Components

Flows

Integrations

Custom Applications
```

Developer does NOT manage:

```text
Server Installation

Database Servers

Operating System Updates
```

Salesforce platform handles them.

---

## Practical on Salesforce Free Account

### 35. Goal

Understand SaaS practically.

---

### Step 1: Open Salesforce Developer Org

Login to your Salesforce Developer Account.

Notice:

```text
No Installation

No Server Setup

No Database Installation
```

Everything already exists.

---

### Step 2: Create Account Record

Navigate:

```text
Accounts
    ↓
New
```

Create:

```text
ABC Technologies
```

Save.

---

### Step 3: Create Contact

Navigate:

```text
Contacts
     ↓
New
```

Create:

```text
Rahul Sharma
```

Save.

---

### Step 4: Observe

You successfully used:

```text
Database

Application

Security

Storage
```

without installing anything.

This is SaaS in action.

---

### Step 5: Open Setup

Navigate:

```text
Setup
```

Observe:

```text
Objects

Users

Security

Automation
```

available immediately.

Again:

```text
No Server Management Required
```

This demonstrates cloud computing and SaaS concepts.

---

## Interview Definitions

### 36. Cloud Computing Definition

Cloud Computing is the delivery of computing resources such as servers, storage, databases, networking, and software over the internet on demand instead of maintaining physical infrastructure.

---

### 37. SaaS Definition

Software as a Service (SaaS) is a cloud computing model in which complete software applications are delivered over the internet and managed entirely by the service provider.

Salesforce CRM is one of the most widely used SaaS applications.
