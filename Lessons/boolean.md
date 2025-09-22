# 📘 Python - Conditional Logic - Boolean Data Type

## The Boolean Type
Boolean has two possible values: `True` & `False`
- `True` is 1 in arithmetic operations
- `False` is 0 in arithmetic operations

```py
True * 1 == 1 == not False
False * 1 == 0 == not True
```

##  Comparison Operators

| Operator | Description           | Example (True) | Example (False) |
|----------|-----------------------|----------------|-----------------|
| `==`     | Equal                 | `5 == 5`       | `5 == 3`        |
| `!=`     | Not Equal             | `5 != 3`       | `5 != 5`        |
| `<`      | Less Than             | `5 < 6`        | `21 < 12`       |
| `>`      | Greater Than          | `10 > 2`       | `2 > 10`        |
| `<=`     | Less Than or Equal    | `4 <= 4`       | `6 <= 3`        |
| `>=`     | Greater Than or Equal | `7 >= 7`       | `3 >= 9`        |


## Membership Tests
Membership tests check if a value exists inside an iterable data type
- The keywords `in` and `not in` are used to conduct membership tests

```py 
message = 'I hope it snows tonight!'
'snow' in message # True
'snow' not in message # False
```

## Boolean operators
Boolean operators allow user to combine multiple comparison operators
- The `and` operator requires all statements to be true
- The `or` operator requires one statement to be true
- Parentheses `()` controls the order of evaluation

**Note**
- If the first expression chained by `and` is False,  by `or` is True, the rest of the clauses will not be evaluated
- Place simple clauses first to eliminate the need to run complex clauses, making program more efficient

```py
price = 105
item = 'skis'
(price <= 100 and item == 'ski poles') or (item == 'skis')
# True because item == 'skis', the `or` operators returns True
```
## Control Flow
- Control Flow is a programming concept that allows you to choose which lines to execute, rather than simply running all the lines from top to bottom
- There are 3 conditional statements that help achieve this: `if`, `else`, and `elif`
- Python uses `indentation` to depart from a linear flow

## The IF/ELSE/ELIF Statements
- The `if statement` runs lines of indented code when a given logical condition is met
- The `elif statements` specifies additional criteria to evaluate when the logical condition in an `if statement` is not met 
- The `else statement` runs lines of indented code when none of the logical conditions in the `if` or `elif` statements are met

**Note**:
-  Press tab, or use four spaces, to indent code when writing if statements, or `IndentationError` occurs
- As more logical statements are added, it's important to be careful with their order. Either put the most restrictive condition firsts, or be more explicit with logic

```py
if condition: 
    do this 
elif condition_2: 
else:
    code = 3
```

## Nested Logic
- Nested logical statements specifies additional criteria to evaluate after a logical condition in a conditional statement is met

```py
price = 499.99
budget = 500.00
inventory = 0

if budget > price: # if statement
    if inventory > 0 # nested if statement
        print('Can afford')
    else: 
        print('Can afford, but it is not available')
else: 
    print("Can't afford")
# Output: 'Can afford, but it is not available'
```
