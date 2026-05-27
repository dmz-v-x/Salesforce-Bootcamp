## Salesforce Release Cycles

### 1. Introduction

Salesforce is a cloud platform.

Unlike traditional software that customers install on their own servers and manually upgrade, Salesforce manages the entire platform and automatically delivers new features, bug fixes, security updates, and performance improvements several times every year.

These updates are called **Salesforce Releases**.

A release is a new version of the Salesforce platform that introduces:

- New features
- New products
- User interface improvements
- Security enhancements
- Performance optimizations
- API enhancements
- Bug fixes
- Deprecated feature notices

Every Salesforce organization (org) eventually receives these updates automatically.

---

### 2. Why Salesforce Has Release Cycles

Before cloud computing became popular, companies often had to:

- Purchase software
- Install software manually
- Upgrade software manually
- Maintain servers
- Apply patches themselves

This created many problems:

- Expensive upgrades
- Long maintenance windows
- Different customers running different versions
- Security vulnerabilities
- Compatibility issues

Salesforce solved this by using a cloud-based model.

Instead of customers upgrading software, Salesforce upgrades the platform for everyone.

Benefits:

- Everyone stays on a modern version
- Security updates arrive automatically
- New functionality becomes available quickly
- Reduced maintenance burden
- Consistent platform experience

---

### 3. What is a Salesforce Release?

A Salesforce release is a major platform update delivered by Salesforce to all customer organizations.

Think of it like:

- Windows version updates
- Android OS updates
- iOS updates

But for the Salesforce platform.

Examples:

- Spring '26
- Summer '26
- Winter '27

Each release contains hundreds or sometimes thousands of improvements.

A release may introduce:

- New Flow capabilities
- New Apex functionality
- New Lightning Experience features
- New Agentforce capabilities
- New API versions
- New security controls
- New AI functionality

---

### 4. Salesforce Release Naming Convention

Salesforce uses seasonal names.

Format:

```
Season + Year
```

Examples:

```
Spring '26
Summer '26
Winter '27
```

Important:

The season does not always exactly match your local weather season.

It is simply Salesforce's naming convention.

Example timeline:

| Release | Approximate Time |
|----------|----------|
| Spring | February |
| Summer | June |
| Winter | October |

---

### 5. How Many Releases Occur Every Year?

Salesforce delivers:

**3 major releases per year**

They are:

1. Spring Release
2. Summer Release
3. Winter Release

Example:

```
Spring '26
Summer '26
Winter '27
```

Therefore Salesforce evolves continuously throughout the year.

---

### 6. Release Timeline Overview

Typical annual cycle:

```
January-February
     ↓
Spring Release

May-June
     ↓
Summer Release

September-October
     ↓
Winter Release
```

Then the cycle repeats.

```
Winter → Spring → Summer → Winter
```

Every year.

---

### 7. What Happens During a Release?

Salesforce performs platform upgrades across its infrastructure.

Customers receive:

- New functionality
- Updated APIs
- Performance improvements
- Security enhancements
- User interface changes
- Metadata updates

Most upgrades happen automatically.

Customers usually do not need to install anything.

---

### 8. Components Affected by Releases

A release can affect almost every Salesforce area.

#### Sales Cloud

Examples:

- Opportunity enhancements
- Forecasting improvements
- Pipeline management updates

#### Service Cloud

Examples:

- Case management updates
- Omni-Channel improvements
- Knowledge enhancements

#### Experience Cloud

Examples:

- Community features
- Portal improvements
- Branding enhancements

#### Platform

Examples:

- Apex features
- SOQL improvements
- SOSL enhancements
- Metadata updates

#### Flow

Examples:

- New Flow elements
- Better debugging
- Improved automation capabilities

#### Security

Examples:

- Permission enhancements
- Authentication improvements
- MFA changes

#### APIs

Examples:

- New REST endpoints
- New SOAP capabilities
- New metadata operations

#### Agentforce and AI

Examples:

- New AI actions
- Prompt Builder improvements
- Agent capabilities
- Generative AI enhancements

---

### 9. Salesforce Release Architecture

A release generally moves through several environments before production.

Flow:

```
Salesforce Engineering
          ↓
Internal Testing
          ↓
Preview Sandboxes
          ↓
Production Rollout
```

This process helps Salesforce identify problems before customers receive updates.

---

### 10. What is a Preview Release?

A preview release allows organizations to see upcoming features before production receives them.

Purpose:

- Test applications
- Validate integrations
- Check custom code
- Verify business processes
- Prepare documentation
- Train users

Preview environments help companies discover issues early.

---

### 11. What is a Preview Sandbox?

A preview sandbox is a sandbox that receives the upcoming release before production.

Example:

Current production:

```
Spring '26
```

Preview sandbox:

```
Summer '26
```

Now developers can test:

- Apex code
- Flows
- Integrations
- Lightning components
- Validation rules
- Security configurations

before production upgrades.

---

### 12. Why Preview Testing is Important

Imagine a company has:

- Hundreds of Flows
- Thousands of Apex classes
- Multiple integrations
- Custom Lightning Web Components

A new release could potentially affect behavior.

Without testing:

- Production failures may occur
- Integrations may break
- UI changes may confuse users

Preview testing helps identify issues early.

---

### 13. Release Notes

For every release Salesforce publishes extensive documentation called Release Notes.

Release Notes explain:

- New features
- Changed features
- Retired functionality
- Critical updates
- Security changes
- API updates
- Known limitations

Release Notes can contain hundreds of pages.

Admins, developers, architects, and consultants often review them before upgrades.

---

### 14. What are Critical Updates?

Some changes are optional at first but later become mandatory.

These are called Critical Updates.

Examples:

- Security behavior changes
- API security updates
- Authentication changes
- Platform behavior modifications

Lifecycle:

```
Announced
      ↓
Optional Testing Period
      ↓
Customer Enablement
      ↓
Automatically Enforced
```

Organizations should test these updates before enforcement.

---

### 15. What Developers Must Check During Every Release

#### Apex

Verify:

- Compilation
- Runtime behavior
- Governor limits impact
- API compatibility

#### SOQL

Verify:

- Query behavior
- Selectivity
- Security enforcement

#### Integrations

Verify:

- API responses
- Authentication
- External system connectivity

#### Lightning Web Components

Verify:

- UI rendering
- Event handling
- Browser compatibility

#### Flows

Verify:

- Automation execution
- Fault handling
- Data updates

#### Security

Verify:

- Profiles
- Permission Sets
- Sharing behavior
- FLS enforcement

---

### 16. What Admins Must Check During Every Release

Admins should review:

- New automation features
- Flow enhancements
- User experience changes
- Permission updates
- Security features
- Reporting improvements
- Dashboard changes
- New setup options

They should also decide:

- Which features to enable
- Which features to postpone
- User training requirements

---

### 17. What Architects Must Check During Every Release

Architects evaluate:

- Platform direction
- Scalability changes
- Security implications
- Integration impacts
- Data architecture changes
- Performance enhancements

Questions they ask:

- Can this reduce custom code?
- Can this improve security?
- Can this simplify architecture?
- Should existing solutions be redesigned?

---

### 18. What Happens to Existing Customizations?

Generally Salesforce maintains backward compatibility.

Existing customizations usually continue working.

Examples:

- Apex Classes
- Triggers
- Flows
- Validation Rules
- LWCs
- Visualforce Pages
- Integrations

However:

- Deprecated features may eventually be removed
- Security updates may require code changes
- Older API versions may become outdated

Therefore testing remains essential.

---

### 19. API Versions and Releases

Each release introduces new API versions.

Example:

```
API v64
API v65
API v66
```

New versions may include:

- New endpoints
- New fields
- New objects
- New capabilities

Developers can often choose when to migrate to newer versions.

Benefits:

- Controlled adoption
- Better compatibility
- Reduced upgrade risk

---

### 20. Sandbox Strategy for Release Testing

Recommended approach:

```
Production
    ↓
Full Sandbox
    ↓
Partial Sandbox
    ↓
Developer Sandbox
```

Testing process:

1. Upgrade preview sandbox
2. Run automated tests
3. Execute manual testing
4. Validate integrations
5. Review critical updates
6. Fix issues
7. Prepare production rollout

---

### 21. Typical Enterprise Release Readiness Process

#### Step 1

Read Release Notes.

#### Step 2

Identify relevant changes.

#### Step 3

Review Critical Updates.

#### Step 4

Test in Preview Sandbox.

#### Step 5

Execute regression testing.

#### Step 6

Validate integrations.

#### Step 7

Train users if required.

#### Step 8

Monitor production after upgrade.

---

### 22. Real-World Example

Suppose a company uses:

- Sales Cloud
- Service Cloud
- Apex
- LWC
- MuleSoft integrations
- Agentforce

A new Summer release arrives.

The team:

1. Reads Release Notes
2. Reviews AI updates
3. Reviews Apex changes
4. Tests flows
5. Tests integrations
6. Verifies LWCs
7. Checks security updates
8. Trains support users
9. Monitors production after rollout

Only after successful validation do they fully adopt new features.

---

### 23. Common Interview Questions

#### What is a Salesforce release?

A platform update delivered by Salesforce that includes new features, fixes, security updates, and enhancements.

#### How many Salesforce releases occur annually?

Three:

- Spring
- Summer
- Winter

#### Why are preview sandboxes important?

They allow organizations to test upcoming releases before production upgrades.

#### What are Release Notes?

Official Salesforce documentation describing changes included in a release.

#### What are Critical Updates?

Platform changes that are initially optional but eventually become mandatory.

#### Why should developers test every release?

To ensure Apex, Flows, LWCs, integrations, and security configurations continue functioning correctly.

---

### 24. Summary

Salesforce release cycles are the mechanism through which Salesforce continuously delivers improvements to all organizations.

Key facts:

- Salesforce provides 3 major releases every year.
- Releases are named Spring, Summer, and Winter.
- Every release introduces new features, fixes, APIs, and security enhancements.
- Preview sandboxes allow early testing.
- Release Notes describe all changes.
- Critical Updates require special attention.
- Developers, admins, and architects should test every release before production rollout.
- Release management is a fundamental responsibility in Salesforce projects.
