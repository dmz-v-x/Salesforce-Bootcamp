## SOQL SELECT Statement in Salesforce 

### 1. Goal of This Lesson

By the end of this lesson, you will understand:

- What SOQL is
- What the SELECT keyword does
- How Salesforce stores data
- How to query records using SELECT
- How to execute SOQL in Apex
- How to test everything in your Salesforce Developer Org
- Real-world business examples
- Common mistakes beginners make

---

### 2. What is SOQL?

SOQL stands for:

Structured Object Query Language

It is Salesforce's query language used to retrieve data from Salesforce objects.

Think of it as asking Salesforce:

"Show me the records I need."

Examples:

- Show all Accounts
- Show all Contacts
- Show all Opportunities
- Show Accounts from India
- Show Opportunities worth more than ₹1,00,000

SOQL only retrieves data.

It does not insert, update, or delete records.

---

### 3. What Does SELECT Mean?

The SELECT keyword tells Salesforce:

"I want to retrieve these fields."

General syntax:

```sql
SELECT Field1, Field2
FROM ObjectName
```

Example:

```sql
SELECT Name
FROM Account
```

Meaning:

"Salesforce, give me the Name field from Account records."

---

### 4. Understanding with a Real Business Example

Imagine a company called:

ABC Technologies

Inside Salesforce Sales Cloud they have:

Accounts:

| Account Name |
|------------|
| Infosys |
| TCS |
| Wipro |

When sales representatives open Salesforce they can see these Accounts.

Internally Salesforce stores data like:

| Id | Name |
|-----|------|
| 001AAA | Infosys |
| 001BBB | TCS |
| 001CCC | Wipro |

Now suppose management asks:

"Show all company names."

SOQL:

```sql
SELECT Name
FROM Account
```

Result:

| Name |
|--------|
| Infosys |
| TCS |
| Wipro |

---

### 5. First Thing To Create In Your Developer Org

Create some sample Accounts.

Navigate to:

```text
App Launcher
    ↓
Sales
    ↓
Accounts
```

Create these records:

Account 1

```text
Account Name = Infosys
```

Account 2

```text
Account Name = TCS
```

Account 3

```text
Account Name = Wipro
```

Save all three.

Now you have real data to query.

---

### 6. Running Your First SOQL Query

Open:

```text
Gear Icon
    ↓
Developer Console
```

Inside Developer Console:

```text
Query Editor
```

Enter:

```sql
SELECT Name
FROM Account
```

Click:

```text
Execute
```

You should see:

```text
Infosys
TCS
Wipro
```

Congratulations.

You just executed your first SOQL query.

---

### 7. Understanding Each Part

Query:

```sql
SELECT Name
FROM Account
```

Breaking it down:

SELECT

```text
Retrieve data
```

Name

```text
Retrieve Name field
```

FROM

```text
Which object to query
```

Account

```text
Salesforce Account object
```

Visualized:

```text
SELECT → What data?
FROM   → From where?
```

Example:

```sql
SELECT Name
FROM Account
```

means

```text
Get Name
From Account
```

---

### 8. Retrieving Multiple Fields

You can request multiple fields.

Example:

```sql
SELECT Id, Name, Type
FROM Account
```

Meaning:

```text
Give me:
- Id
- Name
- Type

from Account records
```

Possible result:

| Id | Name | Type |
|------|------|------|
|001AAA|Infosys|Customer|
|001BBB|TCS|Partner|
|001CCC|Wipro|Customer|

---

### 9. Why SELECT Only Needed Fields?

Bad:

```sql
SELECT Id, Name, Type, Industry, Phone, Website, OwnerId
FROM Account
```

when you only need Name.

Good:

```sql
SELECT Name
FROM Account
```

Reason:

- Faster query
- Less memory
- Better Apex performance
- Better governor limit usage

Professional developers only retrieve fields they need.

---

### 10. Executing SOQL Inside Apex

Now let's use Apex.

Open:

```text
Developer Console
    ↓
Debug
    ↓
Open Execute Anonymous Window
```

Paste:

```apex
List<Account> accounts =
[
    SELECT Name
    FROM Account
];

System.debug(accounts);
```

Execute.

---

### 11. What Happens Internally?

Step 1

SOQL runs:

```sql
SELECT Name
FROM Account
```

Step 2

Salesforce retrieves:

```text
Infosys
TCS
Wipro
```

Step 3

Creates Account objects.

Conceptually:

```apex
Account a1 = new Account();
a1.Name = 'Infosys';

Account a2 = new Account();
a2.Name = 'TCS';

Account a3 = new Account();
a3.Name = 'Wipro';
```

Step 4

Stores them inside List.

```apex
List<Account> accounts
```

Step 5

Debug prints records.

---

### 12. Accessing Individual Records

Example:

```apex
List<Account> accounts =
[
    SELECT Name
    FROM Account
];
```

Access first record:

```apex
System.debug(accounts[0].Name);
```

Output:

```text
Infosys
```

Access second:

```apex
System.debug(accounts[1].Name);
```

Output:

```text
TCS
```

---

### 13. Using Loop with SELECT

Very common in real projects.

Example:

```apex
List<Account> accounts =
[
    SELECT Name
    FROM Account
];

for(Account acc : accounts)
{
    System.debug(acc.Name);
}
```

Output:

```text
Infosys
TCS
Wipro
```

---

### 14. Real-World Sales Team Example

Suppose sales manager wants all customer accounts.

Query:

```sql
SELECT Name, Type
FROM Account
```

Apex:

```apex
List<Account> accounts =
[
    SELECT Name, Type
    FROM Account
];

for(Account acc : accounts)
{
    System.debug(
        'Name: ' + acc.Name +
        ', Type: ' + acc.Type
    );
}
```

Possible output:

```text
Name: Infosys, Type: Customer
Name: TCS, Type: Partner
Name: Wipro, Type: Customer
```

---

### 15. Querying Contacts

Create Contacts:

Contact 1

```text
First Name = Raj
Last Name = Sharma
```

Contact 2

```text
First Name = Amit
Last Name = Patel
```

Query:

```sql
SELECT FirstName, LastName
FROM Contact
```

Result:

```text
Raj Sharma
Amit Patel
```

Apex:

```apex
List<Contact> contacts =
[
    SELECT FirstName, LastName
    FROM Contact
];

for(Contact c : contacts)
{
    System.debug(
        c.FirstName + ' ' +
        c.LastName
    );
}
```

---

### 16. Querying Opportunities

Create an Opportunity.

Example:

```text
Opportunity Name = CRM Deal
Amount = 100000
Stage = Prospecting
```

Query:

```sql
SELECT Name, Amount
FROM Opportunity
```

Result:

```text
CRM Deal
100000
```

Apex:

```apex
List<Opportunity> opportunities =
[
    SELECT Name, Amount
    FROM Opportunity
];

for(Opportunity opp : opportunities)
{
    System.debug(
        opp.Name +
        ' : ' +
        opp.Amount
    );
}
```

---

### 17. Single Record Query

Suppose you know only one Account exists.

```apex
Account acc =
[
    SELECT Name
    FROM Account
    LIMIT 1
];

System.debug(acc.Name);
```

Result:

```text
Infosys
```

---

### 18. Why LIMIT Is Useful

Without limit:

```sql
SELECT Name
FROM Account
```

Could return:

```text
10
100
1000
100000
```

records.

With limit:

```sql
SELECT Name
FROM Account
LIMIT 5
```

Only first 5 records returned.

Useful for:

- Testing
- Debugging
- Performance
- Large datasets

---

### 19. Common Beginner Mistakes

#### Mistake 1

Wrong object name

Wrong:

```sql
SELECT Name
FROM Accounts
```

Correct:

```sql
SELECT Name
FROM Account
```

Object API name must be exact.

---

#### Mistake 2

Wrong field name

Wrong:

```sql
SELECT AccountName
FROM Account
```

Correct:

```sql
SELECT Name
FROM Account
```

Use actual field API names.

---

#### Mistake 3

Forgetting comma

Wrong:

```sql
SELECT Id Name
FROM Account
```

Correct:

```sql
SELECT Id, Name
FROM Account
```

---

#### Mistake 4

Accessing field not queried

Wrong:

```apex
List<Account> accounts =
[
    SELECT Name
    FROM Account
];

System.debug(accounts[0].Type);
```

Error:

```text
Field Type was not queried
```

Correct:

```apex
List<Account> accounts =
[
    SELECT Name, Type
    FROM Account
];
```

---

### 20. Complete Practice Exercise

Step 1

Create Accounts:

```text
Infosys
TCS
Wipro
```

Step 2

Run Query Editor:

```sql
SELECT Id, Name
FROM Account
```

Step 3

Run Execute Anonymous:

```apex
List<Account> accounts =
[
    SELECT Id, Name
    FROM Account
];

for(Account acc : accounts)
{
    System.debug(
        'Account Id: ' +
        acc.Id +
        ' Name: ' +
        acc.Name
    );
}
```

Step 4

Check Logs.

You should see all account names printed.

This is exactly how SOQL SELECT is used daily by Salesforce developers in real-world Apex code.

---

### 21. What You Have Learned

You now understand:

- What SOQL is
- Why SOQL exists
- What SELECT does
- How Salesforce retrieves data
- Query Editor execution
- Apex SOQL syntax
- List<Account> result handling
- Accessing fields
- Looping through query results
- Querying Accounts
- Querying Contacts
- Querying Opportunities
- LIMIT usage
- Common beginner mistakes
- Real-world Salesforce examples

You have learned the foundation upon which every advanced SOQL concept is built.
