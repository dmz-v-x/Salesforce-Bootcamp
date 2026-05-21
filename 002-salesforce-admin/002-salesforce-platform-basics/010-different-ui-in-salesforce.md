## Different User Interfaces in Salesforce: Setup, Service Setup, Developer Console, Salesforce Go, and More

### 1. Why Does Salesforce Have So Many Different Interfaces?

When beginners open Salesforce, they often see many different menus and interfaces:

```text
Setup

Service Setup

Developer Console

App Launcher

Sales App

Service App

Object Manager

Flow Builder

Salesforce Go

AppExchange

Reports

Dashboards
```

and wonder:

```text
Why are there so many UIs?

Who uses them?

Admin?

Developer?

Support Agent?

Salesperson?

Architect?
```

The answer is:

Each UI is designed for a different type of work.

Think of Salesforce as a city.

Different people need different workplaces:

```text
Salesperson → Sales Office

Support Agent → Support Desk

Admin → Administration Office

Developer → Development Workspace

Manager → Reporting Room
```

Salesforce provides separate interfaces for each purpose.

---

## Big Picture Architecture

### 2. Salesforce Interfaces Overview

```text
Salesforce Org
      │
      ├── End User Apps
      │      ├── Sales App
      │      ├── Service App
      │      └── Custom Apps
      │
      ├── Administration
      │      ├── Setup
      │      ├── Service Setup
      │      └── Object Manager
      │
      ├── Development
      │      ├── Developer Console
      │      ├── VS Code + Salesforce CLI
      │      └── Dev Tools
      │
      ├── Automation
      │      └── Flow Builder
      │
      ├── Analytics
      │      ├── Reports
      │      └── Dashboards
      │
      └── Extensions
             ├── AppExchange
             └── Salesforce Go
```

---

# Part 1: App Launcher

### 3. What is App Launcher?

The App Launcher is the entry point into Salesforce applications.

Icon:

```text
9 Dots Grid Icon
```

located in the top-left corner.

---

### 4. Purpose of App Launcher

Used to switch between applications.

Examples:

```text
Sales

Service

Marketing

Custom Apps

Analytics Apps
```

Think of it like:

```text
Windows Start Menu
```

for Salesforce.

---

### 5. Who Uses It?

| Role | Uses App Launcher? |
|--------|--------|
| Salesperson | Yes |
| Support Agent | Yes |
| Admin | Yes |
| Developer | Yes |
| Architect | Yes |

Everyone uses it.

---

### 6. Practical

Open:

```text
App Launcher
```

Search:

```text
Sales

Service
```

Switch between apps.

---

# Part 2: Sales App

### 7. What is Sales App?

Sales App is the workspace used by sales teams.

Primary objects:

```text
Leads

Accounts

Contacts

Opportunities

Tasks

Campaigns
```

---

### 8. Typical Salesperson Activities

```text
Create Lead

Call Customer

Update Opportunity

Track Pipeline

Close Deals
```

All performed inside Sales App.

---

### 9. Who Uses Sales App?

Mostly:

```text
Sales Representatives

Account Executives

Sales Managers
```

Sometimes admins and developers use it for testing.

---

### 10. Practical

Open:

```text
Sales App
```

Explore:

```text
Leads

Accounts

Contacts

Opportunities
```

---

# Part 3: Service App

### 11. What is Service App?

Service App is designed for customer support teams.

Primary objects:

```text
Cases

Accounts

Contacts

Knowledge

Tasks
```

---

### 12. Purpose

Used to manage customer issues.

Example:

```text
Customer Complaint
      ↓
Case Created
      ↓
Assigned
      ↓
Resolved
```

---

### 13. Who Uses It?

Mostly:

```text
Support Agents

Service Managers

Customer Success Teams
```

---

### 14. Practical

Open:

```text
Service App
```

Observe:

```text
Cases

Knowledge

Contacts
```

---

# Part 4: Setup

### 15. What is Setup?

Setup is the administrative control center of Salesforce.

Think of it as:

```text
Control Room
```

for the entire organization.

---

### 16. What Can Be Managed in Setup?

Examples:

```text
Users

Profiles

Permission Sets

Objects

Fields

Security

Flows

Reports

Roles

Sharing Settings
```

Almost every configuration starts here.

---

### 17. Who Uses Setup?

Mostly:

```text
Salesforce Administrators

Salesforce Developers

Architects
```

Normal users rarely access Setup.

---

### 18. Most Important Areas Inside Setup

```text
Object Manager

Users

Profiles

Permission Sets

Flow

Apex Classes

Custom Metadata

Named Credentials
```

You will spend a huge amount of time here.

---

### 19. Practical

Open:

```text
Setup
```

Search:

```text
Users

Flow

Object Manager
```

Explore navigation.

---

# Part 5: Service Setup

### 20. What is Service Setup?

Service Setup is a guided configuration area specifically for Service Cloud.

Instead of manually configuring dozens of service features, Salesforce provides a simplified setup wizard.

---

### 21. Example Features Configured Here

```text
Case Management

Email-to-Case

Knowledge

Omni-Channel

Support Queues

Service Console
```

---

### 22. Why Service Setup Exists?

Without it:

Admin would need to configure many settings manually.

Service Setup provides:

```text
Guided Configuration
```

---

### 23. Who Uses Service Setup?

Mostly:

```text
Salesforce Admins

Service Cloud Consultants

Solution Architects
```

Not used by support agents.

---

### 24. Practical

Open:

```text
Service Setup
```

Observe setup guides for:

```text
Cases

Knowledge

Email-To-Case
```

---

# Part 6: Object Manager

### 25. What is Object Manager?

Object Manager is where admins and developers manage objects.

Examples:

```text
Account

Contact

Lead

Case

Custom Objects
```

---

### 26. What Can Be Done Here?

Manage:

```text
Fields

Relationships

Validation Rules

Page Layouts

Record Types

Buttons

Triggers
```

---

### 27. Who Uses Object Manager?

```text
Admins

Developers

Architects
```

Frequently.

---

### 28. Practical

Navigate:

```text
Setup
    ↓
Object Manager
```

Open:

```text
Account
```

Observe all configuration sections.

---

# Part 7: Flow Builder

### 29. What is Flow Builder?

Flow Builder is Salesforce's automation tool.

Used to automate business processes.

---

### 30. Example

```text
Lead Created
      ↓
Assign Owner
      ↓
Create Task
      ↓
Send Email
```

Automatically.

---

### 31. Who Uses Flow Builder?

Mostly:

```text
Admins

Developers

Consultants
```

---

### 32. Practical

Navigate:

```text
Setup
   ↓
Flows
```

Create a simple flow.

---

# Part 8: Developer Console

### 33. What is Developer Console?

Developer Console is a browser-based development tool.

Used mainly for:

```text
Writing Apex

Executing Code

Debugging

Viewing Logs

Testing SOQL
```

---

### 34. Example Uses

Run Apex:

```java
System.debug('Hello World');
```

Query records:

```sql
SELECT Name FROM Account
```

View debug logs.

---

### 35. Who Uses Developer Console?

Mostly:

```text
Salesforce Developers
```

Sometimes architects.

Rarely admins.

---

### 36. Important Note

Historically very popular.

Today most professional developers prefer:

```text
VS Code + Salesforce CLI
```

for development.

Developer Console is still useful for:

```text
Quick Debugging

Anonymous Apex

Viewing Logs
```

---

### 37. Practical

Navigate:

```text
Gear Icon
     ↓
Developer Console
```

Open:

```text
Debug
     ↓
Open Execute Anonymous Window
```

Execute:

```java
System.debug('Hello Salesforce');
```

Check logs.

---

# Part 9: VS Code + Salesforce CLI

### 38. Modern Development Environment

Professional Salesforce developers typically use:

```text
Visual Studio Code

Salesforce CLI

Git

GitHub
```

instead of Developer Console.

---

### 39. Why?

Better support for:

```text
Source Control

Deployment

CI/CD

Testing

Large Projects
```

---

### 40. Who Uses It?

Primarily:

```text
Salesforce Developers

Technical Architects
```

---

# Part 10: Reports

### 41. What are Reports?

Reports display data.

Examples:

```text
Open Opportunities

Cases By Status

Leads By Source
```

---

### 42. Who Uses Reports?

```text
Sales Users

Support Users

Managers

Admins
```

Almost everyone.

---

# Part 11: Dashboards

### 43. What are Dashboards?

Dashboards visualize report data.

Examples:

```text
Charts

Graphs

KPIs

Revenue Trends
```

---

### 44. Who Uses Dashboards?

Mostly:

```text
Managers

Executives

Team Leads
```

---

# Part 12: AppExchange

### 45. What is AppExchange?

AppExchange is Salesforce's application marketplace.

Purpose:

```text
Install Ready-Made Solutions
```

Examples:

```text
DocuSign

Accounting Apps

Project Management Apps
```

---

### 46. Who Uses AppExchange?

Mostly:

```text
Admins

Consultants

Architects
```

to find solutions.

---

# Part 13: Salesforce Go

### 47. What is Salesforce Go?

Salesforce Go helps organizations discover and enable Salesforce features and products.

Think of it as:

```text
Feature Discovery Center
```

---

### 48. Why Salesforce Go Exists?

Many customers do not know:

```text
What Features They Own

What Features Exist

How To Enable Features
```

Salesforce Go helps identify opportunities.

---

### 49. Example

Salesforce Go may suggest:

```text
Enable Knowledge

Enable Service Features

Try AI Features

Use Data Cloud
```

depending on your licenses.

---

### 50. Who Uses Salesforce Go?

Mostly:

```text
Admins

Architects

Platform Owners

Consultants
```

Not typical end users.

---

# Part 14: Setup vs Service Setup

### 51. Common Interview Question

Many beginners confuse these.

---

### 52. Setup

Purpose:

```text
Entire Salesforce Org Configuration
```

Contains:

```text
Security

Objects

Automation

Users

Reports

Development
```

Scope:

```text
Whole Platform
```

---

### 53. Service Setup

Purpose:

```text
Service Cloud Configuration
```

Contains:

```text
Cases

Knowledge

Email-To-Case

Omni-Channel
```

Scope:

```text
Service Cloud Features
```

Only.

---

# Part 15: Setup vs Developer Console

### 54. Another Common Confusion

Setup:

```text
Configuration
```

Developer Console:

```text
Coding & Debugging
```

---

### 55. Example

Create Field:

```text
Setup
```

Write Apex:

```text
Developer Console
```

View Debug Logs:

```text
Developer Console
```

Create User:

```text
Setup
```

---

# Part 16: Who Uses What?

### 56. Complete Role Mapping

| Interface | Sales User | Support Agent | Admin | Developer | Architect |
|------------|------------|------------|------------|------------|------------|
| App Launcher | Yes | Yes | Yes | Yes | Yes |
| Sales App | Yes | Rarely | Yes | Testing | Review |
| Service App | Rarely | Yes | Yes | Testing | Review |
| Setup | No | No | Yes | Yes | Yes |
| Service Setup | No | No | Yes | Sometimes | Yes |
| Object Manager | No | No | Yes | Yes | Yes |
| Flow Builder | No | No | Yes | Yes | Yes |
| Developer Console | No | No | Rarely | Yes | Sometimes |
| VS Code + CLI | No | No | Rarely | Yes | Yes |
| Reports | Yes | Yes | Yes | Sometimes | Yes |
| Dashboards | Yes | Yes | Yes | Sometimes | Yes |
| AppExchange | No | No | Yes | Sometimes | Yes |
| Salesforce Go | No | No | Yes | Rarely | Yes |

---

## Salesforce Free Account Practical

### 57. Goal

Explore every major Salesforce interface.

---

### Step 1: Open App Launcher

```text
App Launcher
```

Switch between:

```text
Sales

Service
```

---

### Step 2: Explore Sales App

Open:

```text
Leads

Accounts

Contacts

Opportunities
```

---

### Step 3: Explore Service App

Open:

```text
Cases

Knowledge
```

---

### Step 4: Open Setup

Navigate:

```text
Setup
```

Search:

```text
Users

Flow

Object Manager
```

---

### Step 5: Open Object Manager

Inspect:

```text
Account Object
```

Look at:

```text
Fields

Page Layouts

Validation Rules
```

---

### Step 6: Open Flow Builder

Create a new flow (don't activate it yet).

Observe the automation designer.

---

### Step 7: Open Developer Console

Run:

```java
System.debug('Hello Salesforce');
```

Observe logs.

---

### Step 8: Explore Reports

Create a simple Accounts report.

---

### Step 9: Explore Dashboards

Create a simple dashboard using the report.

---

### Step 10: Visit Salesforce Go

Explore available recommendations and feature discovery options in your org.
