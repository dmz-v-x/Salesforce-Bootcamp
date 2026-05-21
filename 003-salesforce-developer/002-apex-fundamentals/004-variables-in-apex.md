## Variables in Apex

### 1. What Is a Variable?

A variable is a named container that stores data in memory while a program is running.

Think of a variable like a labeled box.

Example:

```text
Box Label: name
Value Inside: Himanshu
```

Visual representation:

```text
name
 └── "Himanshu"
```

Instead of remembering the actual value every time, we use the variable name.

---

### 2. Why Do We Need Variables?

Imagine writing:

```apex
System.debug('Himanshu');
System.debug('Himanshu');
System.debug('Himanshu');
System.debug('Himanshu');
```

If the value changes:

```text
Himanshu → Rahul
```

You must update it everywhere.

Instead:

```apex
String name = 'Himanshu';

System.debug(name);
System.debug(name);
System.debug(name);
```

Only one place needs updating.

---

### 3. Variable Syntax

General syntax:

```apex
DataType variableName = value;
```

Example:

```apex
String name = 'Himanshu';
```

Breaking it down:

```apex
String name = 'Himanshu';
```

| Part | Meaning |
|----------|----------|
| String | Data type |
| name | Variable name |
| = | Assignment operator |
| 'Himanshu' | Value |
| ; | Statement terminator |

---

### 4. Reading a Variable Declaration

Example:

```apex
Integer age = 25;
```

Read as:

```text
Create a variable named age
that can store Integer values
and assign 25 to it
```

---

### 5. What Happens Internally?

Code:

```apex
String company = 'Infosys';
```

Conceptually:

```text
Memory
 └── company → Infosys
```

Salesforce runtime allocates memory and stores the value.

---

### 6. Data Type Matters

Variables must have a type.

Example:

```apex
String name = 'John';
```

Allowed:

```text
Text values
```

Not allowed:

```apex
String name = 100;
```

Reason:

```text
100 is Integer
name expects String
```

Type mismatch error.

---

### 7. Common Primitive Data Types

#### String

Stores text.

```apex
String firstName = 'John';
String city = 'Bangalore';
String company = 'Infosys';
```

---

#### Integer

Stores whole numbers.

```apex
Integer age = 25;
Integer quantity = 10;
Integer score = 500;
```

---

#### Long

Stores very large whole numbers.

```apex
Long population = 8000000000L;
```

---

#### Decimal

Stores decimal values.

```apex
Decimal salary = 55000.75;
Decimal discount = 10.5;
```

---

#### Double

Stores floating-point numbers.

```apex
Double percentage = 99.99;
```

---

#### Boolean

Stores true or false.

```apex
Boolean isActive = true;
Boolean isDeleted = false;
```

---

#### Date

Stores only date.

```apex
Date today = Date.today();
```

---

#### Datetime

Stores date and time.

```apex
Datetime nowTime = Datetime.now();
```

---

#### Time

Stores only time.

```apex
Time meetingTime = Time.newInstance(10,30,0,0);
```

---

#### Id

Stores Salesforce record IDs.

```apex
Id accountId = '001XXXXXXXXXXXXXXX';
```

---

### 8. Variable Naming Rules

Valid:

```apex
String firstName;
String accountName;
Integer totalAmount;
```

Invalid:

```apex
String 1name;
String first-name;
String class;
```

Rules:

- Must start with letter or underscore
- Cannot start with number
- Cannot contain hyphen
- Cannot use reserved keywords

---

### 9. Naming Best Practices

Bad:

```apex
String a;
String b;
String c;
```

Good:

```apex
String customerName;
Decimal totalPrice;
Boolean isPremiumCustomer;
```

Variable names should explain purpose.

---

### 10. Variable Declaration

Creating variable without value:

```apex
String name;
Integer age;
Boolean isActive;
```

Only declaration happens.

No value assigned yet.

---

### 11. Variable Initialization

Assigning value:

```apex
String name = 'Rahul';
```

This is declaration + initialization.

---

### 12. Variable Assignment

Value can change later.

```apex
String city = 'Delhi';

city = 'Mumbai';
```

Result:

```text
city → Mumbai
```

Old value replaced.

---

### 13. Multiple Assignments

```apex
Integer count = 10;

count = 20;

count = 30;
```

Final value:

```text
30
```

Only latest value remains.

---

### 14. Using Variables

```apex
String name = 'John';

System.debug(name);
```

Output:

```text
John
```

Variable value gets retrieved.

---

### 15. Variable-to-Variable Assignment

```apex
String firstName = 'John';

String anotherName = firstName;
```

Result:

```text
firstName  → John
anotherName → John
```

---

### 16. Concatenating Variables

Combining text.

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

### 17. Variables in Calculations

```apex
Integer price = 100;
Integer quantity = 5;

Integer total = price * quantity;
```

Result:

```text
500
```

---

### 18. Variables Can Store Formula Results

```apex
Integer a = 10;
Integer b = 20;

Integer result = a + b;
```

Result:

```text
30
```

---

### 19. Default Values

Local variables:

```apex
Integer age;
```

Cannot be used until assigned.

Example:

```apex
System.debug(age);
```

Compilation error.

Must initialize first.

---

### 20. Variable Scope

Scope means where a variable can be accessed.

Example:

```apex
public class TestClass {

    public static void show() {

        String name = 'John';

    }

}
```

Variable exists only inside method.

Outside:

```apex
name
```

Not accessible.

---

### 21. Method Scope Example

```apex
public static void calculate() {

    Integer total = 100;

    System.debug(total);

}
```

Valid.

Outside method:

```apex
System.debug(total);
```

Invalid.

---

### 22. Class Variables

```apex
public class Employee {

    String employeeName = 'John';

}
```

Variable belongs to object.

---

### 23. Static Variables

```apex
public class Counter {

    public static Integer count = 0;

}
```

Shared across all instances during transaction.

---

### 24. Final Variables

Constant values.

```apex
final Integer MAX_LIMIT = 100;
```

Cannot change later.

---

### 25. Variables with Salesforce Objects

```apex
Account acc = new Account();
```

Variable type:

```text
Account
```

Variable:

```text
acc
```

Stores Account object.

---

### 26. Example: Account Record

```apex
Account acc = new Account();

acc.Name = 'Infosys';

insert acc;
```

Variable:

```text
acc
```

contains Account record data.

---

### 27. Variables with Lists

```apex
List<String> cities =
new List<String>();
```

Variable:

```text
cities
```

Stores collection.

---

### 28. Variables with Maps

```apex
Map<Id, Account> accountMap =
new Map<Id, Account>();
```

Variable:

```text
accountMap
```

Stores key-value pairs.

---

### 29. Variables with Sets

```apex
Set<String> skills =
new Set<String>();
```

Variable:

```text
skills
```

Stores unique values.

---

### 30. Real-World Salesforce Example

Lead assignment logic:

```apex
String leadSource = 'Website';
Integer score = 85;
Boolean isQualified = true;
```

Variables store information used for business decisions.

---

### 31. Practice Example 1

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

### 32. Practice Example 2

Predict output:

```apex
Integer a = 10;
Integer b = 20;

Integer result = a + b;

System.debug(result);
```

Answer:

```text
30
```

---

### 33. Practice Example 3

Predict output:

```apex
String city = 'Delhi';

city = 'Mumbai';

System.debug(city);
```

Answer:

```text
Mumbai
```

---

### 34. Practice Example 4

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

### 35. Practice Example 5

Predict output:

```apex
String first = 'Sales';
String second = 'force';

String result = first + second;

System.debug(result);
```

Answer:

```text
Salesforce
```

---

### 36. Practice Example 6

Predict Output

```apex
Integer x = 10;

x = x + 5;

System.debug(x);
```

Answer:

```text
15
```

Explanation:

```text
x = 10

x = 10 + 5

x = 15
```

---

### 37. Practice Example 7

Predict Output

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

### 38. Practice Example 8

Predict Output

```apex
String firstName = 'John';
String lastName = 'Doe';

String fullName =
firstName + ' ' + lastName;

System.debug(fullName);
```

Answer:

```text
John Doe
```

---

### 39. Practice Example 9

What is stored?

```apex
Account acc = new Account();

acc.Name = 'ABC Technologies';
```

Answer:

```text
Variable: acc

Contains:
Account object

Name:
ABC Technologies
```

---

### 40. Practice Example 10

Predict Output

```apex
Integer a = 5;
Integer b = 3;

Integer result = a * b;

System.debug(result);
```

Answer:

```text
15
```

---

### 41. Common Beginner Mistakes

#### Forgetting Data Type

Wrong:

```apex
name = 'John';
```

Correct:

```apex
String name = 'John';
```

---

#### Type Mismatch

Wrong:

```apex
Integer age = '25';
```

Correct:

```apex
Integer age = 25;
```

---

#### Using Variable Before Assignment

Wrong:

```apex
Integer age;

System.debug(age);
```

Correct:

```apex
Integer age = 25;

System.debug(age);
```

---

#### Poor Naming

Bad:

```apex
Integer x;
```

Better:

```apex
Integer customerAge;
```

---

### 42. Final Summary

A variable is a named memory location used to store data during Apex execution. Every variable has a data type that determines what kind of values it can hold. Variables can store primitive values such as strings, numbers, booleans, dates, and IDs, as well as complex objects like Accounts, Contacts, Lists, Maps, and Sets. Variables can be declared, initialized, reassigned, passed between methods, used in calculations, and referenced throughout business logic. Understanding variables is the foundation for learning conditions, loops, methods, classes, collections, triggers, and advanced Apex development.
