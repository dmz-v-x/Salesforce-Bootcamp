## Data Types in Apex — Complete Step-by-Step Guide

### 1. What Is a Data Type?

Before understanding data types, first understand a simple question:

When we create a variable, how does Salesforce know what kind of value we want to store?

Example:

```apex
String name = 'John';
```

How does Salesforce know:

```text
John = Text
```

and not:

```text
Number
Date
Boolean
```

Answer:

Because we specified a **Data Type**.

A data type tells Salesforce:

```text
What kind of data can be stored
How much memory is needed
What operations are allowed
How the value should behave
```

---

### 2. Why Do We Need Data Types?

Imagine Salesforce allowed any value in any variable.

Example:

```apex
Integer age = 'John';
```

Questions arise:

```text
Is John a number?
Can we add 10 to John?
Can we divide John by 2?
```

Makes no sense.

Data types prevent such problems.

They ensure:

```text
Data consistency
Type safety
Better performance
Fewer bugs
```

---

### 3. Real World Analogy

Imagine a supermarket.

Different containers store different things:

```text
Water Bottle → Water
Milk Packet → Milk
Rice Bag → Rice
Gas Cylinder → Gas
```

You cannot store:

```text
50kg rice in a water bottle
```

Similarly:

```text
Integer → Numbers
String → Text
Boolean → True/False
Date → Dates
```

Each variable type has a specific purpose.

---

### 4. Categories of Data Types in Apex

Apex data types are broadly divided into:

```text
1. Primitive Data Types
2. Non-Primitive Data Types
```

Visual:

```text
Data Types
│
├── Primitive
│   ├── Integer
│   ├── Long
│   ├── Decimal
│   ├── Double
│   ├── String
│   ├── Boolean
│   ├── Date
│   ├── Datetime
│   ├── Time
│   └── Id
│
└── Non-Primitive
    ├── Objects
    ├── Lists
    ├── Sets
    ├── Maps
    ├── Classes
    └── Enums
```

---

# Primitive Data Types

### 5. What Are Primitive Data Types?

Primitive types store a single value.

Examples:

```text
25
John
true
2026-05-21
```

One variable = one value.

---

## String Data Type

### 6. What Is String?

String stores text.

Examples:

```text
John
Salesforce
Infosys
Hello World
```

Example:

```apex
String name = 'John';
```

Memory:

```text
name → John
```

---

### 7. Multiple String Examples

```apex
String company = 'Infosys';

String city = 'Bangalore';

String country = 'India';

String email = 'john@gmail.com';
```

---

### 8. String Operations

Concatenation:

```apex
String firstName = 'John';

String lastName = 'Doe';

String fullName = firstName + ' ' + lastName;
```

Result:

```text
John Doe
```

---

### 9. String Methods

Length:

```apex
String name = 'Salesforce';

System.debug(name.length());
```

Output:

```text
10
```

Uppercase:

```apex
System.debug(name.toUpperCase());
```

Output:

```text
SALESFORCE
```

Lowercase:

```apex
System.debug(name.toLowerCase());
```

Output:

```text
salesforce
```

---

## Integer Data Type

### 10. What Is Integer?

Stores whole numbers.

Examples:

```text
1
10
500
9999
```

Not allowed:

```text
10.5
99.99
```

Example:

```apex
Integer age = 25;
```

---

### 11. Integer Examples

```apex
Integer quantity = 100;

Integer score = 95;

Integer employeeCount = 2500;

Integer totalOrders = 500;
```

---

### 12. Integer Arithmetic

Addition:

```apex
Integer a = 10;
Integer b = 20;

Integer result = a + b;
```

Output:

```text
30
```

---

Subtraction:

```apex
Integer result = 20 - 10;
```

Output:

```text
10
```

---

Multiplication:

```apex
Integer result = 10 * 5;
```

Output:

```text
50
```

---

Division:

```apex
Integer result = 20 / 5;
```

Output:

```text
4
```

---

## Long Data Type

### 13. What Is Long?

Long stores very large whole numbers.

Example:

```apex
Long population = 8000000000L;
```

Used when Integer range is insufficient.

Examples:

```text
Population
Bank transaction counts
Large IDs
Analytics data
```

---

## Decimal Data Type

### 14. What Is Decimal?

Stores precise decimal values.

Example:

```apex
Decimal price = 99.99;
```

Used for:

```text
Money
Tax
Discount
Financial calculations
```

---

### 15. Decimal Examples

```apex
Decimal salary = 55000.75;

Decimal gst = 18.5;

Decimal discount = 10.25;
```

---

### 16. Decimal Arithmetic

```apex
Decimal amount = 1000.50;

Decimal tax = 100.25;

Decimal total = amount + tax;
```

Output:

```text
1100.75
```

---

## Double Data Type

### 17. What Is Double?

Stores floating-point values.

Example:

```apex
Double pi = 3.14159;
```

Used for:

```text
Scientific calculations
Engineering calculations
Measurements
```

Example:

```apex
Double radius = 5.5;
```

---

## Boolean Data Type

### 18. What Is Boolean?

Stores only:

```text
true
false
```

Nothing else.

---

### 19. Boolean Examples

```apex
Boolean isActive = true;

Boolean isDeleted = false;

Boolean isPremiumCustomer = true;
```

---

### 20. Boolean Usage

```apex
Boolean isLoggedIn = true;

if(isLoggedIn) {
    System.debug('Access Granted');
}
```

Output:

```text
Access Granted
```

---

## Date Data Type

### 21. What Is Date?

Stores only:

```text
Year
Month
Day
```

No time.

Example:

```apex
Date today = Date.today();
```

Output:

```text
2026-05-21
```

---

### 22. Creating Dates

```apex
Date joiningDate =
Date.newInstance(2026, 5, 21);
```

Result:

```text
2026-05-21
```

---

### 23. Date Operations

Add days:

```apex
Date today = Date.today();

Date futureDate =
today.addDays(10);
```

---

Add months:

```apex
today.addMonths(2);
```

---

Add years:

```apex
today.addYears(1);
```

---

## Datetime Data Type

### 24. What Is Datetime?

Stores:

```text
Date + Time
```

Example:

```apex
Datetime currentTime =
Datetime.now();
```

Output:

```text
2026-05-21 14:30:00
```

---

### 25. Datetime Example

```apex
Datetime meeting =
Datetime.newInstance(
2026,
5,
21,
10,
30,
0
);
```

---

## Time Data Type

### 26. What Is Time?

Stores only time.

Example:

```apex
Time officeStart =
Time.newInstance(
9,
0,
0,
0
);
```

Output:

```text
09:00 AM
```

---

### 27. Time Examples

```apex
Time lunchTime =
Time.newInstance(
13,
0,
0,
0
);

Time meetingTime =
Time.newInstance(
15,
30,
0,
0
);
```

---

## Id Data Type

### 28. What Is Id?

Stores Salesforce Record IDs.

Example:

```apex
Id accountId =
'001XXXXXXXXXXXXXXX';
```

Used for:

```text
Account IDs
Contact IDs
Lead IDs
Opportunity IDs
```

---

### 29. Id Example

```apex
Account acc =
[
 SELECT Id
 FROM Account
 LIMIT 1
];

Id accountId = acc.Id;
```

---

# Non-Primitive Data Types

### 30. What Are Non-Primitive Types?

They store more complex data.

Examples:

```text
Account Records
Lists
Maps
Sets
Custom Objects
Custom Classes
```

---

## Object Data Type

### 31. Object Example

```apex
Account acc =
new Account();
```

Variable:

```text
acc
```

stores an Account object.

---

### 32. Setting Fields

```apex
Account acc =
new Account();

acc.Name = 'Infosys';
```

Object now contains:

```text
Name = Infosys
```

---

## List Data Type

### 33. What Is List?

Stores multiple values in order.

Example:

```apex
List<String> cities =
new List<String>();
```

---

### 34. Adding Values

```apex
cities.add('Delhi');

cities.add('Mumbai');

cities.add('Bangalore');
```

Result:

```text
[Delhi, Mumbai, Bangalore]
```

---

## Set Data Type

### 35. What Is Set?

Stores unique values.

Example:

```apex
Set<String> skills =
new Set<String>();
```

---

### 36. Duplicate Example

```apex
skills.add('Apex');

skills.add('Apex');

skills.add('LWC');
```

Result:

```text
[Apex, LWC]
```

Duplicate removed.

---

## Map Data Type

### 37. What Is Map?

Stores:

```text
Key → Value
```

pairs.

Example:

```apex
Map<Integer,String> students =
new Map<Integer,String>();
```

---

### 38. Map Example

```apex
students.put(1,'John');

students.put(2,'Rahul');
```

Result:

```text
1 → John

2 → Rahul
```

---

# Practice Examples

### 39. Practice Example 1

Predict output:

```apex
String name = 'John';

System.debug(name);
```

Answer:

```text
John
```

---

### 40. Practice Example 2

Predict output:

```apex
Integer a = 10;
Integer b = 20;

System.debug(a+b);
```

Answer:

```text
30
```

---

### 41. Practice Example 3

Predict output:

```apex
Boolean isActive = true;

System.debug(isActive);
```

Answer:

```text
true
```

---

### 42. Practice Example 4

Predict output:

```apex
Decimal price = 99.50;

Decimal tax = 10.50;

System.debug(price + tax);
```

Answer:

```text
110.00
```

---

### 43. Practice Example 5

Predict output:

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

### 44. Practice Example 6

Predict output:

```apex
Set<String> tech =
new Set<String>();

tech.add('Apex');

tech.add('Apex');

System.debug(tech);
```

Answer:

```text
(Apex)
```

Only one value stored.

---

### 45. Practice Example 7

Predict output:

```apex
Map<Integer,String> data =
new Map<Integer,String>();

data.put(1,'Salesforce');

System.debug(data);
```

Answer:

```text
{1=Salesforce}
```

---

### 46. Practice Example 8

Identify Data Types

```apex
String city = 'Delhi';
Integer age = 25;
Boolean active = true;
Decimal salary = 55000.75;
```

Answers:

```text
city → String
age → Integer
active → Boolean
salary → Decimal
```

---

### 47. Practice Example 9

Will this compile?

```apex
Integer age = '25';
```

Answer:

```text
No
```

Reason:

```text
String assigned to Integer
```

Type mismatch.

---

### 48. Practice Example 10

Will this compile?

```apex
Boolean isAdmin = false;
```

Answer:

```text
Yes
```

Valid Boolean assignment.

---

## Final Summary

A Data Type defines what kind of value a variable can store and what operations can be performed on it. Apex provides primitive data types such as String, Integer, Long, Decimal, Double, Boolean, Date, Datetime, Time, and Id for storing single values. It also provides non-primitive types such as Objects, Lists, Sets, Maps, Classes, and Enums for storing complex data structures. Choosing the correct data type is one of the most important foundations of Apex programming because it affects memory usage, validation, calculations, database operations, and overall code reliability.
