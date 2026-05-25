## Salesforce Developer Org

### 1. What Is a Salesforce Developer Org?

A Salesforce Developer Org (Developer Organization) is a **free Salesforce environment provided by Salesforce for learning, development, experimentation, and building applications**.

Think of it as your own personal Salesforce playground where you can:

- Learn Salesforce
- Practice configurations
- Create custom applications
- Write Apex code
- Build Lightning Web Components (LWC)
- Create automation
- Learn integrations
- Experiment without affecting any real business data

It is designed specifically for:

- Students
- Beginners
- Salesforce Developers
- Architects
- Consultants
- Admins learning new features
- Anyone preparing for Salesforce certifications

You can create one completely free.

---

### 2. Why Does Salesforce Provide Developer Orgs?

Imagine Salesforce only allowed development inside real company environments.

Problems:

- You might break production data.
- Learning becomes risky.
- Testing becomes dangerous.
- New developers cannot practice safely.

Therefore Salesforce provides isolated environments where developers can:

- Learn safely
- Build projects
- Test ideas
- Practice certifications
- Create portfolio projects

without impacting any real business.

---

### 3. Real World Analogy

Imagine learning to fly an airplane.

Would you immediately fly a real passenger aircraft?

No.

You first use:

- Flight simulators
- Training aircraft
- Practice environments

A Developer Org is exactly that.

It is:

- A practice Salesforce environment
- A learning sandbox
- A development workspace

for learning Salesforce safely.

---

### 4. Is Developer Org a Real Salesforce Environment?

Yes.

This is one of the biggest misconceptions beginners have.

A Developer Org is NOT:

- A fake Salesforce
- A demo website
- A simulator

It is a real Salesforce environment hosted by Salesforce.

You get access to:

- Objects
- Fields
- Record Types
- Flows
- Validation Rules
- Apex
- SOQL
- SOSL
- LWC
- Security
- Sharing
- Reports
- Dashboards

Almost everything needed for development.

---

### 5. What Do You Get Inside a Developer Org?

A fresh Developer Org typically includes:

#### CRM capabilities

- Accounts
- Contacts
- Leads
- Opportunities
- Cases

---

#### Custom development

- Custom Objects
- Custom Fields
- Custom Metadata
- Custom Settings

---

#### Automation

- Flow Builder
- Approval Processes
- Assignment Rules
- Escalation Rules

---

#### Programming

- Apex Classes
- Apex Triggers
- Batch Apex
- Queueable Apex
- Scheduled Apex

---

#### Frontend Development

- Lightning App Builder
- Lightning Pages
- Lightning Web Components
- Aura Components

---

#### Security Features

- Profiles
- Permission Sets
- Roles
- Sharing Rules

---

#### Data Tools

- Import Wizard
- Data Loader compatibility
- SOQL Query Editor
- Reports
- Dashboards

---

### 6. How Is a Developer Org Created?

You create one from Salesforce's developer program website.

Process:

#### Step 1

Visit Salesforce Developer signup page.

---

#### Step 2

Enter:

- Name
- Email
- Username

---

#### Step 3

Verify email.

---

#### Step 4

Set password.

---

#### Step 5

Login.

Now Salesforce provisions a completely new organization for you.

---

### 7. What Happens Behind The Scenes?

When Salesforce creates your Developer Org:

Salesforce automatically:

- Creates database
- Creates metadata repository
- Creates user account
- Assigns system administrator permissions
- Creates default CRM objects
- Creates default security model

You receive a fully functional Salesforce instance.

---

### 8. What Is an Org?

Before understanding Developer Org, we must understand Org.

Org means:

Organization.

In Salesforce:

Every company gets its own Salesforce environment.

Examples:

#### Company A

- Accounts
- Contacts
- Opportunities

stored separately.

---

#### Company B

- Different data
- Different users
- Different configurations

stored separately.

---

Each company receives:

One Org.

A Developer Org is simply a free Org given for development.

---

### 9. Is Developer Org Multi-Tenant?

Yes.

Salesforce architecture is:

Multi-Tenant Architecture.

Meaning:

Thousands of organizations share Salesforce infrastructure.

Example:

Physical server:

```text
Server
 ├── Org A
 ├── Org B
 ├── Org C
 └── Org D
```

Even though infrastructure is shared:

- Data is isolated
- Metadata is isolated
- Security is isolated

One org cannot access another org.

---

### 10. Default User in Developer Org

When the org is created:

You become:

System Administrator.

This means:

You initially have maximum permissions.

You can:

- Create objects
- Create fields
- Write Apex
- Build LWCs
- Create users
- Configure security
- Build automation

Everything is available.

---

### 11. Why Beginners Love Developer Orgs

Because you can:

Break things.

And nothing important gets damaged.

Examples:

- Delete custom field
- Create bad flow
- Deploy faulty Apex
- Experiment with sharing

No business users are affected.

This makes learning easier.

---

### 12. What Can You Build Inside a Developer Org?

Almost anything.

Examples:

#### CRM System

- Customers
- Leads
- Opportunities

---

#### Helpdesk Application

- Cases
- Support tickets
- Escalations

---

#### HR System

- Employees
- Leave requests
- Approvals

---

#### Inventory System

- Products
- Warehouses
- Orders

---

#### Education Portal

- Students
- Courses
- Attendance

---

#### AI Powered Applications

Using:

- Apex
- APIs
- Einstein
- Agentforce

---

### 13. Developer Org Storage Limits

Because it is free, limits exist.

Typical categories include:

#### Data Storage

Stores records.

Examples:

- Accounts
- Contacts
- Cases

---

#### File Storage

Stores files.

Examples:

- PDFs
- Images
- Documents

---

#### API Limits

Controls API usage.

---

#### Apex Limits

Controls resource consumption.

---

Developer org limits are usually sufficient for:

- Learning
- Certifications
- Personal projects
- Portfolio projects

but not for large production businesses.

---

### 14. Developer Org vs Production Org

| Feature | Developer Org | Production Org |
|----------|----------|----------|
| Cost | Free | Paid |
| Purpose | Learning & Development | Real Business |
| Users | Limited | Business Users |
| Data | Practice Data | Real Data |
| Risk | Safe to Experiment | Must Be Controlled |
| Development | Primary Use | Usually Restricted |
| Testing | Allowed | Carefully Managed |

---

### 15. Developer Org vs Sandbox

This confuses almost everyone.

---

#### Developer Org

Independent Salesforce Org.

Created from Salesforce signup page.

```text
Salesforce
   |
Developer Org
```

Standalone.

---

#### Sandbox

Copy of an existing production org.

```text
Production
     |
 Sandbox
```

Used by companies.

---

Difference:

Developer Org:

- Independent
- Free
- Learning focused

Sandbox:

- Derived from production
- Enterprise development
- Enterprise testing

---

### 16. Can Companies Use Developer Orgs?

Generally:

No.

Companies use:

- Production Org
- Sandboxes
- Scratch Orgs

Developer Org is mainly for:

- Learning
- Demonstrations
- POCs
- Personal development

---

### 17. What Is Included in Setup?

The most important area for Salesforce developers is:

Setup.

Access:

```text
Gear Icon
   →
Setup
```

Inside Setup you can configure:

- Objects
- Fields
- Flows
- Users
- Security
- Apex
- Deployments
- Metadata

Almost all Salesforce development starts from Setup.

---

### 18. Hands-On Example #1 — Create Your First Object

#### Step 1

Open Setup.

---

#### Step 2

Navigate:

```text
Object Manager
```

---

#### Step 3

Click:

```text
Create
→ Custom Object
```

---

#### Step 4

Enter:

```text
Label:
Student

Plural:
Students
```

---

#### Step 5

Save.

Salesforce automatically creates:

```text
Student__c
```

This is your first custom object.

---

### 19. Hands-On Example #2 — Add Fields

Inside Student object:

Click:

```text
Fields & Relationships
```

---

Create:

#### Text Field

```text
Student Name
```

---

#### Number Field

```text
Age
```

---

#### Email Field

```text
Email
```

---

Now you have:

```text
Student
 ├── Student Name
 ├── Age
 └── Email
```

---

### 20. Hands-On Example #3 — Create Records

Open App Launcher.

Search:

```text
Students
```

Open tab.

---

Click:

```text
New
```

Enter:

```text
Name = John
Age = 20
Email = john@example.com
```

Save.

You just created data in Salesforce.

---

### 21. Hands-On Example #4 — Create a Flow

Navigate:

```text
Setup
→ Flows
→ New Flow
```

Choose:

```text
Record Triggered Flow
```

Trigger:

```text
When Student Created
```

Action:

```text
Send Email
```

Activate.

Now automation runs automatically.

---

### 22. Hands-On Example #5 — Write Apex

Navigate:

```text
Setup
→ Apex Classes
→ New
```

Create:

```java
public class StudentHelper {

    public static String getMessage() {
        return 'Welcome Student';
    }

}
```

Save.

You just deployed Apex code.

---

### 23. Common Beginner Mistakes

#### Mistake 1

Thinking Developer Org equals Sandbox.

Wrong.

Developer Org is independent.

---

#### Mistake 2

Learning only clicks.

Modern Salesforce requires:

- Configuration
- Apex
- LWC
- Integrations

all together.

---

#### Mistake 3

Ignoring Setup.

Most Salesforce development starts inside Setup.

---

#### Mistake 4

Not learning data model.

Objects and fields are the foundation.

---

#### Mistake 5

Building random examples.

Build complete projects instead.

Examples:

- CRM
- Helpdesk
- HRMS
- Inventory Management

---

### 24. What Should a Salesforce Developer Learn Using a Developer Org?

Recommended order:

#### Phase 1

Platform Fundamentals

- Navigation
- Setup
- Apps
- Objects
- Fields

---

#### Phase 2

Data Model

- Relationships
- Record Types
- Page Layouts

---

#### Phase 3

Security

- Profiles
- Permission Sets
- Roles
- Sharing

---

#### Phase 4

Automation

- Flows
- Approvals

---

#### Phase 5

Programming

- Apex
- SOQL
- SOSL

---

#### Phase 6

Frontend

- Lightning Web Components

---

#### Phase 7

Integrations

- REST APIs
- Callouts
- Named Credentials

---

#### Phase 8

Deployment

- Sandboxes
- DevOps Center
- SFDX
- CI/CD

---

### 25. Final Mental Model

Think of a Salesforce Developer Org as:

```text
Your Personal Salesforce Laboratory

Inside it you can:

Learn
Practice
Configure
Develop
Test
Deploy
Break Things
Rebuild
Experiment
Build Portfolio Projects
Prepare Certifications
```

It is a complete Salesforce environment provided free by Salesforce, isolated from real businesses, and intended to help developers and administrators learn and build applications safely.
