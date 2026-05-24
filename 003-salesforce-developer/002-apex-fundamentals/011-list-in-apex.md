## List in Apex

### 1. What Is a List?

A List is a collection data structure that stores multiple values in a single variable.

Instead of storing one value:

```apex
String city = 'Delhi';
```

a List can store many values:

```apex
List<String> cities =
new List<String>();

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

### 2. Why Do We Need Lists?

Imagine storing 100 city names.

Without List:

```apex
String city1 = 'Delhi';
String city2 = 'Mumbai';
String city3 = 'Bangalore';
...
String city100 = 'Pune';
```

Problems:

```text
Too many variables
Hard to maintain
Hard to process
Hard to loop
```

With List:

```apex
List<String> cities =
new List<String>();
```

Store all values in one collection.

---

### 3. Real-World Analogy

Think about a shopping basket.

Basket contains:

```text
Milk
Bread
Butter
Rice
Eggs
```

One basket:

```text
Multiple items
```

Similarly:

```apex
List<String> items
```

stores multiple values together.

---

### 4. List Characteristics

Apex Lists:

```text
Store Multiple Values
Maintain Order
Allow Duplicates
Dynamic Size
Indexed Access
Can Store Objects
```

---

### 5. List Visualization

Example:

```apex
List<String> cities =
new List<String>();

cities.add('Delhi');
cities.add('Mumbai');
cities.add('Bangalore');
```

Visual:

```text
Index   Value

0       Delhi

1       Mumbai

2       Bangalore
```

Every element has an index.

---

### 6. What Is an Index?

Index is the position of an element.

Lists start from:

```text
0
```

not:

```text
1
```

Example:

```text
0 → Delhi
1 → Mumbai
2 → Bangalore
```

---

### 7. List Syntax

General syntax:

```apex
List<DataType> variableName =
new List<DataType>();
```

Example:

```apex
List<String> cities =
new List<String>();
```

---

### 8. Breaking Down Syntax

```apex
List<String> cities =
new List<String>();
```

Meaning:

| Part | Meaning |
|----------|----------|
| List | Collection type |
| String | Element type |
| cities | Variable name |
| new | Create object |
| List<String>() | Empty list |

---

### 9. Empty List Creation

```apex
List<String> cities =
new List<String>();
```

Current state:

```text
[]
```

No elements.

---

### 10. Adding Elements

Method:

```apex
add()
```

Example:

```apex
cities.add('Delhi');
```

Result:

```text
[
 Delhi
]
```

---

### 11. Adding Multiple Elements

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

### 12. Duplicate Values Allowed

```apex
cities.add('Delhi');

cities.add('Delhi');
```

Result:

```text
[
 Delhi,
 Delhi
]
```

Lists allow duplicates.

---

### 13. Direct Initialization

Instead of add():

```apex
List<String> cities =
new List<String>
{
    'Delhi',
    'Mumbai',
    'Bangalore'
};
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

### 14. Accessing Elements

Use index.

Example:

```apex
cities[0]
```

Output:

```text
Delhi
```

---

### 15. More Examples

```apex
cities[1]
```

Output:

```text
Mumbai
```

---

```apex
cities[2]
```

Output:

```text
Bangalore
```

---

### 16. Storing Retrieved Value

```apex
String city =
cities[0];
```

Result:

```text
city → Delhi
```

---

### 17. Updating Element

Example:

```apex
cities[1] = 'Chennai';
```

Before:

```text
Delhi
Mumbai
Bangalore
```

After:

```text
Delhi
Chennai
Bangalore
```

---

### 18. List Size

Method:

```apex
size()
```

Example:

```apex
cities.size();
```

Result:

```text
3
```

---

### 19. Empty List Size

```apex
List<String> cities =
new List<String>();

cities.size();
```

Result:

```text
0
```

---

### 20. Remove Element

Method:

```apex
remove(index)
```

Example:

```apex
cities.remove(1);
```

Before:

```text
Delhi
Mumbai
Bangalore
```

After:

```text
Delhi
Bangalore
```

---

### 21. Remove First Element

```apex
cities.remove(0);
```

Removes:

```text
Delhi
```

---

### 22. Clear Entire List

Method:

```apex
clear()
```

Example:

```apex
cities.clear();
```

Result:

```text
[]
```

---

### 23. Check If List Is Empty

Method:

```apex
isEmpty()
```

Example:

```apex
cities.isEmpty();
```

Output:

```text
true
```

if list has no elements.

---

### 24. Contains Method

Method:

```apex
contains()
```

Example:

```apex
cities.contains('Delhi');
```

Output:

```text
true
```

---

### 25. Contains Example

```apex
cities.contains('Pune');
```

Output:

```text
false
```

---

### 26. Iterating Through List

Loop:

```apex
for(String city : cities)
{
    System.debug(city);
}
```

Output:

```text
Delhi
Mumbai
Bangalore
```

---

### 27. Traditional For Loop

```apex
for(Integer i=0;
    i<cities.size();
    i++)
{
    System.debug(
        cities[i]
    );
}
```

---

### 28. List of Integers

```apex
List<Integer> marks =
new List<Integer>();
```

Add:

```apex
marks.add(90);

marks.add(80);

marks.add(70);
```

Result:

```text
[
 90,
 80,
 70
]
```

---

### 29. Integer Calculation Example

```apex
Integer total = 0;

for(Integer mark : marks)
{
    total += mark;
}
```

Result:

```text
240
```

---

### 30. List of Decimal

```apex
List<Decimal> prices =
new List<Decimal>();
```

Example:

```apex
prices.add(100.50);

prices.add(200.75);
```

---

### 31. List of Boolean

```apex
List<Boolean> flags =
new List<Boolean>();
```

Example:

```apex
flags.add(true);

flags.add(false);
```

---

### 32. List of Date

```apex
List<Date> holidays =
new List<Date>();
```

Example:

```apex
holidays.add(
Date.today()
);
```

---

### 33. List of Id

```apex
List<Id> accountIds =
new List<Id>();
```

Common in triggers.

---

### 34. List of Accounts

```apex
List<Account> accounts =
new List<Account>();
```

Stores Account records.

---

### 35. Adding Account Records

```apex
Account acc =
new Account(
    Name='Infosys'
);

accounts.add(acc);
```

---

### 36. Multiple Account Records

```apex
accounts.add(
new Account(
Name='Infosys'
));

accounts.add(
new Account(
Name='TCS'
));
```

---

### 37. Access Account Record

```apex
accounts[0].Name
```

Output:

```text
Infosys
```

---

### 38. SOQL Returns Lists

Most common usage.

```apex
List<Account> accounts =
[
 SELECT Id,
        Name
 FROM Account
];
```

Query returns:

```text
Multiple Records
```

Stored in List.

---

### 39. Why SOQL Returns List?

Because query may return:

```text
1 Record
10 Records
100 Records
1000 Records
```

Need collection.

---

### 40. Loop Through Query Results

```apex
for(Account acc :
    accounts)
{
    System.debug(
        acc.Name
    );
}
```

---

### 41. List Clone

Method:

```apex
clone()
```

Example:

```apex
List<String> copy =
cities.clone();
```

Creates duplicate list.

---

### 42. Sort List

Method:

```apex
sort()
```

Example:

```apex
cities.sort();
```

Before:

```text
Mumbai
Delhi
Bangalore
```

After:

```text
Bangalore
Delhi
Mumbai
```

---

### 43. Reverse Order

Method:

```apex
cities.reverse();
```

Reverses list order.

---

### 44. Nested Lists

List inside list.

Example:

```apex
List<List<Integer>>
matrix =
new List<List<Integer>>();
```

Represents:

```text
Rows and Columns
```

---

### 45. Common Salesforce Usage

Lists are heavily used in:

```text
SOQL Results
Bulk Triggers
Batch Apex
Queueable Apex
Flows
Integrations
REST APIs
Data Processing
```

---

### 46. Bulk Trigger Example

```apex
trigger AccountTrigger
on Account
(after insert)
{
    List<Account> accounts =
    Trigger.new;
}
```

Trigger.new itself is a List.

---

### 47. Governor Limit Friendly Processing

Bad:

```apex
Process one record at a time
```

Good:

```apex
Process entire List
```

Bulkification relies heavily on Lists.

---

### 48. Common Beginner Mistake

Wrong:

```apex
cities[5]
```

when list size is:

```text
3
```

Error:

```text
List Index Out Of Bounds
```

---

### 49. Safe Access

```apex
if(cities.size() > 5)
{
    System.debug(
        cities[5]
    );
}
```

Safe.

---

### 50. Null List Problem

Wrong:

```apex
List<String> cities;

cities.add('Delhi');
```

Error:

```text
Null Pointer Exception
```

---

Correct:

```apex
List<String> cities =
new List<String>();

cities.add('Delhi');
```

---

## Practice Examples

### 51. Practice Example 1

Predict Output

```apex
List<String> cities =
new List<String>();

cities.add('Delhi');

cities.add('Mumbai');

System.debug(cities);
```

Answer:

```text
(Delhi, Mumbai)
```

---

### 52. Practice Example 2

Predict Output

```apex
List<String> cities =
new List<String>
{
    'Delhi',
    'Mumbai'
};

System.debug(
cities[0]
);
```

Answer:

```text
Delhi
```

---

### 53. Practice Example 3

Predict Output

```apex
List<Integer> nums =
new List<Integer>();

nums.add(10);

nums.add(20);

System.debug(
nums.size()
);
```

Answer:

```text
2
```

---

### 54. Practice Example 4

Predict Output

```apex
List<String> cities =
new List<String>
{
    'Delhi',
    'Mumbai'
};

cities.remove(0);

System.debug(cities);
```

Answer:

```text
(Mumbai)
```

---

### 55. Practice Example 5

Predict Output

```apex
List<String> cities =
new List<String>();

System.debug(
cities.isEmpty()
);
```

Answer:

```text
true
```

---

### 56. Practice Example 6

Predict Output

```apex
List<String> cities =
new List<String>
{
    'Delhi',
    'Mumbai'
};

System.debug(
cities.contains(
'Mumbai'
)
);
```

Answer:

```text
true
```

---

### 57. Practice Example 7

Predict Output

```apex
List<Integer> marks =
new List<Integer>
{
    90,
    80,
    70
};

Integer total = 0;

for(Integer mark :
    marks)
{
    total += mark;
}

System.debug(total);
```

Answer:

```text
240
```

---

### 58. Practice Example 8

Predict Output

```apex
List<String> cities =
new List<String>
{
    'Mumbai',
    'Delhi'
};

cities.sort();

System.debug(cities);
```

Answer:

```text
(Bangalore-like alphabetical order)

(Delhi, Mumbai)
```

---

### 59. Practice Example 9

Will This Work?

```apex
List<String> cities;

cities.add('Delhi');
```

Answer:

```text
No
```

Reason:

```text
List not initialized
```

Null Pointer Exception.

---

### 60. Practice Example 10

Will This Work?

```apex
List<String> cities =
new List<String>();

cities.add('Delhi');
```

Answer:

```text
Yes
```

Valid.

---

### 61. Interview Questions

#### What Is a List?

Answer:

```text
An ordered collection
that stores multiple values
of the same type.
```

---

#### Does List Allow Duplicates?

Answer:

```text
Yes
```

Example:

```text
Delhi
Delhi
Mumbai
```

Valid.

---

#### Does List Maintain Order?

Answer:

```text
Yes
```

Insertion order preserved.

---

#### What Is First Index?

Answer:

```text
0
```

---

#### How To Get List Size?

```apex
list.size();
```

---

#### How To Check Empty List?

```apex
list.isEmpty();
```

---

#### How To Remove Element?

```apex
list.remove(index);
```

---

#### Most Common List Usage?

```text
SOQL query results
Trigger.new
Bulk processing
```

---

## 62. Final Summary

A List in Apex is an ordered collection that stores multiple values of the same type. Lists maintain insertion order, allow duplicate values, provide index-based access starting at index `0`, and dynamically grow or shrink as elements are added or removed. Lists can store primitive values such as Strings, Integers, Dates, and Booleans, as well as complex objects such as Accounts, Contacts, custom classes, and other collections. Lists are one of the most important data structures in Salesforce development because SOQL queries return Lists, triggers process Lists of records, bulkified code relies on Lists, and nearly every Apex application uses Lists for data processing, integrations, automation, and business logic.
