## Salesforce Company Settings

### 1. Introduction to Company Settings

Company Settings in Salesforce are used to configure organization-level settings.

These settings control how the Salesforce organization behaves globally.

Think of Company Settings as:

"Core configuration settings for the entire Salesforce organization."

These settings affect:
- Users
- Business processes
- Time calculations
- Language behavior
- Security
- Domains
- Calendars
- Holidays
- Fiscal reporting

Company Settings are usually configured by:
- Salesforce Administrators
- System Administrators
- Architects

---

### 2. Where to Find Company Settings

In Salesforce Setup:

Go to:

Setup → Company Settings

Inside this section, Salesforce provides multiple configuration areas.

---

## Business Hours

### 3. What are Business Hours

Business Hours define the official working hours of a company.

These hours are used by Salesforce for:
- Support processes
- SLA calculations
- Escalations
- Case management
- Entitlement tracking

---

### 4. Real-World Example of Business Hours

Suppose a company works:

- Monday to Friday
- 9 AM to 6 PM

A customer raises a support case at:
Friday 5 PM

If SLA says:
"Resolve within 4 business hours"

Salesforce calculates only business hours.

So:
- 1 hour counted on Friday
- Remaining 3 hours counted on Monday

This is why Business Hours are important.

---

### 5. Components of Business Hours

Business Hours configuration includes:

- Working days
- Start time
- End time
- Time zone
- Holidays

---

### 6. Multiple Business Hours

Large companies may have different working schedules.

Example:

India Support Team:
- 9 AM to 6 PM IST

US Support Team:
- 9 AM to 5 PM PST

Salesforce allows creation of multiple Business Hours records.

---

## Calendar Settings

### 7. What are Calendar Settings

Calendar Settings control scheduling and shared calendar functionality inside Salesforce.

These settings help users:
- Schedule events
- Manage resources
- Share calendars
- Coordinate teams

---

## Public Calendars and Resources

### 8. What are Public Calendars

Public Calendars are shared calendars accessible by multiple users.

They help organizations coordinate activities.

Example:
- Company event calendar
- Training calendar
- Leave calendar

---

### 9. Real-World Example of Public Calendars

Suppose HR schedules company interviews.

Instead of sending emails repeatedly, HR can maintain:

"Interview Calendar"

Everyone can see:
- Interview timings
- Meeting rooms
- Schedules

---

### 10. What are Resources

Resources represent shared assets or facilities.

Example:
- Meeting rooms
- Company vehicles
- Projectors
- Conference halls

Users can reserve these resources through Salesforce calendars.

---

### 11. Benefits of Public Calendars

Benefits include:
- Better scheduling
- Reduced conflicts
- Team coordination
- Resource management

---

## Company Information

### 12. What is Company Information

Company Information stores basic details about the Salesforce organization.

This includes:
- Organization name
- Organization ID
- Address
- Time zone
- Number of licenses
- Storage usage

---

### 13. Why Company Information is Important

Administrators use this section to:
- Monitor storage
- Check licenses
- Verify organization details
- Track edition type

---

### 14. Salesforce Organization ID

Every Salesforce org has a unique Organization ID.

This ID is important for:
- Integrations
- Support cases
- Deployments
- API operations

---

## Data Protection and Privacy

### 15. What is Data Protection and Privacy

This section manages privacy and compliance-related settings.

Modern companies must protect:
- Customer data
- Employee data
- Sensitive information

Salesforce provides settings to support:
- Data privacy
- Security compliance
- Regulatory requirements

---

### 16. Real-World Importance

Many countries have strict privacy laws.

Examples:
- GDPR in Europe
- Data protection laws in India
- HIPAA in healthcare

Companies must ensure customer data is handled securely.

---

### 17. Features Under Privacy Settings

Examples include:
- Data consent
- User privacy controls
- Data retention policies
- Cookie preferences
- Personal data management

---

## Fiscal Year

### 18. What is Fiscal Year

Fiscal Year represents the accounting year used by businesses.

Companies use fiscal years for:
- Financial reporting
- Revenue tracking
- Budget planning
- Quarterly reports

Important:
Fiscal year does not always match the calendar year.

---

### 19. Calendar Year vs Fiscal Year

Calendar Year:
- January to December

Fiscal Year:
Can vary.

Example:
- April to March
- July to June

Different companies choose different fiscal periods.

---

## Standard Fiscal Year

### 20. What is Standard Fiscal Year

Standard Fiscal Year follows a regular monthly structure.

Example:
- 12 months
- Standard quarters

Most businesses use this configuration.

---

### 21. Standard Fiscal Year Example

Example:

Fiscal Year:
April 2026 → March 2027

Quarters:
- Q1 → Apr-Jun
- Q2 → Jul-Sep
- Q3 → Oct-Dec
- Q4 → Jan-Mar

---

## Custom Fiscal Year

### 22. What is Custom Fiscal Year

Some businesses need non-standard accounting structures.

Salesforce allows Custom Fiscal Years.

Used when companies have:
- Uneven quarters
- Retail calendars
- Special accounting periods

---

### 23. Real-World Example of Custom Fiscal Year

Retail companies sometimes use:
4-4-5 calendar structure

Meaning:
- 4 weeks
- 4 weeks
- 5 weeks

This helps standardize retail reporting.

---

### 24. Important Limitation

Once Custom Fiscal Year is enabled:
- Reverting becomes difficult
- Certain configurations become restricted

So companies plan carefully before enabling it.

---

## Holidays

### 25. What are Holidays in Salesforce

Holidays represent non-working days.

Salesforce uses holidays together with:
- Business Hours
- SLA calculations
- Escalations

---

### 26. Holiday Example

Suppose:
- Saturday and Sunday are weekends
- Monday is a public holiday

If a support SLA spans Monday:
Salesforce skips that day in calculations.

---

### 27. Benefits of Holiday Configuration

Benefits:
- Accurate SLA tracking
- Proper support calculations
- Better workforce planning

---

## Language Settings

### 28. What are Language Settings

Language Settings control:
- Default language
- Translation behavior
- Localization

Salesforce supports multiple languages.

---

### 29. Why Language Settings Matter

Global companies have employees across different countries.

Example:
- India
- Japan
- Germany
- France

Different users may prefer different languages.

Salesforce allows localized user experiences.

---

### 30. Examples of Localization

Localization includes:
- Date formats
- Currency formats
- Number formats
- Language translations

Example:

US Format:
MM/DD/YYYY

India Format:
DD/MM/YYYY

---

## My Domain

### 31. What is My Domain

My Domain creates a custom Salesforce login domain for the organization.

Instead of generic Salesforce URLs, companies get custom branded URLs.

---

### 32. Example of My Domain

Without My Domain:
company.salesforce.com/randomURL

With My Domain:
mycompany.my.salesforce.com

---

### 33. Why My Domain is Important

My Domain is extremely important in Salesforce.

It enables:
- Branding
- Secure login
- Single Sign-On (SSO)
- Lightning Components
- Authentication customization

---

### 34. Real-World Importance of My Domain

Large companies often want branded login experiences.

Example:
Employees trust:
companyname.my.salesforce.com

More than random Salesforce URLs.

---

### 35. My Domain and Security

My Domain improves security by supporting:
- Identity providers
- Authentication systems
- Login policies

---

### 36. My Domain and Lightning Components

Certain Salesforce features require My Domain.

Especially:
- Lightning Web Components (LWC)
- Lightning Experience
- Authentication-based features

Without My Domain, some modern features may not work properly.

---
