## Salesforce Objects

# 1. First Understand The Problem

Before Salesforce existed, companies stored data in:

- Excel sheets
- Databases
- Paper files
- Local software

Example:

A company wants to store:

- Customers
- Employees
- Products
- Orders
- Support Cases

Question:

Where should all this information live?

Need:

- Organized storage
- Search capability
- Security
- Relationships
- Reporting

Salesforce solves this problem.

---

# 2. What Is An Object?

Most important definition:

An Object is a container that stores a specific type of business information.

Think:

| Real World | Salesforce |
|------------|------------|
| Notebook | Object |
| Page | Record |
| Column | Field |

Example:

Customer notebook:

| Name | Phone | Email |
|--------|--------|--------|
| John | 999999 | john@email.com |

Notebook = Object

John row = Record

Name column = Field

---

# 3. Object Definition

Officially:

An Object is a database table in Salesforce.

If you know SQL:

Database = Salesforce Org

Table = Object

Row = Record

Column = Field

Example:

Customer table:

| Id | Name | Email |
|----|----|----|
|1|John|john@mail.com|
|2|Mike|mike@mail.com|

In Salesforce:

Customer Object

contains

Customer Records

with

Customer Fields

---

# 4. Why Objects Exist

Objects help organize data.

Without objects:

Everything mixed together.

Bad example:

| Name | Product | Employee | Case |
|--------|--------|--------|--------|
| John | Laptop | David | Broken screen |

Very messy.

Instead:

Customer Object

Product Object

Employee Object

Case Object

Separate storage.

Much cleaner.

---

# 5. Salesforce Database Architecture

Simplified:

Salesforce Org

↓

Objects

↓

Records

↓

Fields

Visual:

Organization

├── Account Object

│ ├── Record 1

│ ├── Record 2

│ └── Record 3

│

├── Contact Object

│ ├── Record 1

│ ├── Record 2

│

└── Opportunity Object

└── Record 1

---

# 6. Standard Objects

Salesforce provides built-in objects.

These come automatically.

Examples:

### Account

Stores companies.

Example:

Amazon

Google

Microsoft

---

### Contact

Stores people.

Example:

John Smith

Mary Thomas

---

### Lead

Potential customer.

Example:

Someone filled website form.

---

### Opportunity

Potential sale.

Example:

$50,000 software deal.

---

### Case

Support issue.

Example:

Customer complaint.

---

### Campaign

Marketing initiative.

Example:

Summer Sale 2026

---

### Product

Items being sold.

Example:

Laptop

Phone

Software License

---

# 7. Custom Objects

When standard objects aren't enough.

You create your own.

Examples:

Hospital:

Patient Object

University:

Student Object

Gym:

Membership Object

Travel Agency:

Tour Package Object

Real Estate:

Property Object

These are called Custom Objects.

---

# 8. How Salesforce Identifies Custom Objects

Salesforce adds:

__c

Example:

Student__c

Patient__c

Vehicle__c

Property__c

The "__c" means:

Custom object.

---

# 9. Object Structure

Every object contains:

- Fields
- Records
- Relationships
- Security
- Validation Rules
- Automation
- Reports
- API Metadata

Think of object as a complete mini application.

---

# 10. Record

A single entry.

Example:

Student Object

| Student Name | Age |
|----|----|
| Rahul | 21 |

Rahul = Record

---

# 11. Fields

Fields store individual values.

Example:

Student Record

Name = Rahul

Age = 21

Email = rahul@gmail.com

Phone = 999999999

Each piece = Field

---

# 12. Every Object Has Standard Fields

Salesforce automatically creates fields.

Examples:

### Id

Unique identifier.

Example:

001XX000000ABCDEF

---

### Owner

Who owns record.

---

### Created Date

When record created.

---

### Last Modified Date

Last update timestamp.

---

### Created By

Creator user.

---

### Last Modified By

Updater user.

---

# 13. Name Field

Every object requires one name field.

Two options:

### Text

Example:

Student Name

---

### Auto Number

Example:

STU-0001

STU-0002

STU-0003

Generated automatically.

---

# 14. Object Metadata

Object itself is metadata.

Metadata means:

Configuration that defines behavior.

Examples:

- Object name
- Label
- API name
- Fields
- Relationships
- Validation rules

All metadata.

Not actual data.

---

# 15. Object Label vs API Name

Example:

Label:

Student

API Name:

Student__c

Developers use API Name.

Users see Label.

---

# 16. Plural Label

Example:

Label:

Student

Plural:

Students

Used in UI.

Example:

Students Tab

---

# 17. API Name Rules

Allowed:

Student__c

Vehicle__c

Employee_Record__c

Not allowed:

Student Data!

My Object@

Special characters not allowed.

---

# 18. Deployment Status

Options:

### In Development

Visible only to admins.

---

### Deployed

Available to users.

Very important during production rollout.

---

# 19. Object Settings

While creating object:

Choose:

- Allow Reports
- Allow Activities
- Allow Search
- Track History
- Enable Feeds
- Enable Bulk API
- Enable Streaming API

Each setting changes behavior.

---

# 20. Allow Reports

Without this:

Cannot build reports.

Usually enabled.

---

# 21. Allow Activities

Enables:

Tasks

Events

Calls

Meetings

Emails

Associated with records.

---

# 22. Track Field History

Tracks field changes.

Example:

Status

Open → Closed

Salesforce stores audit history.

---

# 23. Enable Search

Allows global search.

Without it:

Records won't appear in search results.

---

# 24. Object Relationships

Objects rarely live alone.

Example:

Company

has

Employees

Account

has

Contacts

Relationship needed.

---

# 25. Lookup Relationship

Loose relationship.

Example:

Student → Teacher

Teacher deleted?

Student remains.

Reference removed.

---

# 26. Master Detail Relationship

Strong relationship.

Example:

Order

contains

Order Items

Delete order?

Items deleted automatically.

Very important concept.

---

# Hands-On Lab 1 — Create First Custom Object

Goal:

Create Student Object.

### Step 1

Login Developer Org.

### Step 2

Click Gear Icon

→ Setup

### Step 3

Search:

Object Manager

### Step 4

Click:

Object Manager

### Step 5

Click:

Create

→ Custom Object

### Step 6

Fill:

Label:

Student

Plural Label:

Students

Record Name:

Student Number

Data Type:

Auto Number

Display Format:

STU-{0000}

Start Number:

1

### Step 7

Check:

Allow Reports

Allow Activities

Track Field History

### Step 8

Save

Student object created.

---

# Hands-On Lab 2 — Add Fields

Inside Student Object:

### New Field 1

Text

Field Label:

Student Name

Length:

80

Save

---

### New Field 2

Email

Field Label:

Email

Save

---

### New Field 3

Number

Field Label:

Age

Length:

3

Decimal Places:

0

Save

---

### New Field 4

Date

Field Label:

Admission Date

Save

---

### New Field 5

Picklist

Field Label:

Status

Values:

Active

Inactive

Graduated

Save

---

# Hands-On Lab 3 — Create Records

Open:

App Launcher

Search:

Students

Click:

New

Create:

Student 1

Name:

Rahul Sharma

Email:

rahul@gmail.com

Age:

21

Status:

Active

Save

Create several records.

Observe:

Auto Number generated automatically.

Example:

STU-0001

STU-0002

STU-0003

---

# Hands-On Lab 4 — Create Relationship

Goal:

Student belongs to Department.

Create Object:

Department

Fields:

Department Name

Create records:

Computer Science

Mechanical

Civil

Now:

Student Object

New Field

Relationship

Lookup Relationship

Related To:

Department

Save

Now each student can belong to department.

---

# Real Enterprise Example

University CRM

Objects:

Student__c

Professor__c

Course__c

Department__c

Enrollment__c

Relationships:

Student

↓

Enrollment

↓

Course

↓

Department

Entire system built using objects.

---

# What Developers Do With Objects

Apex:

query records

insert records

update records

delete records

Example:

Student__c s = new Student__c();

s.Student_Name__c = 'Rahul';

insert s;

Object becomes code representation.

---

# What Admins Do With Objects

Admins:

- Create objects
- Add fields
- Manage security
- Configure layouts
- Build automation
- Build reports

No coding required.

---

# Common Object Design Mistakes

### Mistake 1

Creating duplicate objects.

Bad:

Student Object

Student Info Object

Student Data Object

Use one properly designed object.

---

### Mistake 2

Too many fields.

200 unnecessary fields.

Hard to maintain.

---

### Mistake 3

Wrong relationship type.

Using Lookup instead of Master Detail.

Causes reporting issues.

---

### Mistake 4

Poor naming.

Obj1__c

Obj2__c

Meaningless.

Use business names.

---

# Hidden Gotchas

### Gotcha 1

Object Label can change.

API Name cannot easily change later.

Choose carefully.

---

### Gotcha 2

Deleting object deletes records.

Potential data loss.

Always backup.

---

### Gotcha 3

Custom Object counts toward limits.

Enterprise orgs have limits.

Plan architecture.

---

### Gotcha 4

Master Detail ownership inherited.

Cannot set separate owner.

Many beginners get confused.

---

### Gotcha 5

Field History Tracking has limits.

Not every field can be tracked forever.

Understand retention policies.

---

# Object Creation Checklist

Before creating object ask:

1. What business process exists?
2. What data must be stored?
3. What fields needed?
4. Relationships needed?
5. Security requirements?
6. Reporting requirements?
7. Automation requirements?
8. Mobile requirements?
9. Integration requirements?
10. Long-term scalability?

---

# Interview Questions

### What is an Object?

A database table in Salesforce used to store a specific type of business data.

---

### Difference Between Standard And Custom Object?

Standard:

Provided by Salesforce.

Custom:

Created by users/admins.

---

### Why Use Custom Objects?

To store business-specific information not supported by standard objects.

---

### What Is Record?

Single row of data in an object.

---

### What Is Field?

Single piece of information in a record.

---

### Why Is API Name Important?

Used by Apex, SOQL, APIs, integrations, flows, reports and metadata references.

---

# Final Mental Model

Think:

Salesforce Org = Entire Library

Object = One Book

Field = Column Heading

Record = One Row

Relationship = Link Between Books

Metadata = Book Structure

Data = Information Written Inside

Everything in Salesforce ultimately revolves around:

Objects → Fields → Records → Relationships → Security → Automation → Reporting

If you truly understand objects, you understand the foundation upon which almost every Salesforce feature is built.
