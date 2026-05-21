## Salesforce Org Tour

### 1. What is a Salesforce Org

In Salesforce, an organization is usually called an "Org".

A Salesforce Org is a dedicated Salesforce environment provided to a company or user.

Think of it as:

"A complete Salesforce workspace where all business data, users, configurations, automation, and applications exist."

Every company using Salesforce gets its own org.

---

### 2. Real-World Analogy for Salesforce Org

Imagine an apartment building.

The building is Salesforce infrastructure.

Each apartment is a separate Salesforce Org.

Every apartment:
- Has different people
- Has different data
- Has different settings
- Is isolated from others

Similarly:
Every Salesforce org is separate and secure.

---

### 3. Types of Salesforce Orgs

Common types include:

#### Production Org
Real live environment used by businesses.

Contains:
- Real users
- Real customer data
- Actual operations

---

#### Sandbox Org
Copy of production used for:
- Testing
- Development
- Training

---

#### Developer Org
Free org for learning and development.

Mostly used by:
- Beginners
- Developers
- Students

---

#### Trailhead Playground
Practice org connected with Trailhead exercises.

---

## Salesforce Org Tour Overview

### 4. What Exists Inside a Salesforce Org

A Salesforce org contains:

- Users
- Data
- Objects
- Applications
- Security settings
- Automation
- Reports
- Dashboards
- Code
- Integrations

Everything inside a company's Salesforce system exists inside the org.

---

### 5. Main Areas of Salesforce UI

When you open Salesforce, you generally interact with two major areas:

1. Application Area
2. Setup Area

Understanding the difference is extremely important.

---

## What is Sales Application

### 6. What is an Application in Salesforce

In Salesforce, an application (App) is a collection of tools, tabs, objects, and features grouped together for specific business purposes.

Example apps:
- Sales App
- Service App
- Marketing App

Apps help different teams work efficiently.

---

### 7. What is the Sales Application

Sales Application (Sales App) is a Salesforce application designed mainly for sales teams.

It helps salespeople manage:
- Leads
- Customers
- Opportunities
- Accounts
- Contacts
- Deals
- Sales activities

---

### 8. Real-World Example of Sales Application

Suppose a company sells software products.

Sales team needs to:
- Track interested customers
- Record meetings
- Manage follow-ups
- Close deals

Sales App provides all required tools in one place.

---

### 9. Major Features of Sales App

Sales App commonly includes:

- Leads
- Accounts
- Contacts
- Opportunities
- Tasks
- Events
- Reports
- Dashboards

---

### 10. What is a Lead

A Lead represents a potential customer.

Example:
Someone fills:
"Contact Us" form on website.

That person becomes a Lead.

---

### 11. What is an Account

An Account usually represents:
- Company
OR
- Customer organization

Example:
"TCS", "Infosys", "Amazon"

---

### 12. What is a Contact

Contact represents a person associated with an account.

Example:

Account:
Amazon

Contact:
John Smith (Manager at Amazon)

---

### 13. What is an Opportunity

Opportunity represents a possible sales deal.

Example:
Customer interested in buying software worth $50,000.

Sales team tracks:
- Deal stage
- Expected revenue
- Probability of closing

Using opportunities.

---

## Setup UI vs Service Setup UI

### 14. Introduction to Setup Areas

Salesforce has multiple administrative interfaces.

Two important ones are:

1. Setup UI
2. Service Setup UI

Beginners often confuse these.

So let us understand them carefully.

---

## Setup UI

### 15. What is Setup UI

Setup UI is the main administrative area of Salesforce.

Administrators and developers use Setup to configure the Salesforce org.

Think of Setup as:

"The control center of Salesforce."

---

### 16. Where Setup is Used

Setup is used for:
- Configuration
- Customization
- Security
- Development
- Automation
- User management

Almost all Salesforce administration happens here.

---

### 17. Examples of Things Managed in Setup

Inside Setup, administrators manage:

- Users
- Profiles
- Roles
- Objects
- Fields
- Validation rules
- Flows
- Apex classes
- Security settings
- Apps
- Integrations

---

### 18. How to Open Setup UI

Usually:
- Click Gear Icon
- Click "Setup"

This opens the Setup interface.

---

### 19. Structure of Setup UI

Setup UI mainly contains:

#### Navigation Panel
Left-side menu containing settings.

#### Quick Find Box
Search bar to quickly find settings.

#### Main Configuration Area
Displays selected setup pages.

---

### 20. Who Uses Setup UI

Main users:
- Salesforce Administrators
- Developers
- Architects
- Consultants

End business users generally do not use Setup.

---

## Service Setup UI

### 21. What is Service Setup UI

Service Setup is a specialized guided setup interface for Service Cloud configuration.

It simplifies customer service setup.

Think of it as:

"A simplified setup experience focused on customer support operations."

---

### 22. Why Service Setup Exists

Normal Setup contains thousands of settings.

Beginners may feel overwhelmed.

Service Setup provides:
- Guided workflows
- Simplified configuration
- Service-focused setup experience

---

### 23. Features Configured in Service Setup

Service Setup helps configure:

- Support channels
- Case management
- Email-to-case
- Live chat
- Knowledge base
- Omni-channel routing

---

### 24. Real-World Example

Suppose a company wants:
- Customer support agents
- Ticketing system
- Live chat support

Instead of manually configuring everything through Setup, Service Setup provides guided steps.

---

## Difference Between Setup UI and Service Setup UI

### 25. Main Difference

#### Setup UI
General-purpose administration interface.

#### Service Setup UI
Customer service-focused guided configuration interface.

---

### 26. Complexity Difference

#### Setup UI
- Very powerful
- Very detailed
- Contains thousands of settings

#### Service Setup UI
- Simplified
- Guided
- Focused on service features

---

### 27. Audience Difference

#### Setup UI
Used by:
- Admins
- Developers
- Architects

#### Service Setup UI
Used by:
- Service administrators
- Support managers
- Beginners configuring Service Cloud

---

### 28. Flexibility Difference

#### Setup UI
Maximum customization and control.

#### Service Setup UI
Simplified experience with limited guided flows.

---

### 29. Where Do We Actually Work

In real-world Salesforce work:

Most administrators and developers primarily work inside:
Setup UI

Because:
- Full configuration options exist there
- Advanced customization requires Setup
- Development work happens there

Service Setup is mainly used for:
- Faster Service Cloud onboarding
- Guided customer service configuration

---

### 30. Important Beginner Understanding

Service Setup is not separate from Salesforce.

It is simply:
"A specialized setup experience built on top of the main Setup system."

Actual configurations still belong to the same org.

---

## Company Information

### 31. What is Company Information

Company Information is a section under:

Setup → Company Settings → Company Information

It contains basic information about the Salesforce organization.

Think of it as:

"The identity and resource information page of the org."

---

### 32. Information Available in Company Information

This page contains details like:

- Organization Name
- Organization ID
- Salesforce Edition
- Instance
- Time Zone
- Storage Usage
- User Licenses
- API Usage

---

### 33. Why Company Information is Important

Administrators use it to:
- Monitor org limits
- Track licenses
- Verify org details
- Check storage
- Identify org type

---

### 34. Storage Information

Salesforce provides storage limits.

Two important types:

#### Data Storage
Stores records.

Example:
Accounts, Contacts, Opportunities.

---

#### File Storage
Stores uploaded files and attachments.

Example:
PDFs, images, documents.

---

### 35. User License Information

Company Information shows:
- Total licenses
- Used licenses
- Remaining licenses

Example:
100 total licenses
75 used
25 available

---

## Salesforce Organization ID

### 36. What is Organization ID

Every Salesforce org has a unique identifier called:

Organization ID

Also called:
Org ID

---

### 37. Why Organization ID Exists

Salesforce manages millions of orgs globally.

Each org needs a unique identity.

Organization ID helps Salesforce uniquely identify an org.

---

### 38. Real-World Analogy

Think of Organization ID like:

- Passport number
- Aadhaar number
- Company registration number

It uniquely identifies the organization.

---

### 39. Where to Find Organization ID

Path:

Setup → Company Settings → Company Information

There you can find:
Organization ID

---

### 40. Format of Organization ID

Organization IDs are long alphanumeric values.

Example format:
00DXXXXXXXXXXXX

Every org has a different ID.

---

### 41. Why Org ID is Important

Org ID is used in:

- API integrations
- Salesforce support cases
- Deployments
- Connected apps
- CI/CD pipelines
- Authentication systems

---

### 42. Real-World Example of Org ID Usage

Suppose a developer builds integration between:
- Salesforce
- External payment system

The integration may use Org ID to identify the correct Salesforce org.

---

### 43. Security Importance of Org ID

Org ID alone does not give system access.

But it is still considered important organization information.

Companies usually avoid exposing it publicly unnecessarily.
