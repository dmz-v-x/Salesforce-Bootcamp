## Primitive Types in Apex

### 1. What Are Primitive Types?

Primitive types are the most basic built-in data types provided by Apex.

They are used to store a **single value directly**.

Examples:

```text
John
25
99.99
true
2026-05-21
```

Each of these values can be stored using a primitive type.

---

### 2. Why Are Primitive Types Called "Primitive"?

The word primitive means:

```text
Basic
Fundamental
Building Block
```

Primitive types are the foundation of programming.

Everything more complex is built using them.

Example:

```apex
String name = 'John';
Integer age = 25;
Boolean isActive = true;
```

These are basic pieces of information.

---

### 3. Primitive vs Non-Primitive

Primitive:

```apex
Integer age = 25;
```

Stores:

```text
Single Value
```

Non-Primitive:

```apex
Account acc = new Account();
```

Stores:

```text
Object
Multiple Properties
Multiple Values
```

Comparison:

| Primitive | Non-Primitive |
|------------|------------|
| Stores single value | Stores complex data |
| Built into Apex | Can be custom or built-in |
| Simple | More complex |
| Examples: Integer, String | Examples: Account, List, Map |

---

### 4. List of Primitive Types in Apex

Apex provides these primitive types:

```text
String
Integer
Long
Decimal
Double
Boolean
Date
Datetime
Time
Id
Blob
```

These are the core primitive data types every Apex developer uses daily.

---

# String Type

### 5. What Is String?

String stores text.

Examples:

```text
John
Salesforce
India
Hello World
```

Example:

```apex
String name = 'John';
```

Memory representation:

```text
name → John
```

---

### 6. Multiple String Examples

```apex
String company = 'Infosys';

String city = 'Bangalore';

String country = 'India';

String technology = 'Salesforce';
```

---

### 7. String Concatenation

Combining strings:

```apex
String firstName = 'John';

String lastName = 'Doe';

String fullName =
firstName + ' ' + lastName;
```

Result:

```text
John Doe
```

---

### 8. String Methods

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

Contains:

```apex
System.debug(
name.contains('force')
);
```

Output:

```text
true
```

---

# Integer Type

### 9. What Is Integer?

Stores whole numbers.

Examples:

```text
1
10
100
5000
```

Not allowed:

```text
10.5
20.75
```

Example:

```apex
Integer age = 25;
```

---

### 10. Integer Examples

```apex
Integer quantity = 50;

Integer totalMarks = 500;

Integer employeeCount = 10000;

Integer totalOrders = 250;
```

---

### 11. Integer Arithmetic

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
Integer result = 50 - 20;
```

Output:

```text
30
```

---

Multiplication:

```apex
Integer result = 5 * 6;
```

Output:

```text
30
```

---

Division:

```apex
Integer result = 30 / 3;
```

Output:

```text
10
```

---

Modulo:

```apex
Integer result = 10 % 3;
```

Output:

```text
1
```

---

# Long Type

### 12. What Is Long?

Long stores very large whole numbers.

Used when Integer range is insufficient.

Example:

```apex
Long population = 8000000000L;
```

Notice:

```text
L
```

at the end.

It tells Apex this is a Long value.

---

### 13. Long Examples

```apex
Long totalViews = 5000000000L;

Long transactionCount = 9999999999L;

Long population = 1400000000L;
```

---

### 14. When To Use Long?

Use Long when dealing with:

```text
Population
Large counters
Analytics systems
Huge transaction numbers
Large identifiers
```

---

# Decimal Type

### 15. What Is Decimal?

Decimal stores precise decimal values.

Most common type for money.

Example:

```apex
Decimal salary = 55000.75;
```

---

### 16. Why Not Use Integer?

Integer:

```text
100
```

Cannot store:

```text
100.25
```

Decimal can.

---

### 17. Decimal Examples

```apex
Decimal amount = 1000.50;

Decimal tax = 18.75;

Decimal discount = 10.25;

Decimal price = 49999.99;
```

---

### 18. Decimal Arithmetic

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

### 19. Real Salesforce Example

Opportunity amount:

```apex
Decimal opportunityAmount =
250000.50;
```

Commission:

```apex
Decimal commission =
opportunityAmount * 0.10;
```

Result:

```text
25000.05
```

---

# Double Type

### 20. What Is Double?

Double stores floating-point numbers.

Example:

```apex
Double pi = 3.1415926535;
```

---

### 21. Double Examples

```apex
Double radius = 10.5;

Double distance = 250.78;

Double temperature = 37.5;
```

---

### 22. Decimal vs Double

Decimal:

```text
Financial calculations
High precision
```

Double:

```text
Scientific calculations
Measurements
Approximations
```

Example:

```apex
Decimal amount = 99.99;

Double pi = 3.14159;
```

---

# Boolean Type

### 23. What Is Boolean?

Boolean stores only:

```text
true
false
```

Nothing else.

---

### 24. Boolean Examples

```apex
Boolean isActive = true;

Boolean isDeleted = false;

Boolean isAdmin = true;

Boolean isPremium = false;
```

---

### 25. Boolean Usage

```apex
Boolean isLoggedIn = true;

if(isLoggedIn){
    System.debug('Access Granted');
}
```

Output:

```text
Access Granted
```

---

### 26. Real World Example

```apex
Boolean paymentReceived = true;
```

Decision:

```text
true
 ↓
Ship Product

false
 ↓
Do Not Ship Product
```

---

# Date Type

### 27. What Is Date?

Stores:

```text
Year
Month
Day
```

Only date.

No time.

---

### 28. Date Example

```apex
Date today = Date.today();
```

Output:

```text
2026-05-21
```

---

### 29. Creating Date

```apex
Date joiningDate =
Date.newInstance(
2026,
5,
21
);
```

Output:

```text
2026-05-21
```

---

### 30. Date Operations

Add days:

```apex
Date futureDate =
Date.today().addDays(10);
```

---

Add months:

```apex
Date.today().addMonths(2);
```

---

Add years:

```apex
Date.today().addYears(1);
```

---

# Datetime Type

### 31. What Is Datetime?

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
2026-05-21 15:30:00
```

---

### 32. Datetime Example

```apex
Datetime interviewTime =
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

### 33. Real World Examples

```text
Case Created Time
Lead Conversion Time
Login Time
Order Time
Payment Time
```

Usually stored as Datetime.

---

# Time Type

### 34. What Is Time?

Stores only time.

Example:

```apex
Time startTime =
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

### 35. Time Examples

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

### 36. Real World Usage

```text
Store Office Start Time
Store Meeting Time
Store Alarm Time
Store Appointment Time
```

---

# Id Type

### 37. What Is Id?

Stores Salesforce Record IDs.

Example:

```apex
Id accountId =
'001XXXXXXXXXXXXXXX';
```

---

### 38. Why Is Id Special?

Salesforce records have unique IDs.

Example:

```text
Account
001XXXXXXXXXXXXXXX

Contact
003XXXXXXXXXXXXXXX

Lead
00QXXXXXXXXXXXXXXX
```

The Id type is designed specifically for these values.

---

### 39. Id Example

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

# Blob Type

### 40. What Is Blob?

Blob stores binary data.

Examples:

```text
PDF
Image
Excel File
Word Document
Audio
Video
```

---

### 41. Blob Example

```apex
Blob data =
Blob.valueOf('Hello');
```

---

### 42. Common Blob Usage

Used in:

```text
File Uploads
Attachments
ContentVersion
Document Processing
API Integrations
```

---

# Practice Examples

### 43. Practice Example 1

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

### 44. Practice Example 2

Predict output:

```apex
Integer age = 25;

System.debug(age);
```

Answer:

```text
25
```

---

### 45. Practice Example 3

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

### 46. Practice Example 4

Predict output:

```apex
Decimal amount = 100.50;
Decimal tax = 10.50;

System.debug(amount+tax);
```

Answer:

```text
111.00
```

---

### 47. Practice Example 5

Predict output:

```apex
Boolean active = true;

System.debug(active);
```

Answer:

```text
true
```

---

### 48. Practice Example 6

Predict output:

```apex
String first = 'Sales';
String second = 'force';

System.debug(first+second);
```

Answer:

```text
Salesforce
```

---

### 49. Practice Example 7

Identify Type

```apex
Date today =
Date.today();
```

Answer:

```text
Date
```

---

### 50. Practice Example 8

Identify Type

```apex
Datetime nowTime =
Datetime.now();
```

Answer:

```text
Datetime
```

---

### 51. Practice Example 9

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

---

### 52. Practice Example 10

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

### 53. Practice Example 11

Predict output:

```apex
Integer x = 10;

x = x + 5;

System.debug(x);
```

Answer:

```text
15
```

---

### 54. Practice Example 12

Predict output:

```apex
Decimal salary = 50000;

salary = salary + 10000;

System.debug(salary);
```

Answer:

```text
60000
```

---

## Final Summary

Primitive types are the fundamental built-in data types of Apex used to store single values directly. Apex provides **String** for text, **Integer** and **Long** for whole numbers, **Decimal** and **Double** for decimal numbers, **Boolean** for true/false values, **Date** for dates, **Datetime** for date and time values, **Time** for time-only values, **Id** for Salesforce record identifiers, and **Blob** for binary data. Understanding primitive types is essential because every Apex program, trigger, class, Flow integration, and Salesforce application relies on them as the building blocks for storing and manipulating data.
