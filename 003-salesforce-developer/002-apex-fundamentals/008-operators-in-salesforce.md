## Operators in Apex 

### 1. What Are Operators?

An operator is a special symbol that tells Apex to perform an operation on one or more values.

Example:

```apex
Integer result = 10 + 20;
```

Operator:

```apex
+
```

Instruction:

```text
Add 10 and 20
```

Result:

```text
30
```

---

### 2. Why Do We Need Operators?

Without operators, programming would be impossible.

We constantly need to:

```text
Add values
Subtract values
Compare values
Check conditions
Assign values
Increment counters
Combine conditions
```

Operators perform these tasks.

---

### 3. Real-World Analogy

Imagine a calculator.

Buttons:

```text
+
-
*
/
=
%
```

These symbols perform operations.

Operators in Apex work similarly.

Example:

```apex
5 + 3
```

Calculator:

```text
8
```

Apex:

```text
8
```

---

### 4. Categories of Operators in Apex

Major operator categories:

```text
1. Arithmetic Operators
2. Assignment Operators
3. Comparison (Relational) Operators
4. Logical Operators
5. Increment & Decrement Operators
6. Conditional (Ternary) Operator
7. Equality Operators
8. Instanceof Operator
```

Visual:

```text
Operators
│
├── Arithmetic
├── Assignment
├── Comparison
├── Logical
├── Increment/Decrement
├── Conditional
├── Equality
└── Instanceof
```

---

# Arithmetic Operators

### 5. What Are Arithmetic Operators?

Used for mathematical calculations.

Operators:

```text
+
-
*
/
%
```

---

## Addition Operator (+)

### 6. Purpose

Adds values.

Example:

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

### 7. Multiple Addition Examples

```apex
5 + 5
```

Result:

```text
10
```

---

```apex
100 + 50
```

Result:

```text
150
```

---

```apex
Decimal price = 100.50;
Decimal tax = 10.50;

Decimal total = price + tax;
```

Result:

```text
111.00
```

---

## Subtraction Operator (-)

### 8. Purpose

Subtracts values.

Example:

```apex
Integer result = 50 - 20;
```

Result:

```text
30
```

---

### 9. More Examples

```apex
100 - 50
```

Result:

```text
50
```

---

```apex
25 - 10
```

Result:

```text
15
```

---

## Multiplication Operator (*)

### 10. Purpose

Multiplies values.

Example:

```apex
Integer result = 5 * 6;
```

Result:

```text
30
```

---

### 11. Examples

```apex
10 * 10
```

Result:

```text
100
```

---

```apex
20 * 3
```

Result:

```text
60
```

---

## Division Operator (/)

### 12. Purpose

Divides values.

Example:

```apex
Integer result = 20 / 5;
```

Result:

```text
4
```

---

### 13. Examples

```apex
100 / 10
```

Result:

```text
10
```

---

```apex
60 / 3
```

Result:

```text
20
```

---

### 14. Integer Division Gotcha

```apex
Integer result = 5 / 2;
```

Result:

```text
2
```

Not:

```text
2.5
```

Reason:

Both operands are Integer.

---

To get decimal:

```apex
Decimal result = 5.0 / 2;
```

Result:

```text
2.5
```

---

## Modulus Operator (%)

### 15. Purpose

Returns remainder.

Example:

```apex
Integer result = 10 % 3;
```

Result:

```text
1
```

Because:

```text
10 ÷ 3 = 3 remainder 1
```

---

### 16. Examples

```apex
15 % 2
```

Result:

```text
1
```

---

```apex
20 % 5
```

Result:

```text
0
```

---

### 17. Real-World Use

Checking even numbers:

```apex
if(number % 2 == 0)
```

Meaning:

```text
Even Number
```

---

# Assignment Operators

### 18. What Are Assignment Operators?

Used to assign values.

Basic operator:

```text
=
```

---

## Simple Assignment (=)

### 19. Example

```apex
Integer age = 25;
```

Meaning:

```text
Store 25 in age
```

---

### 20. More Examples

```apex
String name = 'John';
```

---

```apex
Boolean active = true;
```

---

```apex
Decimal salary = 50000;
```

---

## Addition Assignment (+=)

### 21. Example

```apex
Integer total = 10;

total += 5;
```

Equivalent:

```apex
total = total + 5;
```

Result:

```text
15
```

---

## Subtraction Assignment (-=)

### 22. Example

```apex
Integer total = 20;

total -= 5;
```

Result:

```text
15
```

---

## Multiplication Assignment (*=)

### 23. Example

```apex
Integer value = 10;

value *= 2;
```

Result:

```text
20
```

---

## Division Assignment (/=)

### 24. Example

```apex
Integer value = 20;

value /= 2;
```

Result:

```text
10
```

---

# Comparison (Relational) Operators

### 25. What Are Comparison Operators?

Compare two values.

Result always:

```text
true
or
false
```

Operators:

```text
>
<
>=
<=
```

---

## Greater Than (>)

### 26. Example

```apex
10 > 5
```

Result:

```text
true
```

---

### 27. More Examples

```apex
50 > 100
```

Result:

```text
false
```

---

## Less Than (<)

### 28. Example

```apex
5 < 10
```

Result:

```text
true
```

---

## Greater Than or Equal (>=)

### 29. Example

```apex
10 >= 10
```

Result:

```text
true
```

---

```apex
20 >= 10
```

Result:

```text
true
```

---

## Less Than or Equal (<=)

### 30. Example

```apex
5 <= 10
```

Result:

```text
true
```

---

# Equality Operators

## Equal To (==)

### 31. Purpose

Checks whether values are equal.

Example:

```apex
10 == 10
```

Result:

```text
true
```

---

### 32. Examples

```apex
5 == 10
```

Result:

```text
false
```

---

```apex
'John' == 'John'
```

Result:

```text
true
```

---

## Not Equal (!=)

### 33. Purpose

Checks whether values differ.

Example:

```apex
10 != 20
```

Result:

```text
true
```

---

### 34. Examples

```apex
10 != 10
```

Result:

```text
false
```

---

```apex
'John' != 'Rahul'
```

Result:

```text
true
```

---

# Logical Operators

### 35. What Are Logical Operators?

Used to combine conditions.

Operators:

```text
&&
||
!
```

---

## Logical AND (&&)

### 36. Rule

All conditions must be true.

Example:

```apex
true && true
```

Result:

```text
true
```

---

### 37. Examples

```apex
10 > 5 && 20 > 10
```

Result:

```text
true
```

---

```apex
10 > 5 && 5 > 20
```

Result:

```text
false
```

---

### 38. Real World Example

```apex
if(age >= 18 && isVerified)
```

Meaning:

```text
Adult
AND
Verified
```

Both required.

---

## Logical OR (||)

### 39. Rule

At least one condition must be true.

Example:

```apex
true || false
```

Result:

```text
true
```

---

### 40. Examples

```apex
10 > 5 || 5 > 20
```

Result:

```text
true
```

---

```apex
false || false
```

Result:

```text
false
```

---

### 41. Real World Example

```apex
if(isAdmin || isManager)
```

Meaning:

```text
Admin OR Manager
```

Either works.

---

## Logical NOT (!)

### 42. Purpose

Reverses boolean value.

Example:

```apex
!true
```

Result:

```text
false
```

---

### 43. Examples

```apex
!false
```

Result:

```text
true
```

---

```apex
Boolean active = false;

!active
```

Result:

```text
true
```

---

# Increment & Decrement Operators

## Increment (++)

### 44. Purpose

Increase value by 1.

Example:

```apex
Integer count = 5;

count++;
```

Result:

```text
6
```

---

### 45. Equivalent

```apex
count = count + 1;
```

---

## Decrement (--)

### 46. Purpose

Decrease value by 1.

Example:

```apex
Integer count = 5;

count--;
```

Result:

```text
4
```

---

### 47. Equivalent

```apex
count = count - 1;
```

---

# Conditional (Ternary) Operator

### 48. Purpose

Short form of if-else.

Syntax:

```apex
condition ? value1 : value2
```

---

### 49. Example

```apex
Integer age = 20;

String result =
age >= 18
?
'Adult'
:
'Minor';
```

Result:

```text
Adult
```

---

### 50. Equivalent If Else

```apex
if(age >= 18)
{
    result = 'Adult';
}
else
{
    result = 'Minor';
}
```

---

# Instanceof Operator

### 51. Purpose

Checks object type.

Example:

```apex
Object obj =
new Account();
```

---

### 52. Example

```apex
Boolean result =
obj instanceof Account;
```

Result:

```text
true
```

---

# Operator Precedence

### 53. What Is Precedence?

Determines execution order.

Example:

```apex
2 + 3 * 4
```

Executed as:

```text
3 * 4 = 12

2 + 12 = 14
```

Result:

```text
14
```

---

### 54. Using Parentheses

```apex
(2 + 3) * 4
```

Execution:

```text
2 + 3 = 5

5 * 4 = 20
```

Result:

```text
20
```

---

# Practice Examples

### 55. Practice Example 1

Predict output:

```apex
Integer result = 10 + 20;

System.debug(result);
```

Answer:

```text
30
```

---

### 56. Practice Example 2

Predict output:

```apex
Integer result = 50 - 20;

System.debug(result);
```

Answer:

```text
30
```

---

### 57. Practice Example 3

Predict output:

```apex
Integer result = 5 * 6;

System.debug(result);
```

Answer:

```text
30
```

---

### 58. Practice Example 4

Predict output:

```apex
Integer result = 20 / 4;

System.debug(result);
```

Answer:

```text
5
```

---

### 59. Practice Example 5

Predict output:

```apex
Integer result = 10 % 3;

System.debug(result);
```

Answer:

```text
1
```

---

### 60. Practice Example 6

Predict output:

```apex
System.debug(10 > 5);
```

Answer:

```text
true
```

---

### 61. Practice Example 7

Predict output:

```apex
System.debug(10 == 10);
```

Answer:

```text
true
```

---

### 62. Practice Example 8

Predict output:

```apex
System.debug(
10 > 5 && 20 > 10
);
```

Answer:

```text
true
```

---

### 63. Practice Example 9

Predict output:

```apex
Boolean active = false;

System.debug(!active);
```

Answer:

```text
true
```

---

### 64. Practice Example 10

Predict output:

```apex
Integer count = 10;

count++;

System.debug(count);
```

Answer:

```text
11
```

---

### 65. Practice Example 11

Predict output:

```apex
Integer x = 10;

x += 5;

System.debug(x);
```

Answer:

```text
15
```

---

### 66. Practice Example 12

Predict output:

```apex
System.debug(
5 > 10 || 20 > 10
);
```

Answer:

```text
true
```

---

### 67. Practice Example 13

Predict output:

```apex
Integer result =
2 + 3 * 4;

System.debug(result);
```

Answer:

```text
14
```

---

### 68. Practice Example 14

Predict output:

```apex
Integer result =
(2 + 3) * 4;

System.debug(result);
```

Answer:

```text
20
```

---

### 69. Practice Example 15

Predict output:

```apex
String result =
10 > 5
?
'Yes'
:
'No';

System.debug(result);
```

Answer:

```text
Yes
```

---

## 70. Final Summary

Operators are special symbols that perform actions on values and variables. Apex provides arithmetic operators (`+`, `-`, `*`, `/`, `%`) for calculations, assignment operators (`=`, `+=`, `-=`, `*=`, `/=`) for storing values, comparison operators (`>`, `<`, `>=`, `<=`) for comparisons, equality operators (`==`, `!=`) for checking equality, logical operators (`&&`, `||`, `!`) for combining conditions, increment/decrement operators (`++`, `--`) for changing counters, the conditional (ternary) operator (`? :`) for concise decisions, and the `instanceof` operator for type checking. Operators are used in almost every Apex program, including calculations, validations, business rules, loops, triggers, Flows, integrations, and enterprise application logic.
