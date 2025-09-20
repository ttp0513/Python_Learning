# 📘 Python - Strings Data Types

## String Basics
- Strings are sequence of character data commonly used to store text
- Create string by using quotation marks, or converting from numbers
- Quotation Marks:
 - **Double quotes "** allow using single quote inside the string
 - **Triple quotes '''** allow writing multiple strings, without worrying about "errors" due to using single or double quotes

## String Arithmetic
| Operation        | Example                      | Result / Behavior                        | Notes                                           |
|------------------|------------------------------|------------------------------------------|-------------------------------------------------|
| Concatenation    | `"Hello" + "World"`          | `"HelloWorld"`                           | Combines two strings                           |
| Repetition       | `"Hi" * 3`                   | `"HiHiHi"`                                | Repeats the string 3 times                     |
| Invalid Subtract | `"Hello" - "World"`          | ❌ `TypeError`                            | Strings can't be subtracted                    |
| Invalid Divide   | `"Hello" / 2`                | ❌ `TypeError`                            | Strings can't be divided                       |
| Invalid Modulo   | `"Hello" % 2`                | ❌ `TypeError`                            | Unless used for formatting (see below)         |
| Format (modulo)  | `"Name: %s" % "Alice"`       | `"Name: Alice"`                           | Old-style string formatting                    |
| Format (f-string)| `f"Score: {95}"`             | `"Score: 95"`                             | Modern string interpolation                    |
| Join             | `" ".join(["a", "b", "c"])`  | `"a b c"`                                 | Joins list of strings with a separator         |
| Length           | `len("Python")`              | `6`                                       | Returns number of characters                   |

## String Indexing
- Strings, along with sequence data types, can be navigated via their **index**
- Python is 0-indexed, which means that the first item in a sequence has an index of 0, not 1
- Access individual characters in a string by using **bracket[index]**
 - **Positive indices**: Begin at the beginning of the object, starting with 0 and work forwards
 - **Negative indices**: Begin at the end of the object and work backwards. There is no negative 0, so it starts at `-1`
- Indexing a value greater than the length of the string or object results in an `IndexError`
```py
message = 'I love Python!'
message[0] # 'I'
message[-1] # '!'
message[25] # IndexError: string index out of range
```

## String Slicing
Slicing returns multiple elements in a string, or sequence, via indexing

`[start:stop:step size]`
- `start`: index value to start with (**default is 0**)
- `stop`: index value to stop at, not inclusive (**default is all the values after the start**)
- `step size`: amount to increment each subsequent index (**default is 1**). Can reverse the string with -1

```py
message = 'I love Python and JS'
message[0:6:1] = message[:6] # 'I love'
message[6:] # " Python and JS"
message[::-1] # 'SJ dna nohtyP evol I'
```
## String Methods
- Methods are functions that only apply to a specific data type or object
- Calling a method by following the object with a period (.) then the method name
- If applying a string method to an integer, it'll result in an `AttributeError`


| Method              | Description                                                  | Example Usage                                 | Output                          |
|---------------------|--------------------------------------------------------------|------------------------------------------------|----------------------------------|
| `str.upper()`       | Converts all characters to uppercase                         | `'hello'.upper()`                             | `'HELLO'`                        |
| `str.lower()`       | Converts all characters to lowercase                         | `'HELLO'.lower()`                             | `'hello'`                        |
| `str.title()`       | Capitalizes first letter of each word                        | `'hello world'.title()`                       | `'Hello World'`                  |
| `str.capitalize()`  | Capitalizes first character only                             | `'python'.capitalize()`                       | `'Python'`                       |
| `str.strip()`       | Removes leading/trailing whitespace                          | `'  hello  '.strip()`                         | `'hello'`                        |
| `str.lstrip()`      | Removes leading whitespace                                   | `'  hello'.lstrip()`                          | `'hello'`                        |
| `str.rstrip()`      | Removes trailing whitespace                                  | `'hello  '.rstrip()`                          | `'hello'`                        |
| `str.replace(a, b)` | Replaces substring `a` with `b`                              | `'hello world'.replace('world', 'Python')`    | `'hello Python'`                |
| `str.split(sep)`    | Splits string into list by separator `sep`                  | `'a,b,c'.split(',')`                          | `['a', 'b', 'c']`                |
| `delimiter.join(list)`    | Joins list into string with separator                        | `'-'.join(['a', 'b', 'c'])`                   | `'a-b-c'`                        |
| `str.find(sub)`     | Returns index of first occurrence of `sub`                  | `'hello'.find('e')`                           | `1`                              |
| `str.index(sub)`    | Like `find()`, but raises error if not found                | `'hello'.index('e')`                          | `1`                              |
| `str.count(sub)`    | Counts occurrences of `sub`                                  | `'banana'.count('a')`                         | `3`                              |
| `str.startswith(x)` | Checks if string starts with `x`                             | `'hello'.startswith('he')`                    | `True`                           |
| `str.endswith(x)`   | Checks if string ends with `x`                               | `'hello'.endswith('lo')`                      | `True`                           |
| `str.isalpha()`     | Checks if all characters are alphabetic                      | `'abc'.isalpha()`                             | `True`                           |
| `str.isdigit()`     | Checks if all characters are digits                          | `'123'.isdigit()`                             | `True`                           |
| `str.isalnum()`     | Checks if all characters are alphanumeric                    | `'abc123'.isalnum()`                          | `True`                           |
| `str.isspace()`     | Checks if all characters are whitespace                      | `'   '.isspace()`                             | `True`                           |
| `str.swapcase()`    | Swaps case of each character                                 | `'Hello'.swapcase()`                          | `'hELLO'`                        |
| `str.zfill(width)`  | Pads string on the left with zeros to reach `width`         | `'42'.zfill(5)`                               | `'00042'`                        |
| `str.center(w)`     | Centers string in a field of width `w`                      | `'hi'.center(6)`                              | `'  hi  '`                       |
| `str.ljust(w)`      | Left-aligns string in field of width `w`                    | `'hi'.ljust(6)`                               | `'hi    '`                       |
| `str.rjust(w)`      | Right-aligns string in field of width `w`                   | `'hi'.rjust(6)`                               | `'    hi'`                       |
| `str.partition(x)`  | Splits string into 3 parts: before, separator, after        | `'key=value'.partition('=')`                  | `('key', '=', 'value')`         |
| `str.rpartition(x)` | Like `partition()`, but splits at last occurrence of `x`    | `'a=b=c'.rpartition('=')`                     | `('a=b', '=', 'c')`             |
| `str.rsplit(sep)`   | Splits from the right by separator                          | `'a,b,c'.rsplit(',', 1)`                      | `['a,b', 'c']`                   |
| `str.casefold()`    | Aggressive lowercase (for caseless comparison)              | `'Straße'.casefold()`                         | `'strasse'`                      |


## Chaining Methods
Methods can be chained together to create powerful expressions

```py
message = 'I hope I can get a developer job SOON'
message[6::].lower().split()
# Output: ['i', 'can', 'get', 'a', 'developer', 'job', 'soon']
```

## F-Strings
- Including variables in strings by using `f-strings`
- This allows changing the output text based on changing variable values
- Use: Add an `f` before the quotation marks to indicate an `f-string` and place the variable names into the string by using curly braces `{}`

```py
name = 'john'
role = 'employee'
print(f'{name.title()} is our favorite {role}!')
# John is our favorite employee!
```

