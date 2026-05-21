## Sales Pipeline

### 1. What is a Sales Pipeline?

A Sales Pipeline is a visual representation of all potential sales opportunities and the stages they move through before becoming actual customers.

In simple words:

```text
Potential Customer
        ↓
Lead
        ↓
Qualified Lead
        ↓
Opportunity
        ↓
Proposal
        ↓
Negotiation
        ↓
Closed Won
```

A Sales Pipeline shows:

- where every deal currently stands
- what actions need to be taken next
- how much potential revenue exists
- which deals are likely to close

Think of it as a "tracking system" for sales deals.

---

### 2. Why is it Called a Pipeline?

Imagine a water pipeline.

```text
Water Enters
      ↓
Moves Through Pipe
      ↓
Comes Out At End
```

Similarly:

```text
Potential Customer Enters
          ↓
Moves Through Sales Stages
          ↓
Becomes Customer
```

Not every deal reaches the end.

Some deals:

```text
Drop Out
Lose Interest
Choose Competitor
Lack Budget
```

Only some opportunities successfully flow through the pipeline and become revenue.

---

### 3. Why Companies Need a Sales Pipeline

Without a sales pipeline:

- salespeople forget follow-ups
- managers cannot track deals
- future revenue is unknown
- opportunities get lost
- sales process becomes chaotic

A pipeline provides visibility into the entire sales process.

---

### 4. Benefits of a Sales Pipeline

#### A. Track Every Deal

Sales teams know:

```text
Which customer?
Which stage?
Next action?
Expected revenue?
```

---

#### B. Revenue Forecasting

Management can estimate future revenue.

Example:

```text
Opportunity A = ₹5,00,000

Opportunity B = ₹10,00,000

Opportunity C = ₹15,00,000

Pipeline Value = ₹30,00,000
```

---

#### C. Better Follow-Ups

Salespeople can quickly identify:

```text
Customers waiting for proposal

Customers needing demos

Customers ready for negotiation
```

---

#### D. Performance Tracking

Managers can see:

```text
Deals Closed

Deals Lost

Conversion Rates

Salesperson Performance
```

---

### 5. Real-World Example

Suppose a company sells CRM software.

A new customer:

```text
ABC Technologies
```

shows interest.

The customer will move through multiple stages before purchasing.

That journey is called the Sales Pipeline.

---

## Typical Sales Pipeline Stages

### 6. Stage 1: Lead

Customer first expresses interest.

Example:

```text
Rahul Sharma

Company:
ABC Technologies

Interested In:
CRM Software
```

At this stage:

```text
Lead Created
```

---

### 7. Stage 2: Qualification

Salesperson contacts customer.

Questions asked:

```text
Budget Available?

Decision Maker?

Business Need?

Timeline?
```

If answers are positive:

```text
Qualified Lead
```

---

### 8. Stage 3: Opportunity Creation

Lead is converted.

Salesforce creates:

```text
Account

Contact

Opportunity
```

Opportunity example:

```text
CRM Implementation

Value:
₹10,00,000
```

Now the deal officially enters the sales pipeline.

---

### 9. Stage 4: Needs Analysis

Sales team understands customer requirements.

Example:

```text
500 Users

Sales Automation

Support Management

Reporting
```

Requirements are documented.

---

### 10. Stage 5: Proposal / Quote

Company sends pricing proposal.

Example:

```text
Software License:
₹8,00,000

Implementation:
₹2,00,000

Total:
₹10,00,000
```

Customer reviews the proposal.

---

### 11. Stage 6: Negotiation

Customer and company discuss:

```text
Pricing

Contract Terms

Support Services

Training
```

Possible outcome:

```text
Original:
₹10,00,000

Negotiated:
₹9,50,000
```

---

### 12. Stage 7: Closed Won

Customer accepts proposal.

Contract signed.

Opportunity stage:

```text
Closed Won
```

Meaning:

```text
Deal Successfully Closed
```

Revenue generated.

---

### 13. Stage 8: Closed Lost

Sometimes customer rejects proposal.

Possible reasons:

```text
No Budget

Selected Competitor

Project Cancelled

Requirements Changed
```

Opportunity stage:

```text
Closed Lost
```

Meaning:

```text
Deal Not Won
```

---

## Visual Sales Pipeline Example

### 14. Pipeline View

```text
Lead
(20 Records)
      ↓

Qualification
(15 Records)
      ↓

Needs Analysis
(10 Records)
      ↓

Proposal
(8 Records)
      ↓

Negotiation
(5 Records)
      ↓

Closed Won
(3 Records)
```

Notice how the number decreases at every stage.

This is called a Sales Funnel.

---

### 15. Why Pipeline Gets Smaller

Some prospects leave because:

```text
No Budget

No Urgency

Wrong Fit

Competitor Chosen

No Response
```

Therefore fewer opportunities reach the final stage.

---

## Sales Pipeline vs Sales Funnel

### 16. Important Difference

Many beginners confuse these terms.

| Sales Pipeline | Sales Funnel |
|----------|----------|
| Seller's perspective | Buyer's perspective |
| Tracks opportunities | Tracks customer journey |
| Focuses on deal stages | Focuses on conversion percentages |
| Used by sales teams | Used by marketing and sales |

---

### 17. Easy Way to Remember

Pipeline asks:

```text
Where is the deal?
```

Funnel asks:

```text
How many customers remain?
```

---

## Sales Pipeline in Salesforce

### 18. How Salesforce Manages Pipeline

Salesforce primarily uses:

```text
Opportunity Object
```

to manage sales pipelines.

Each opportunity contains:

```text
Customer

Deal Amount

Stage

Expected Close Date

Probability
```

---

### 19. Example Opportunity Record

```text
Opportunity Name:
CRM Project

Amount:
₹10,00,000

Stage:
Proposal

Close Date:
30 June

Probability:
70%
```

Salesforce tracks this automatically.

---

### 20. Opportunity Stages in Salesforce

Common stages:

```text
Prospecting
      ↓
Qualification
      ↓
Needs Analysis
      ↓
Proposal
      ↓
Negotiation
      ↓
Closed Won
```

Organizations can customize these stages.

---

### 21. Pipeline Reports

Salesforce can generate reports showing:

```text
Total Pipeline Value

Open Opportunities

Won Opportunities

Lost Opportunities

Revenue Forecasts
```

Managers use these reports for decision making.

---

### 22. Pipeline Dashboard Example

```text
Total Pipeline:
₹2 Crore

Open Opportunities:
25

Closed Won:
10

Closed Lost:
5

Expected Revenue:
₹75 Lakh
```

All this information comes from Opportunity records.

---

## Complete Demo Scenario

### 23. End-to-End Example

Customer:

```text
ABC Technologies
```

Journey:

```text
Website Inquiry
        ↓
Lead Created
        ↓
Qualified
        ↓
Opportunity Created
        ↓
Needs Analysis
        ↓
Proposal Sent
        ↓
Negotiation
        ↓
Closed Won
```

Deal Value:

```text
₹10,00,000
```

This opportunity successfully moved through the entire sales pipeline.

---

## Salesforce Free Account Practical

### 24. Goal

Create and manage your own sales pipeline using Opportunities.

---

### Step 1: Open Sales App

```text
App Launcher
      ↓
Sales
```

---

### Step 2: Create Lead

Navigate:

```text
Leads
     ↓
New
```

Create:

```text
Name:
Rahul Sharma

Company:
ABC Technologies
```

Save.

---

### Step 3: Convert Lead

Open Lead.

Click:

```text
Convert
```

Salesforce creates:

```text
Account

Contact

Opportunity
```

---

### Step 4: Open Opportunity

Navigate:

```text
Opportunities
```

Open the newly created opportunity.

---

### Step 5: Update Stage Sequentially

Move through stages one by one:

```text
Prospecting
```

Save.

Then:

```text
Qualification
```

Save.

Then:

```text
Needs Analysis
```

Save.

Then:

```text
Proposal
```

Save.

Then:

```text
Negotiation
```

Save.

Observe how the deal progresses through the pipeline.

---

### Step 6: Mark Closed Won

Update:

```text
Stage = Closed Won
```

Save.

You have successfully completed a sales pipeline.

---

### Step 7: Create Multiple Opportunities

Create additional opportunities:

```text
CRM Project
₹5,00,000

ERP Project
₹15,00,000

Support Contract
₹2,00,000
```

Place them in different stages.

This will simulate a real company pipeline.

---

### Step 8: View Opportunity List

Observe:

```text
Different Opportunities

Different Stages

Different Values
```

This is your sales pipeline.

---

### Step 9: Create Opportunity Report (Advanced)

Navigate:

```text
Reports
      ↓
New Report
      ↓
Opportunities
```

Generate report showing:

```text
Opportunity Name

Stage

Amount

Close Date
```

This is how managers monitor pipeline health.

---

### 25. Real-World Enterprise Example

A software company may have:

```text
100 Open Opportunities

Pipeline Value:
₹50 Crore
```

Management can immediately know:

- future revenue potential
- deals at risk
- sales team performance
- expected monthly revenue

All through the sales pipeline.
