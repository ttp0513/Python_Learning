# 📘 Python - Variables

## Variable Assignment
- Variables are containers used to label and store values for future reference
- Variable can store any Python data type, including function, dictionary
- Only assign variables for values that can change or will be used repeatedly; if not sure, it's recommended to assign a variable

```py
variable_name = value
# variable_name: intuitive label assigned to the variable
# value: initial value assigned to the variable
```
Example
```py
price = 5
discount = 1.5
discount_price = price - discount # output = 3.5
```

## Overwriting Variables
- Overwrite by assigning a new value to it
    - Variables can be assigned as values to other variables
- Overwrite can happen multiple times
- When overwrite a variable, its previous value will be lost and cannot be retrieved

**Tip**
Create a new variable when testing programs with different values to make sure no important data will be lost - once the code works as needed, remove any extra variables to enhance readability and prevent confusion and memory issues

```py
price = 5 # Python stores the value of 5 in memory when assigned to price
price = 6 # Then price stores the value 6 and 5 gets removed from memory
new_price = 7 # Assign 7 to new price
price = new_price # Assign the value of new_price which is 7 to price and 6 get removed from memory
new_price = 8 # Assign 8 to new price
print(price) # price is still 7 as it's not tied to the value of new_price!
```

## Deleting Variables - `del`
- `del` keyword will permanently remove variables and other objects

```py
price = 6
del price
print(price) # NameError occurs when referencing a variable that isn't defined
```
**Note**
Deleting objects is generally unnecessary; in most cases, reassign the variables instead and Python will remove the old value

