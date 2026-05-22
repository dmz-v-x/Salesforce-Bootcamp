## Salesforce Apps & Navigation

Before learning objects, records, automation, or security, it is important to understand how users actually access Salesforce.

When a user logs in to Salesforce, they do not directly open an object such as Account or Opportunity.

Instead, they open an **App**.

An app acts like a workspace that brings together:

- Objects
- Tabs
- Navigation menus
- Utilities
- Branding
- Productivity tools

Think of an app as a complete working environment designed for a specific team.

Examples:

- Sales team uses Sales App
- Service team uses Service App
- Marketing team uses Marketing App
- HR team uses HR App
- Finance team uses Finance App

Everything in this chapter revolves around how Salesforce organizes these workspaces.

---

### 1. What Is a Salesforce App?

A Salesforce App is a collection of components bundled together into a single workspace.

It provides users with everything they need for a particular job role.

A Salesforce app can contain:

- Objects
- Tabs
- Lightning pages
- Utility tools
- Navigation items
- Branding
- Dashboards
- Reports

Without apps, users would have access to everything in one giant interface, which would be confusing.

Apps organize Salesforce into logical workspaces.

---

### 2. Real-World Analogy

Imagine a smartphone.

Your phone contains many applications:

- WhatsApp
- Instagram
- Gmail
- YouTube

Each app contains different screens and features.

Similarly, Salesforce contains different business apps.

Examples:

Sales App:

- Leads
- Accounts
- Opportunities

Service App:

- Cases
- Knowledge
- Service Console

Marketing App:

- Campaigns
- Leads
- Reports

Each app focuses on a specific business function.

---

### 3. Why Salesforce Uses Apps

Without apps:

- Sales users see service tools
- Service users see marketing tools
- HR users see finance tools

Result:

- Confusion
- Poor productivity
- Cluttered interface

Apps solve this problem by displaying only relevant tools.

Benefits:

- Better user experience
- Easier navigation
- Faster productivity
- Less training required
- Cleaner interface

---

### 4. Types of Salesforce Apps

Major categories:

1. Standard Apps
2. Custom Apps
3. Console Apps

These are the most important app types in Salesforce.

---

### 5. Standard Apps

A Standard App is an app provided by Salesforce out of the box.

These apps already exist when Salesforce is installed.

Salesforce creates them for common business functions.

Examples:

- Sales
- Service
- Marketing
- Commerce
- Analytics
- Field Service
- Education
- Financial Services (depending on edition)

---

### 6. Sales App

Most common standard app.

Designed for sales teams.

Contains:

- Leads
- Accounts
- Contacts
- Opportunities
- Campaigns
- Tasks
- Dashboards
- Reports

Example:

Sales representative workflow:

1. Receive lead
2. Convert lead
3. Manage account
4. Create opportunity
5. Close deal

All tools are available inside the Sales App.

---

### 7. Service App

Designed for support teams.

Contains:

- Cases
- Accounts
- Contacts
- Knowledge
- Reports
- Dashboards

Example:

Customer reports issue.

Support agent:

1. Opens case
2. Reviews customer details
3. Searches knowledge article
4. Resolves issue
5. Closes case

Everything happens within Service App.

---

### 8. Marketing App

Designed for marketing teams.

Contains:

- Campaigns
- Leads
- Reports
- Dashboards

Example:

Marketing manager:

1. Creates campaign
2. Tracks responses
3. Analyzes performance
4. Generates reports

---

### 9. Characteristics of Standard Apps

Created by Salesforce.

Advantages:

- Ready to use
- No development required
- Best-practice design
- Supported by Salesforce
- Easy setup

Limitations:

- May contain unnecessary features
- Not fully tailored to company needs

Because every company is different, custom apps are often created.

---

### 10. What Is a Custom App?

A Custom App is an app created by an administrator or developer.

It is designed specifically for an organization's business processes.

Unlike standard apps, custom apps are completely customizable.

---

### 11. Why Custom Apps Exist

Every company has unique requirements.

Example:

Hospital:

Needs:

- Patients
- Doctors
- Appointments

School:

Needs:

- Students
- Teachers
- Classes

Construction company:

Needs:

- Projects
- Sites
- Contractors

Standard Salesforce apps do not provide these objects by default.

Custom apps solve this problem.

---

### 12. Example: Hospital Management App

Custom app called:

Hospital Management

Contains:

- Patients
- Doctors
- Appointments
- Billing
- Medical Reports

Navigation may include:

- Home
- Patients
- Doctors
- Appointments
- Reports

Only hospital-related tools are displayed.

---

### 13. Example: Recruitment App

Recruitment department needs:

- Candidates
- Interviews
- Job Openings
- Recruiters

Custom app:

Recruitment Management

Navigation:

- Candidates
- Jobs
- Interviews
- Offers
- Reports

Users see only recruitment functionality.

---

### 14. Components of a Custom App

A custom app may include:

- Standard objects
- Custom objects
- Lightning pages
- Reports
- Dashboards
- Utility tools
- Navigation menu
- Branding

Administrator decides exactly what users can access.

---

### 15. Advantages of Custom Apps

Benefits:

- Tailored to business needs
- Cleaner navigation
- Better user adoption
- Higher productivity
- Easier maintenance

---

### 16. Standard App vs Custom App

| Feature | Standard App | Custom App |
|----------|----------|----------|
| Created By | Salesforce | Admin/Developer |
| Ready To Use | Yes | No |
| Customizable | Limited | Extensive |
| Business Specific | No | Yes |
| Development Needed | No | Often Yes |

---

### 17. What Is a Console App?

A Console App is a specialized Salesforce app designed for users who handle many records simultaneously.

Examples:

- Customer support agents
- Call center agents
- Sales representatives
- Help desk staff

Console apps allow users to work faster using tabs and sub-tabs.

---

### 18. Why Console Apps Were Created

Imagine a support agent.

Customer calls and says:

"My order is delayed."

Agent must check:

- Customer record
- Case record
- Order record
- Previous interactions
- Knowledge articles

Opening each page separately wastes time.

Console apps keep everything organized in a single workspace.

---

### 19. Traditional Navigation Problem

Without console:

Open Account

Then:

Back

Open Case

Then:

Back

Open Contact

Then:

Back

This is slow.

---

### 20. Console Solution

Console provides:

- Primary tabs
- Sub-tabs
- Multi-record workspace

Agent can keep many records open simultaneously.

Example:

Main Tab:
Customer Account

Sub-tabs:

- Contact
- Case
- Order
- Notes

Everything remains visible.

---

### 21. Features of Console Apps

Major features:

- Tabbed interface
- Sub-tabs
- Split view
- Workspace API
- Keyboard shortcuts
- Utility bar integration
- Productivity tools

---

### 22. Service Console Example

Customer support agent opens:

Case #1001

Related records open as subtabs:

- Customer
- Product
- Order
- Knowledge Article

Agent solves issue without repeatedly navigating.

This significantly improves productivity.

---

### 23. Sales Console Example

Sales representative works on:

Opportunity

Sub-tabs:

- Account
- Contact
- Activities
- Quotes

All information stays together.

---

### 24. What Are Navigation Items?

Navigation items are the tabs shown at the top of a Salesforce app.

Examples:

- Home
- Accounts
- Contacts
- Leads
- Opportunities
- Cases
- Reports

These items allow users to move between different parts of the application.

---

### 25. Navigation Bar

Top horizontal menu in Lightning Experience.

Example:

Home | Accounts | Contacts | Opportunities | Reports

Each item is a navigation item.

---

### 26. Purpose of Navigation Items

They help users quickly access frequently used resources.

Benefits:

- Faster navigation
- Better usability
- Reduced clicks
- Better productivity

---

### 27. What Can Be Added as Navigation Items?

Navigation bar can contain:

- Standard objects
- Custom objects
- Reports
- Dashboards
- Lightning pages
- Visualforce pages
- Web tabs
- Custom tabs

---

### 28. Example Navigation Setup

Sales App:

- Home
- Leads
- Accounts
- Contacts
- Opportunities
- Reports
- Dashboards

Service App:

- Home
- Cases
- Accounts
- Contacts
- Knowledge

Each app can have different navigation items.

---

### 29. What Is the Utility Bar?

The Utility Bar is a small toolbar that appears at the bottom of a Lightning app.

It provides quick access to tools without leaving the current page.

Think of it as a toolbox always available while working.

---

### 30. Why Utility Bar Exists

Without utility bar:

User must navigate away from current record.

With utility bar:

User can access tools instantly.

Improves productivity.

---

### 31. Common Utility Bar Components

Examples:

- Notes
- History
- Softphone
- Recent Records
- Omni-Channel
- Macros
- Custom Lightning Components

---

### 32. Utility Bar Example

Support agent is viewing a case.

At bottom:

- Notes
- Phone
- History

Agent can:

- Add notes
- Make call
- Check history

Without leaving the case page.

---

### 33. Softphone Example

Call center agents often use integrated telephony.

Utility Bar can contain:

Softphone

Agent can:

- Receive calls
- Dial customers
- Log interactions

Directly inside Salesforce.

---

### 34. Omni-Channel Example

Utility Bar may contain:

Omni-Channel

Automatically routes:

- Cases
- Chats
- Messages

To available agents.

---

### 35. Benefits of Utility Bar

Advantages:

- Faster work
- Fewer page changes
- Better multitasking
- Improved productivity
- Better user experience

---

### 36. What Is App Branding?

App Branding is the process of customizing the visual identity of a Salesforce app.

Branding makes apps easier to recognize and provides a professional appearance.

---

### 37. Why App Branding Matters

Imagine an organization with:

- Sales App
- HR App
- Finance App
- Recruitment App

Without branding:

All apps look similar.

Users may accidentally open the wrong app.

Branding improves recognition.

---

### 38. Branding Elements

Common branding options:

- App logo
- App icon
- Color theme
- App name
- Company identity

---

### 39. Example Branding

Sales App:

- Blue icon
- Sales logo

Service App:

- Green icon
- Headset logo

Recruitment App:

- Purple icon
- Candidate logo

Users immediately know which app they opened.

---

### 40. How App Branding Helps Users

Benefits:

- Faster recognition
- Better navigation
- Professional appearance
- Strong company identity
- Better user adoption

---

### 41. Real-World End-to-End Example

Company:

ABC Technologies

Departments:

- Sales
- Customer Support
- HR

Sales App:

Navigation:

- Leads
- Accounts
- Opportunities

Utility Bar:

- Notes
- Recent Records

Branding:

- Blue sales icon

---

Service Console App:

Navigation:

- Cases
- Knowledge
- Contacts

Utility Bar:

- Omni-Channel
- Softphone
- Notes

Branding:

- Green headset icon

---

HR Custom App:

Navigation:

- Employees
- Leave Requests
- Payroll

Utility Bar:

- Notes
- Quick Actions

Branding:

- Purple HR icon

Each department receives a dedicated workspace optimized for its tasks.

---

### 42. Complete Revision

#### Standard Apps

- Built by Salesforce
- Ready to use
- Sales App
- Service App
- Marketing App

#### Custom Apps

- Built by admin/developer
- Tailored to business needs
- Uses custom objects and pages

#### Console Apps

- Multi-record workspace
- Tabs and subtabs
- Best for support and high-volume users

#### Navigation Items

- Top menu tabs
- Provide quick access to resources
- Different for each app

#### Utility Bar

- Bottom toolbar
- Always accessible
- Contains productivity tools

#### App Branding

- Logo
- Icon
- Color identity
- Improves recognition and usability

Together, these components form the foundation of how users interact with Salesforce applications in Lightning Experience.
