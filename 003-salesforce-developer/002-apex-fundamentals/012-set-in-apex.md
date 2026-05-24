## Set in Apex

### 1. What Is a Set?

A Set is a collection data structure that stores **unique values only**.

Unlike a List:

```apex
List<String> cities =
new List<String>();

cities.add('Delhi');
cities.add('Delhi');
cities.add('Mumbai');
```

Result:

```text
[
 Delhi,
 Delhi,
 Mumbai
]
```

Duplicates are allowed.

---

A Set automatically removes duplicates.

Example:

```apex
Set<String> cities =
new Set<String>();

cities.add('Delhi');
cities.add('Delhi');
cities.add('Mumbai');
```

Result:

```text
[
 Delhi,
 Mumbai
]
```

Only unique values remain.

---

### 2. Why Do We Need Sets?

Suppose we have thousands of records.

Example:

```text
Account IDs

001AAA
001BBB
001AAA
001CCC
001BBB
```

Duplicate IDs exist.

If we use a Set:

```apex
Set<Id> accountIds =
new Set<Id>();
```

Result:

```text
001AAA
001BBB
001CCC
```

Duplicates automatically removed.

---

### 3. Real-World Analogy

Imagine an event registration system.

People registering:

```text
John
Rahul
John
Amit
Rahul
```

Should the same person be registered multiple times?

Usually:

```text
No
```

We want unique entries.

Set behaves similarly.

---

### 4. Set Characteristics

Apex Sets:

```text
Store Multiple Values
Store Unique Values Only
No Duplicate Values
Dynamic Size
Fast Lookup
No Index Access
No Guaranteed Ordering
```

---

### 5. List vs Set

Example:

List:

```apex
List<String> names =
new List<String>();

names.add('John');
names.add('John');
```

Result:

```text
John
John
```

Duplicates remain.

---

Set:

```apex
Set<String> names =
new Set<String>();

names.add('John');
names.add('John');
```

Result:

```text
John
```

Duplicate removed.

---

### 6. Set Syntax

General syntax:

```apex
Set<DataType> variableName =
new Set<DataType>();
```

Example:

```apex
Set<String> cities =
new Set<String>();
```

---

### 7. Breaking Down Syntax

```apex
Set<String> cities =
new Set<String>();
```

Meaning:

| Part | Meaning |
|----------|----------|
| Set | Collection type |
| String | Element type |
| cities | Variable name |
| new | Create object |
| Set<String>() | Empty Set |

---

### 8. Empty Set Creation

```apex
Set<String> cities =
new Set<String>();
```

Current state:

```text
{}
```

Empty Set.

---

### 9. Adding Values

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
{
 Delhi
}
```

---

### 10. Adding Multiple Values

```apex
cities.add('Delhi');

cities.add('Mumbai');

cities.add('Bangalore');
```

Result:

```text
{
 Delhi,
 Mumbai,
 Bangalore
}
```

---

### 11. Duplicate Handling

Example:

```apex
cities.add('Delhi');

cities.add('Delhi');

cities.add('Delhi');
```

Result:

```text
{
 Delhi
}
```

Only one copy stored.

---

### 12. Direct Initialization

```apex
Set<String> cities =
new Set<String>
{
    'Delhi',
    'Mumbai',
    'Bangalore'
};
```

Result:

```text
{
 Delhi,
 Mumbai,
 Bangalore
}
```

---

### 13. Duplicate During Initialization

```apex
Set<String> cities =
new Set<String>
{
    'Delhi',
    'Delhi',
    'Mumbai'
};
```

Result:

```text
{
 Delhi,
 Mumbai
}
```

Duplicate removed automatically.

---

### 14. Set Size

Method:

```apex
size()
```

Example:

```apex
cities.size();
```

Output:

```text
3
```

---

### 15. Duplicate Size Example

```apex
Set<String> cities =
new Set<String>();

cities.add('Delhi');

cities.add('Delhi');
```

Size:

```text
1
```

Not:

```text
2
```

---

### 16. Check Empty Set

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

if no elements exist.

---

### 17. Contains Method

Most important Set method.

Example:

```apex
cities.contains('Delhi');
```

Output:

```text
true
```

---

### 18. Contains Example

```apex
cities.contains('Pune');
```

Output:

```text
false
```

---

### 19. Why Contains Is Important?

Example:

```text
10000 Account IDs
```

Need to check:

```text
Does ID exist?
```

Set lookup is extremely fast.

---

### 20. Remove Element

Method:

```apex
remove()
```

Example:

```apex
cities.remove('Delhi');
```

Result:

```text
Delhi removed
```

---

### 21. Clear Entire Set

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
{}
```

Empty Set.

---

### 22. Iterating Through Set

Use for-each loop.

Example:

```apex
for(String city :
    cities)
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

### 23. No Index Access

List:

```apex
cities[0]
```

Valid.

---

Set:

```apex
cities[0]
```

Invalid.

Reason:

```text
Sets do not support indexing
```

---

### 24. Why No Index?

Because Set focuses on:

```text
Uniqueness
Fast Lookup
```

Not position-based access.

---

### 25. Set of Integers

```apex
Set<Integer> marks =
new Set<Integer>();
```

Example:

```apex
marks.add(90);

marks.add(80);

marks.add(90);
```

Result:

```text
90
80
```

Duplicate removed.

---

### 26. Set of Strings

```apex
Set<String> technologies =
new Set<String>();
```

Example:

```apex
technologies.add('Apex');

technologies.add('LWC');

technologies.add('Apex');
```

Result:

```text
Apex
LWC
```

---

### 27. Set of Decimal

```apex
Set<Decimal> prices =
new Set<Decimal>();
```

Example:

```apex
prices.add(100.50);

prices.add(100.50);
```

Result:

```text
100.50
```

---

### 28. Set of Boolean

```apex
Set<Boolean> values =
new Set<Boolean>();
```

Possible values:

```text
true
false
```

Only two unique values can exist.

---

### 29. Set of Date

```apex
Set<Date> holidays =
new Set<Date>();
```

Stores unique dates.

---

### 30. Set of Id

Very common.

```apex
Set<Id> accountIds =
new Set<Id>();
```

Used heavily in triggers.

---

### 31. Example

```apex
accountIds.add(
'001AAA'
);

accountIds.add(
'001AAA'
);
```

Result:

```text
Only one ID stored
```

---

### 32. Set of Accounts

Possible:

```apex
Set<Account> accounts =
new Set<Account>();
```

Stores unique Account objects.

---

### 33. Converting List To Set

Example:

```apex
List<String> cities =
new List<String>
{
    'Delhi',
    'Delhi',
    'Mumbai'
};
```

Convert:

```apex
Set<String> citySet =
new Set<String>(cities);
```

Result:

```text
Delhi
Mumbai
```

Duplicates removed.

---

### 34. Converting Set To List

Example:

```apex
List<String> cityList =
new List<String>(
citySet
);
```

Set becomes List.

---

### 35. Common Salesforce Usage

Sets are heavily used for:

```text
Record IDs
Emails
Usernames
Permissions
Bulk Processing
SOQL Optimization
Duplicate Elimination
```

---

### 36. Trigger Example

```apex
Set<Id> accountIds =
new Set<Id>();

for(Contact con :
    Trigger.new)
{
    accountIds.add(
        con.AccountId
    );
}
```

Result:

```text
Unique Account IDs
```

Collected automatically.

---

### 37. Why Trigger Developers Love Sets?

Without Set:

```text
Duplicate IDs
Extra Processing
Extra Queries
```

With Set:

```text
Unique IDs
Optimized Queries
Bulkified Logic
```

---

### 38. SOQL Query Optimization

Example:

```apex
Set<Id> accountIds =
new Set<Id>();
```

Query:

```apex
[
 SELECT Id,
        Name
 FROM Account
 WHERE Id IN :accountIds
]
```

Very common pattern.

---

### 39. Set Equality

Example:

```apex
Set<Integer> set1 =
new Set<Integer>
{
    1,2,3
};

Set<Integer> set2 =
new Set<Integer>
{
    1,2,3
};
```

Equivalent values.

---

### 40. Null Set Problem

Wrong:

```apex
Set<String> cities;

cities.add('Delhi');
```

Runtime error:

```text
Null Pointer Exception
```

---

Correct:

```apex
Set<String> cities =
new Set<String>();

cities.add('Delhi');
```

---

### 41. Common Beginner Mistake

Expecting duplicate storage.

```apex
cities.add('Delhi');

cities.add('Delhi');
```

Result:

```text
One Delhi
```

Not two.

---

### 42. Common Beginner Mistake

Trying index access.

```apex
cities[0]
```

Invalid.

Sets have no indexes.

---

### 43. Common Beginner Mistake

Expecting order.

Example:

```apex
Delhi
Mumbai
Bangalore
```

A Set should not be relied upon for a specific display order. If order matters, use a List.

---

## Set Operations

### 44. Union Operation

Combine all unique values.

Example:

```apex
Set<Integer> set1 =
new Set<Integer>{1,2,3};

Set<Integer> set2 =
new Set<Integer>{3,4,5};
```

```apex
set1.addAll(set2);
```

Result:

```text
1
2
3
4
5
```

---

### 45. Intersection Operation

Find common values.

```apex
Set<Integer> set1 =
new Set<Integer>{1,2,3};

Set<Integer> set2 =
new Set<Integer>{3,4,5};
```

```apex
set1.retainAll(set2);
```

Result:

```text
3
```

---

### 46. Difference Operation

Remove common values.

```apex
Set<Integer> set1 =
new Set<Integer>{1,2,3};

Set<Integer> set2 =
new Set<Integer>{3};
```

```apex
set1.removeAll(set2);
```

Result:

```text
1
2
```

---

## Practice Examples

### 47. Practice Example 1

Predict Output

```apex
Set<String> cities =
new Set<String>();

cities.add('Delhi');

cities.add('Mumbai');

System.debug(cities);
```

Answer:

```text
Delhi
Mumbai
```

---

### 48. Practice Example 2

Predict Output

```apex
Set<String> cities =
new Set<String>();

cities.add('Delhi');

cities.add('Delhi');

System.debug(cities);
```

Answer:

```text
Delhi
```

Only one value stored.

---

### 49. Practice Example 3

Predict Output

```apex
Set<Integer> nums =
new Set<Integer>();

nums.add(10);

nums.add(20);

nums.add(10);

System.debug(
nums.size()
);
```

Answer:

```text
2
```

Unique values:

```text
10
20
```

---

### 50. Practice Example 4

Predict Output

```apex
Set<String> cities =
new Set<String>
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

### 51. Practice Example 5

Predict Output

```apex
Set<String> cities =
new Set<String>
{
    'Delhi'
};

cities.remove('Delhi');

System.debug(
cities.isEmpty()
);
```

Answer:

```text
true
```

---

### 52. Practice Example 6

Will This Work?

```apex
Set<String> cities;

cities.add('Delhi');
```

Answer:

```text
No
```

Reason:

```text
Null Pointer Exception
```

---

### 53. Practice Example 7

Will This Work?

```apex
Set<String> cities =
new Set<String>();

cities.add('Delhi');
```

Answer:

```text
Yes
```

Valid.

---

### 54. Practice Example 8

Predict Output

```apex
Set<Integer> values =
new Set<Integer>
{
    1,
    2,
    2,
    3
};

System.debug(
values.size()
);
```

Answer:

```text
3
```

Unique values:

```text
1
2
3
```

---

### 55. Practice Example 9

Predict Output

```apex
List<String> cities =
new List<String>
{
    'Delhi',
    'Delhi',
    'Mumbai'
};

Set<String> citySet =
new Set<String>(
cities
);

System.debug(
citySet.size()
);
```

Answer:

```text
2
```

Duplicates removed.

---

### 56. Practice Example 10

Identify Collection Type

Requirement:

```text
Store unique Account IDs
```

Best choice?

Answer:

```apex
Set<Id>
```

---

### 57. Interview Questions

#### What Is a Set?

Answer:

```text
A collection that stores
unique values only.
```

---

#### Does Set Allow Duplicates?

Answer:

```text
No
```

Duplicates automatically removed.

---

#### Does Set Support Indexes?

Answer:

```text
No
```

No index-based access.

---

#### How To Check Existence?

```apex
set.contains(value);
```

---

#### How To Get Size?

```apex
set.size();
```

---

#### How To Remove Value?

```apex
set.remove(value);
```

---

#### Most Common Salesforce Usage?

```text
Set<Id>
```

Used in:

```text
Triggers
SOQL Queries
Bulk Processing
```

---

## 58. Final Summary

A Set in Apex is an unordered collection that stores only unique values. It automatically removes duplicates, provides fast existence checking through the `contains()` method, dynamically grows as values are added, and is widely used for efficient bulk processing. Sets do not support index-based access and should not be relied upon for a specific ordering of elements. Apex Sets can store primitive values, Salesforce IDs, sObjects, custom class instances, and other supported data types. In Salesforce development, `Set<Id>` is one of the most frequently used collections because it helps gather unique record IDs for optimized SOQL queries, trigger processing, integrations, and bulkified enterprise applications.
