## Enums in Apex — Complete Step-by-Step Guide

### 1. What Is an Enum?

Enum stands for:

```text
Enumeration
```

An enum is a special data type that represents a **fixed set of predefined constant values**.

Example:

```apex
public enum Status {
    New,
    InProgress,
    Completed
}
```

This enum can only have one of these values:

```text
New
InProgress
Completed
```

Nothing else.

---

### 2. Why Were Enums Created?

Imagine you are storing order status as a String.

```apex
String status = 'Completed';
```

Looks fine.

But later someone writes:

```apex
String status = 'completed';
```

or

```apex
String status = 'COMPLETED';
```

or

```apex
String status = 'Compelted';
```

Notice:

```text
Typo
Wrong capitalization
Invalid value
```

All are possible.

This can introduce bugs.

Enums solve this problem.

---

### 3. Real-World Analogy

Think of a traffic signal.

Allowed values:

```text
Red
Yellow
Green
```

Not allowed:

```text
Blue
Purple
Black
```

Traffic signals have a fixed set of values.

Enums work exactly the same way.

---

### 4. Without Enum Example

Using String:

```apex
String status = 'Completed';
```

Possible values:

```text
Completed
completed
COMPLETED
Done
Finished
Compelted
Anything
```

No control.

---

### 5. With Enum Example

```apex
public enum Status {
    New,
    InProgress,
    Completed
}
```

Usage:

```apex
Status currentStatus =
Status.Completed;
```

Allowed values:

```text
New
InProgress
Completed
```

Only these.

---

### 6. Basic Enum Syntax

General syntax:

```apex
public enum EnumName {

    VALUE1,

    VALUE2,

    VALUE3

}
```

Example:

```apex
public enum Priority {

    Low,

    Medium,

    High

}
```

---

### 7. Understanding Enum Components

Example:

```apex
public enum Priority {

    Low,

    Medium,

    High

}
```

Parts:

| Part | Meaning |
|----------|----------|
| enum | Keyword |
| Priority | Enum name |
| Low | Enum constant |
| Medium | Enum constant |
| High | Enum constant |

---

### 8. Creating Enum Variable

Example:

```apex
Priority priority;
```

Variable type:

```text
Priority
```

Possible values:

```text
Low
Medium
High
```

---

### 9. Assigning Enum Value

```apex
Priority priority =
Priority.High;
```

Result:

```text
priority → High
```

---

### 10. Accessing Enum Value

```apex
System.debug(
Priority.High
);
```

Output:

```text
High
```

---

### 11. Multiple Enum Examples

Order Status:

```apex
public enum OrderStatus {

    Created,

    Processing,

    Shipped,

    Delivered,

    Cancelled

}
```

---

User Role:

```apex
public enum UserRole {

    Admin,

    Manager,

    Employee

}
```

---

Ticket Priority:

```apex
public enum TicketPriority {

    Low,

    Medium,

    High,

    Critical

}
```

---

Payment Status:

```apex
public enum PaymentStatus {

    Pending,

    Success,

    Failed

}
```

---

### 12. Using Enum In If Statements

Example:

```apex
Priority priority =
Priority.High;

if(priority == Priority.High)
{
    System.debug(
        'Urgent Ticket'
    );
}
```

Output:

```text
Urgent Ticket
```

---

### 13. Comparing Enum Values

Example:

```apex
Priority priority =
Priority.Medium;
```

Check:

```apex
priority == Priority.Medium
```

Result:

```text
true
```

---

Example:

```apex
priority == Priority.High
```

Result:

```text
false
```

---

### 14. Enum In Switch Statements

Enums work beautifully with switch.

Example:

```apex
Priority priority =
Priority.High;

switch on priority {

    when Low {
        System.debug('Low');
    }

    when Medium {
        System.debug('Medium');
    }

    when High {
        System.debug('High');
    }

}
```

Output:

```text
High
```

---

### 15. Why Enum + Switch Is Powerful?

Without enum:

```apex
String status =
'Completed';
```

Need string comparisons.

Risk:

```text
Typo
Invalid value
```

With enum:

```apex
Status.Completed
```

Safe and predictable.

---

### 16. Getting Enum Name

Example:

```apex
Priority priority =
Priority.High;
```

Get text:

```apex
String value =
String.valueOf(priority);
```

Output:

```text
High
```

---

### 17. Convert String To Enum

Example:

```apex
Priority priority =
Priority.valueOf('High');
```

Result:

```text
Priority.High
```

---

### 18. Invalid Conversion

Example:

```apex
Priority priority =
Priority.valueOf('Critical');
```

Error:

```text
Invalid enum value
```

Reason:

```text
Critical not defined
```

---

### 19. Enum values() Method

Returns all enum values.

Example:

```apex
Priority.values();
```

Result:

```text
[
 Low,
 Medium,
 High
]
```

---

### 20. Loop Through Enum Values

```apex
for(Priority p :
    Priority.values())
{
    System.debug(p);
}
```

Output:

```text
Low

Medium

High
```

---

### 21. Real World Salesforce Example — Case Priority

```apex
public enum CasePriority {

    Low,

    Medium,

    High,

    Critical

}
```

Usage:

```apex
CasePriority priority =
CasePriority.Critical;
```

Decision:

```apex
if(priority ==
   CasePriority.Critical)
{
    sendImmediateAlert();
}
```

---

### 22. Real World Example — Lead Status

```apex
public enum LeadStatus {

    New,

    Contacted,

    Qualified,

    Converted,

    Closed

}
```

Usage:

```apex
LeadStatus status =
LeadStatus.Qualified;
```

---

### 23. Real World Example — Approval Status

```apex
public enum ApprovalStatus {

    Pending,

    Approved,

    Rejected
}
```

---

Usage:

```apex
ApprovalStatus status =
ApprovalStatus.Pending;
```

---

### 24. Real World Example — User Permissions

```apex
public enum AccessLevel {

    Read,

    Write,

    Delete,

    Admin
}
```

---

Check:

```apex
if(level ==
   AccessLevel.Admin)
{
    System.debug(
        'Full Access'
    );
}
```

---

### 25. Enum Inside Class

Example:

```apex
public class OrderService {

    public enum OrderStatus {

        Created,

        Processing,

        Delivered

    }

}
```

Usage:

```apex
OrderService.OrderStatus
```

---

### 26. Public Enum

```apex
public enum Status {

    Active,

    Inactive
}
```

Accessible throughout org.

---

### 27. Private Enum

```apex
private enum Status {

    Active,

    Inactive
}
```

Only inside class.

---

### 28. Enum Best Practices

Use singular names.

Good:

```apex
Priority
Status
Role
AccessLevel
```

Avoid:

```apex
Priorities
Statuses
Roles
```

---

### 29. Enum Naming Convention

Enum Name:

```apex
PascalCase
```

Example:

```apex
OrderStatus
```

---

Values:

```apex
PascalCase
```

Example:

```apex
PendingApproval
```

---

### 30. Advantages Of Enums

#### Type Safety

Only valid values allowed.

---

#### Prevent Typo Bugs

Wrong spelling impossible.

---

#### Better Readability

Example:

```apex
Status.Completed
```

Very clear.

---

#### Better IDE Support

Auto-completion available.

---

#### Easier Maintenance

Centralized values.

---

### 31. Disadvantages Of String-Based Status

Example:

```apex
String status =
'Completed';
```

Problems:

```text
Typos
Case sensitivity
Invalid values
No compile-time validation
```

---

Enums eliminate all these problems.

---

### 32. Practice Example 1

Predict Output

```apex
public enum Priority {

    Low,

    Medium,

    High

}
```

```apex
Priority p =
Priority.High;

System.debug(p);
```

Answer:

```text
High
```

---

### 33. Practice Example 2

Predict Output

```apex
Priority p =
Priority.Low;

System.debug(
p == Priority.Low
);
```

Answer:

```text
true
```

---

### 34. Practice Example 3

Predict Output

```apex
Priority p =
Priority.High;

System.debug(
p == Priority.Low
);
```

Answer:

```text
false
```

---

### 35. Practice Example 4

Predict Output

```apex
String value =
String.valueOf(
Priority.High
);

System.debug(value);
```

Answer:

```text
High
```

---

### 36. Practice Example 5

Predict Output

```apex
Priority p =
Priority.valueOf('Medium');

System.debug(p);
```

Answer:

```text
Medium
```

---

### 37. Practice Example 6

Will This Work?

```apex
Priority p =
Priority.valueOf('Critical');
```

Answer:

```text
No
```

Reason:

```text
Critical does not exist
```

---

### 38. Practice Example 7

Predict Output

```apex
for(Priority p :
    Priority.values())
{
    System.debug(p);
}
```

Answer:

```text
Low

Medium

High
```

---

### 39. Practice Example 8

Identify Enum Value

```apex
public enum Role {

    Admin,

    Manager,

    User

}
```

Valid:

```apex
Role.Admin
```

Answer:

```text
Valid
```

---

### 40. Practice Example 9

Identify Enum Value

```apex
Role.SuperAdmin
```

Answer:

```text
Invalid
```

Not defined.

---

### 41. Practice Example 10

Predict Output

```apex
Priority p =
Priority.Medium;

if(p ==
   Priority.Medium)
{
    System.debug(
        'Matched'
    );
}
```

Answer:

```text
Matched
```

---

### 42. Interview Questions

#### What Is Enum?

Answer:

```text
A user-defined data type that
contains a fixed set of constants.
```

---

#### Why Use Enum Instead Of String?

Answer:

```text
Type safety
Prevent typos
Better readability
Compile-time validation
```

---

#### How To Convert String To Enum?

```apex
Priority.valueOf('High');
```

---

#### How To Get All Enum Values?

```apex
Priority.values();
```

---

#### How To Convert Enum To String?

```apex
String.valueOf(priority);
```

---

## 43. Final Summary

Enums in Apex are special user-defined data types used to represent a fixed set of predefined constants. They provide type safety, improve readability, prevent invalid values and typo-related bugs, and make code easier to maintain. Enums are commonly used for statuses, priorities, roles, approval states, permissions, workflow stages, and other business concepts that have a limited number of valid values. Apex provides useful enum capabilities such as comparison, iteration using `values()`, conversion from String using `valueOf()`, conversion to String using `String.valueOf()`, and seamless integration with `if` statements and `switch` expressions.
