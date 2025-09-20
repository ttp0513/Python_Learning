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

## Naming Variables Rules
Give variables intuitive names to make understanding code easier, e.g instead of PL19, consider price_list_2019
### CAN
- Contain letters (case sensitive)
- Contain numbers
- Contain underscores
- Begin with a letter or underscore

### CAN'T
- Begin with a number
- Contain spaces or other special character (*, &, ^, - , etc)
- Be reserved Python keywords like `del` or `list`
```py
# Variables valid name
price_list_2019
_price_list_2019
PRICE_LIST_2019
pl2019

# Variables invalid name
2019_price_list # start with a number
price-list-2019 # has special character '-'
2018 price list # has spaces
list # reserved Python keyword
```

## Tracking Variables

### `%who`
This returns variable names 

### `%whos`
This returns variables name **type**, and information on the data contained

**Note**
Magic commands that start with `%` only work in **IPython or Jupyter notebooks/Colab**
```py
x = 42
y = "hello"
z = [1, 2, 3
%who
# x  y  z - variable names
%whos
# Variable   Type        Data/Info
# x          int         42
# y          str         hello
# z          list        3 elements
```
