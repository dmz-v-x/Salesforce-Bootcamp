## Type Casting in Apex

### 1. What Is Type Casting?

Type casting is the process of converting a value from one data type into another data type.

Example:

```apex
Integer age = 25;

String ageText = String.valueOf(age);
```

Before:

```text
Integer → 25
```

After:

```text
String → "25"
```

The value remains conceptually the same, but its data type changes.

---

### 2. Why Do We Need Type Casting?

Different parts of an application often expect different data types.

Example:

```apex
Integer age = 25;
```

Suppose we want:

```text
Display in UI
Send via API
Store in text field
Generate log message
```

Most of these require String values.

Therefore:

```apex
String ageText =
String.valueOf(age);
```

Type conversion becomes necessary.

---

### 3. Real World Analogy

Imagine:

```text
Water
```

stored in:

```text
Bottle
```

Now move same water into:

```text
Glass
```

Water remains the same.

Container changes.

Similarly:

```text
25
```

can be:

```text
Integer
String
Long
Decimal
Double
```

depending on conversion.

---

### 4. Why Can't Apex Automatically Convert Everything?

Suppose:

```apex
Integer age = 'John';
```

Questions:

```text
How does John become a number?
```

Impossible.

Therefore Apex enforces type safety.

You must explicitly convert when necessary.

---

### 5. Categories of Type Casting

In Apex:

```text
1. Primitive Type Conversion
2. Object Casting
3. Upcasting
4. Downcasting
5. sObject Casting
6. Collection Casting
```

---

## Primitive Type Conversion

### 6. Primitive Conversion Overview

Converting between:

```text
String
Integer
Long
Decimal
Double
Boolean
Date
Datetime
Id
```

is called primitive type conversion.

---

# Integer to String

### 7. Integer → String

Example:

```apex
Integer age = 25;

String text =
String.valueOf(age);
```

Result:

```text
"25"
```

---

### 8. Multiple Examples

```apex
Integer count = 100;

String value =
String.valueOf(count);
```

Result:

```text
"100"
```

---

```apex
Integer score = 500;

String text =
String.valueOf(score);
```

Result:

```text
"500"
```

---

### 9. Real World Example

```apex
Integer totalRecords = 150;

System.debug(
'Records: ' +
String.valueOf(totalRecords)
);
```

Output:

```text
Records: 150
```

---

# String to Integer

### 10. String → Integer

Example:

```apex
String ageText = '25';

Integer age =
Integer.valueOf(ageText);
```

Result:

```text
25
```

---

### 11. Multiple Examples

```apex
String quantity = '100';

Integer qty =
Integer.valueOf(quantity);
```

Result:

```text
100
```

---

```apex
String score = '999';

Integer result =
Integer.valueOf(score);
```

Result:

```text
999
```

---

### 12. Invalid Conversion Example

```apex
String name = 'John';

Integer age =
Integer.valueOf(name);
```

Runtime error.

Reason:

```text
John is not a valid Integer
```

---

# Integer to Decimal

### 13. Integer → Decimal

Example:

```apex
Integer age = 25;

Decimal value =
Decimal.valueOf(age);
```

Result:

```text
25.0
```

---

### 14. Examples

```apex
Integer marks = 90;

Decimal score =
Decimal.valueOf(marks);
```

Result:

```text
90.0
```

---

```apex
Integer quantity = 5;

Decimal qty =
Decimal.valueOf(quantity);
```

Result:

```text
5.0
```

---

# Decimal to Integer

### 15. Decimal → Integer

Example:

```apex
Decimal amount = 99.99;

Integer value =
amount.intValue();
```

Result:

```text
99
```

Notice:

```text
Decimal part removed
```

---

### 16. Examples

```apex
Decimal marks = 88.75;

Integer score =
marks.intValue();
```

Result:

```text
88
```

---

```apex
Decimal tax = 18.5;

Integer value =
tax.intValue();
```

Result:

```text
18
```

---

# String to Decimal

### 17. String → Decimal

Example:

```apex
String amount = '1500.75';

Decimal value =
Decimal.valueOf(amount);
```

Result:

```text
1500.75
```

---

### 18. Examples

```apex
String salary = '50000.50';

Decimal result =
Decimal.valueOf(salary);
```

---

```apex
String discount = '10.25';

Decimal value =
Decimal.valueOf(discount);
```

---

# Decimal to String

### 19. Decimal → String

Example:

```apex
Decimal amount = 100.50;

String text =
String.valueOf(amount);
```

Result:

```text
"100.50"
```

---

# Boolean Conversion

### 20. String → Boolean

Example:

```apex
String value = 'true';

Boolean result =
Boolean.valueOf(value);
```

Output:

```text
true
```

---

### 21. Example

```apex
String value = 'false';

Boolean result =
Boolean.valueOf(value);
```

Output:

```text
false
```

---

# Date Conversion

### 22. String → Date

Example:

```apex
String dateText =
'2026-05-21';

Date d =
Date.valueOf(dateText);
```

Result:

```text
2026-05-21
```

---

### 23. Date → String

Example:

```apex
Date today =
Date.today();

String text =
String.valueOf(today);
```

Result:

```text
"2026-05-21"
```

---

# Datetime Conversion

### 24. String → Datetime

Example:

```apex
String value =
'2026-05-21 10:30:00';

Datetime dt =
Datetime.valueOf(value);
```

---

### 25. Datetime → String

Example:

```apex
Datetime nowTime =
Datetime.now();

String value =
String.valueOf(nowTime);
```

---

# Id Conversion

### 26. String → Id

Example:

```apex
String accId =
'001XXXXXXXXXXXXXXX';

Id recordId =
(Id)accId;
```

Result:

```text
Valid Salesforce Id
```

---

### 27. Id → String

Example:

```apex
Id accountId =
'001XXXXXXXXXXXXXXX';

String text =
String.valueOf(accountId);
```

---

# Object Casting

### 28. What Is Object Casting?

Converting between related object types.

Most common in:

```text
Custom Classes
sObjects
Inheritance
Polymorphism
```

---

# Upcasting

### 29. What Is Upcasting?

Child object stored in parent reference.

Example:

```apex
public class Animal {

}
```

---

```apex
public class Dog
extends Animal {

}
```

---

### 30. Upcasting Example

```apex
Dog dog =
new Dog();

Animal animal =
dog;
```

Visual:

```text
Dog
 ↓
Animal Reference
```

Allowed automatically.

No explicit cast required.

---

### 31. Why Is Upcasting Safe?

Because:

```text
Every Dog IS an Animal
```

Therefore:

```apex
Animal animal = dog;
```

always valid.

---

# Downcasting

### 32. What Is Downcasting?

Parent reference converted back to child type.

Example:

```apex
Animal animal =
new Dog();
```

Now:

```apex
Dog dog =
(Dog)animal;
```

---

### 33. Why Cast Needed?

Because parent reference could point to:

```text
Dog
Cat
Bird
```

Compiler needs confirmation.

---

### 34. Downcasting Example

```apex
Animal animal =
new Dog();

Dog dog =
(Dog)animal;
```

Valid.

---

### 35. Invalid Downcast

```apex
Animal animal =
new Animal();

Dog dog =
(Dog)animal;
```

Runtime exception.

Reason:

```text
Animal is not Dog
```

---

# sObject Casting

### 36. Generic sObject Example

```apex
sObject record =
new Account(
    Name='Infosys'
);
```

---

### 37. Cast Back To Account

```apex
Account acc =
(Account)record;
```

Now:

```apex
acc.Name
```

can be accessed.

---

### 38. Why Use sObject Casting?

Useful when processing:

```text
Account
Contact
Lead
Opportunity
```

generically.

---

# Collection Casting

### 39. List Casting Example

```apex
List<sObject> records =
new List<sObject>();
```

Contains:

```text
Accounts
```

Need Account list:

```apex
List<Account> accounts =
(List<Account>)records;
```

---

### 40. Map Casting Example

```apex
Object data =
new Map<String,String>();
```

Cast:

```apex
Map<String,String> mapData =
(Map<String,String>)data;
```

---

# Common Salesforce Type Casting Examples

### 41. URL Parameter Example

URL values arrive as:

```text
String
```

Example:

```apex
String ageText = '25';
```

Need Integer:

```apex
Integer age =
Integer.valueOf(ageText);
```

---

### 42. Text Field To Number

Custom Field:

```text
Text
```

Contains:

```text
100
```

Convert:

```apex
Integer value =
Integer.valueOf(textField);
```

---

### 43. API Payload Example

API:

```json
{
  "amount":"5000.50"
}
```

Received:

```text
String
```

Convert:

```apex
Decimal amount =
Decimal.valueOf(value);
```

---

# Practice Examples

### 44. Practice Example 1

Predict Output

```apex
Integer age = 25;

String text =
String.valueOf(age);

System.debug(text);
```

Answer:

```text
25
```

Type:

```text
String
```

---

### 45. Practice Example 2

Predict Output

```apex
String ageText = '50';

Integer age =
Integer.valueOf(ageText);

System.debug(age);
```

Answer:

```text
50
```

---

### 46. Practice Example 3

Predict Output

```apex
String value = '100.50';

Decimal amount =
Decimal.valueOf(value);

System.debug(amount);
```

Answer:

```text
100.50
```

---

### 47. Practice Example 4

Predict Output

```apex
Decimal amount = 99.99;

Integer value =
amount.intValue();

System.debug(value);
```

Answer:

```text
99
```

---

### 48. Practice Example 5

Predict Output

```apex
String value = 'true';

Boolean result =
Boolean.valueOf(value);

System.debug(result);
```

Answer:

```text
true
```

---

### 49. Practice Example 6

Will This Work?

```apex
String name = 'John';

Integer age =
Integer.valueOf(name);
```

Answer:

```text
No
```

Runtime exception.

Reason:

```text
John is not numeric
```

---

### 50. Practice Example 7

Predict Output

```apex
Integer quantity = 10;

Decimal qty =
Decimal.valueOf(quantity);

System.debug(qty);
```

Answer:

```text
10.0
```

---

### 51. Practice Example 8

Predict Output

```apex
Date today =
Date.today();

String value =
String.valueOf(today);

System.debug(value);
```

Answer:

```text
Current date as String
```

---

### 52. Practice Example 9

Identify Casting Type

```apex
Animal animal =
new Dog();
```

Answer:

```text
Upcasting
```

---

### 53. Practice Example 10

Identify Casting Type

```apex
Dog dog =
(Dog)animal;
```

Answer:

```text
Downcasting
```

---

## 54. Common Beginner Mistakes

### Mistake 1

```apex
Integer age = '25';
```

Wrong.

Correct:

```apex
Integer age =
Integer.valueOf('25');
```

---

### Mistake 2

```apex
Integer age =
Integer.valueOf('John');
```

Invalid.

Reason:

```text
Not numeric
```

---

### Mistake 3

Unsafe Downcast:

```apex
Animal animal =
new Animal();

Dog dog =
(Dog)animal;
```

Fails at runtime.

---

### Mistake 4

Ignoring Null Values

```apex
String value = null;

Integer age =
Integer.valueOf(value);
```

Can throw exceptions.

Always validate first.

---

## 55. Final Summary

Type casting is the process of converting one data type into another. Apex supports primitive conversions such as String ↔ Integer, String ↔ Decimal, String ↔ Boolean, String ↔ Date, String ↔ Datetime, and Id ↔ String using methods like `valueOf()`, `String.valueOf()`, and `intValue()`. Apex also supports object casting through inheritance and polymorphism, including **upcasting** (child to parent), **downcasting** (parent to child), **sObject casting**, and collection casting. Type casting is heavily used in Salesforce development when processing user input, API payloads, URL parameters, SOQL results, dynamic Apex, generic sObject handling, and enterprise application logic.
