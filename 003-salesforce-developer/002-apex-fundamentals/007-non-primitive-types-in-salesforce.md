## Non-Primitive Types in Apex

### 1. What Are Non-Primitive Types?

Before learning non-primitive types, let's quickly recall primitive types.

Primitive types store a single value.

Examples:

```apex
String name = 'John';

Integer age = 25;

Boolean isActive = true;
```

Each variable stores only one value.

---

Non-primitive types are different.

They can store:

```text
Multiple values
Complex structures
Objects
Collections
Relationships
Custom logic
```

Examples:

```apex
Account acc;

List<Account> accounts;

Map<Id, Account> accountMap;

Set<String> skills;
```

These are all non-primitive types.

---

### 2. Why Do We Need Non-Primitive Types?

Imagine a company record.

Information:

```text
Company Name
Industry
Phone
Website
Revenue
Employees
Address
```

Can a String store all of this?

```apex
String company = ???;
```

No.

One primitive value is insufficient.

Therefore Salesforce provides complex data types.

---

### 3. Real World Analogy

Primitive:

```text
One Paper
```

Non-Primitive:

```text
Entire File Folder
```

Example:

```text
Primitive
--------
John

Non-Primitive
-------------
Name = John
Age = 25
City = Bangalore
Salary = 50000
```

Non-primitive types can hold many pieces of information together.

---

### 4. Categories of Non-Primitive Types

Major non-primitive types in Apex:

```text
Object
sObject
Custom Classes
List
Set
Map
Enum
```

Visual:

```text
Non Primitive Types
│
├── Objects
├── sObjects
├── Custom Classes
├── Lists
├── Sets
├── Maps
└── Enums
```

---

# Object Type

### 5. What Is an Object?

An object represents a real-world entity.

Examples:

```text
Account
Contact
Lead
Opportunity
Case
User
```

Each object contains multiple fields.

---

### 6. Account Object Example

```apex
Account acc = new Account();
```

Variable:

```text
acc
```

Stores:

```text
Account Object
```

Not a single value.

Entire object.

---

### 7. Setting Object Fields

```apex
Account acc = new Account();

acc.Name = 'Infosys';

acc.Phone = '1234567890';

acc.Website = 'www.infosys.com';
```

Visual:

```text
Account

Name     = Infosys
Phone    = 1234567890
Website  = www.infosys.com
```

One object contains multiple values.

---

### 8. Inserting Object Into Database

```apex
Account acc = new Account();

acc.Name = 'Infosys';

insert acc;
```

Object becomes a Salesforce record.

---

### 9. Contact Object Example

```apex
Contact con = new Contact();

con.FirstName = 'John';

con.LastName = 'Doe';
```

Visual:

```text
Contact

FirstName = John
LastName  = Doe
```

---

# sObject Type

### 10. What Is sObject?

sObject is the parent type of every Salesforce object.

Think:

```text
Object
  ↑
sObject
```

Examples:

```text
Account
Contact
Lead
Opportunity
Case
```

All inherit from:

```text
sObject
```

---

### 11. Generic sObject Example

```apex
sObject record =
new Account(
    Name='Infosys'
);
```

Variable type:

```text
sObject
```

Actual object:

```text
Account
```

---

### 12. Why Use sObject?

Useful when object type is unknown.

Example:

```text
Could be Account
Could be Contact
Could be Lead
```

Generic processing becomes possible.

---

# Custom Classes

### 13. What Is a Custom Class?

A class is a blueprint.

Example:

```apex
public class Employee {

    public String name;

    public Integer age;

}
```

Class defines structure.

---

### 14. Creating Objects From Class

```apex
Employee emp =
new Employee();
```

Object created.

---

### 15. Storing Values

```apex
emp.name = 'Rahul';

emp.age = 25;
```

Visual:

```text
Employee

name = Rahul
age  = 25
```

---

### 16. Real World Class Example

```apex
public class Student {

    public String name;

    public Integer marks;

    public String city;

}
```

Object:

```text
Name
Marks
City
```

all together.

---

# List Type

### 17. What Is a List?

List stores multiple values in order.

Think:

```text
Shopping List
```

Example:

```apex
List<String> cities =
new List<String>();
```

---

### 18. Adding Values

```apex
cities.add('Delhi');

cities.add('Mumbai');

cities.add('Bangalore');
```

Result:

```text
[
 Delhi,
 Mumbai,
 Bangalore
]
```

---

### 19. List Characteristics

List:

```text
Maintains Order
Allows Duplicates
Indexed
Dynamic Size
```

Example:

```apex
List<String> skills =
new List<String>();

skills.add('Apex');

skills.add('Apex');
```

Result:

```text
[Apex, Apex]
```

Duplicates allowed.

---

### 20. Accessing Elements

```apex
System.debug(
cities[0]
);
```

Output:

```text
Delhi
```

---

### 21. List of Integers

```apex
List<Integer> marks =
new List<Integer>();

marks.add(90);

marks.add(80);

marks.add(70);
```

Result:

```text
[90,80,70]
```

---

### 22. List of Accounts

```apex
List<Account> accounts =
new List<Account>();
```

Stores multiple Account records.

---

### 23. SOQL Result Is Usually a List

```apex
List<Account> accounts =
[
 SELECT Id, Name
 FROM Account
];
```

Multiple records returned.

Stored in List.

---

# Set Type

### 24. What Is a Set?

Set stores unique values.

Duplicates automatically removed.

---

### 25. Set Example

```apex
Set<String> skills =
new Set<String>();
```

---

### 26. Adding Values

```apex
skills.add('Apex');

skills.add('LWC');

skills.add('Apex');
```

Result:

```text
[
 Apex,
 LWC
]
```

Duplicate removed.

---

### 27. Why Use Set?

Useful for:

```text
Unique IDs
Unique Emails
Unique Skills
Unique Values
```

---

### 28. Set Example With IDs

```apex
Set<Id> accountIds =
new Set<Id>();
```

Stores unique record IDs.

Very common in triggers.

---

### 29. Set Contains Method

```apex
skills.contains('Apex');
```

Output:

```text
true
```

---

# Map Type

### 30. What Is a Map?

Map stores:

```text
Key → Value
```

pairs.

---

### 31. Real World Analogy

Dictionary:

```text
Word → Meaning
```

Student database:

```text
Roll Number → Name
```

---

### 32. Map Example

```apex
Map<Integer,String> students =
new Map<Integer,String>();
```

---

### 33. Adding Values

```apex
students.put(1,'John');

students.put(2,'Rahul');

students.put(3,'Amit');
```

Result:

```text
1 → John

2 → Rahul

3 → Amit
```

---

### 34. Retrieving Value

```apex
students.get(2);
```

Output:

```text
Rahul
```

---

### 35. Most Common Salesforce Map

```apex
Map<Id,Account> accountMap =
new Map<Id,Account>();
```

Key:

```text
Account Id
```

Value:

```text
Account Record
```

---

### 36. Map From Query

```apex
Map<Id,Account> accountMap =
new Map<Id,Account>(
[
 SELECT Id, Name
 FROM Account
]
);
```

Automatically creates:

```text
Id → Account
```

mapping.

---

### 37. Why Maps Are Fast

Without Map:

```text
Loop through 1000 records
Find matching record
```

With Map:

```text
Direct lookup
```

Very efficient.

---

# Enum Type

### 38. What Is Enum?

Enum represents a fixed set of values.

Example:

```apex
public enum Status {

    New,

    InProgress,

    Completed

}
```

---

### 39. Using Enum

```apex
Status currentStatus =
Status.Completed;
```

Only predefined values allowed.

---

### 40. Benefits Of Enum

Without enum:

```apex
String status =
'Completed';
```

Risk:

```apex
'complete'
'COMPLETED'
'compelted'
```

Typo possible.

---

With enum:

```apex
Status.Completed
```

Safe and controlled.

---

# Common Salesforce Collections

### 41. List vs Set vs Map

| Feature | List | Set | Map |
|----------|----------|----------|----------|
| Stores Multiple Values | Yes | Yes | Yes |
| Allows Duplicates | Yes | No | Key No |
| Maintains Order | Yes | No | No |
| Indexed Access | Yes | No | No |
| Key-Value Storage | No | No | Yes |
| Fast Lookup | Medium | Fast | Very Fast |

---

### 42. When To Use List?

Use when:

```text
Order matters
Duplicates allowed
Need index access
```

Examples:

```text
Student Marks
Cities
Products
Accounts
```

---

### 43. When To Use Set?

Use when:

```text
Only unique values needed
Duplicate removal required
Membership checking required
```

Examples:

```text
Emails
Record IDs
Usernames
Skills
```

---

### 44. When To Use Map?

Use when:

```text
Fast lookup required
Key-value relationship exists
```

Examples:

```text
Id → Account
Id → Contact
ProductId → Product
```

---

# Practice Examples

### 45. Practice Example 1

Predict Output

```apex
List<String> names =
new List<String>();

names.add('John');

names.add('Rahul');

System.debug(names);
```

Answer:

```text
(John, Rahul)
```

---

### 46. Practice Example 2

Predict Output

```apex
Set<String> skills =
new Set<String>();

skills.add('Apex');

skills.add('Apex');

System.debug(skills);
```

Answer:

```text
(Apex)
```

Duplicate removed.

---

### 47. Practice Example 3

Predict Output

```apex
Map<Integer,String> data =
new Map<Integer,String>();

data.put(1,'Salesforce');

System.debug(
data.get(1)
);
```

Answer:

```text
Salesforce
```

---

### 48. Practice Example 4

Predict Output

```apex
List<Integer> marks =
new List<Integer>();

marks.add(90);

marks.add(80);

System.debug(
marks[1]
);
```

Answer:

```text
80
```

---

### 49. Practice Example 5

Predict Output

```apex
Set<Integer> numbers =
new Set<Integer>();

numbers.add(10);

numbers.add(10);

numbers.add(20);
```

Answer:

```text
(10,20)
```

---

### 50. Practice Example 6

Identify Type

```apex
Account acc =
new Account();
```

Answer:

```text
Object Type
```

More specifically:

```text
Account sObject
```

---

### 51. Practice Example 7

Identify Type

```apex
Map<Id,Account> accountMap;
```

Answer:

```text
Map
```

---

### 52. Practice Example 8

Will This Compile?

```apex
List<String> names =
new List<String>();

names.add('John');
```

Answer:

```text
Yes
```

Valid List usage.

---

### 53. Practice Example 9

Will This Compile?

```apex
Set<Integer> values =
new Set<Integer>();

values.add(100);
```

Answer:

```text
Yes
```

Valid Set usage.

---

### 54. Practice Example 10

Predict Output

```apex
Map<Integer,String> students =
new Map<Integer,String>();

students.put(1,'John');

students.put(2,'Rahul');

System.debug(
students.get(2)
);
```

Answer:

```text
Rahul
```

---

## 55. Interview-Oriented Examples

### Example 1: Collect Unique Account IDs

```apex
Set<Id> accountIds =
new Set<Id>();

for(Contact con :
[
 SELECT AccountId
 FROM Contact
])
{
    accountIds.add(
        con.AccountId
    );
}
```

Purpose:

```text
Collect unique Account IDs
```

---

### Example 2: Query Accounts Into Map

```apex
Map<Id,Account> accountMap =
new Map<Id,Account>
(
[
 SELECT Id,
        Name
 FROM Account
]
);
```

Purpose:

```text
Fast Account lookup
```

---

### Example 3: Query Multiple Accounts

```apex
List<Account> accounts =
[
 SELECT Id,
        Name
 FROM Account
];
```

Purpose:

```text
Store multiple records
```

---

## 56. Final Summary

Non-primitive types are complex data types that can store multiple values, objects, relationships, and structured information. Apex provides several important non-primitive types including **Objects (Account, Contact, Lead, etc.)**, **sObject**, **Custom Classes**, **Lists**, **Sets**, **Maps**, and **Enums**. Lists are used for ordered collections and allow duplicates, Sets store only unique values, Maps store key-value pairs for fast lookups, Objects represent Salesforce records, Custom Classes model business entities, and Enums define fixed sets of allowed values. These types form the foundation of real-world Salesforce development because almost every trigger, Apex class, Flow integration, SOQL query result, and enterprise application relies heavily on them.
