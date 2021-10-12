# Logical Operators

Logical operators are used to combine tests. Instead of embedded or multiple statements, one if statement could handle it all.

For most languages except Python:

|                                     | Operator | Example(s)                          |
| ----------------------------------- | -------- | ----------------------------------- |
| and (all tests are true)            | &&       | if (x > 1 && x < 5) { ... }         |
| or (at least one test is true)      | \|\|     | if (num == 3 \|\| num == 6) { ... } |
| not (runs if the variable is false) | !        | if (!lightOn) { ... }               |

Python:

{% hint style="warning" %}
These examples have not been tested
{% endhint %}

|                                     | Operator | Example(s)                   |
| ----------------------------------- | -------- | ---------------------------- |
| and (all tests are true)            | and      | if x > 1 and x < 5: ...      |
| or (at least one test is true)      | or       | if num == 3 or num == 6: ... |
| not (runs if the variable is false) | not      | if not lightOn: ...          |

