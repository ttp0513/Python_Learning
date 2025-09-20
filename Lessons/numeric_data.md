# 📘 Python - Numeric Data Types

## Numeric Data Types
### Integers(`int`)
- Whole numbers without decimal points
```py
integerNumber = 3
```

### Float(`float`)
- Real numbers with decimal points
```py
floatNumber = 3.14
```
### Complex(`complex`)
- Numbers with real and imaginary portions
```py
complexEx = 3.5 + 2j
```

## Numeric Type Conversion
Use `\<data type>(object)` to convert any number into a numeric data type, as long as they contain numeric characters

```py
# Convert float to int
number = 2.9
number = int(number)
number # 2, int rounds down

# Convert int to float
value = 1
value = float(value)
value # 1.0

# Convert strings with numeric only to floats/integers
string = '1.2'
string = float(string)
string # 1.2

# Cant convert anything that isn't numeric only
mix_string = 'abc123'
mix_string = float(mix_string)
mix_string # ValueError
```

## Arithmetic Operators 
| Operator | Description               | Example             |
|----------|---------------------------|---------------------|
| `+`      | Addition                  | `5 + 3 = 8`         |
| `-`      | Subtraction               | `10 - 4 = 6`        |
| `*`      | Multiplication            | `7 * 2 = 14`        |
| `/`      | Division (float result)   | `8 / 2 = 4.0`       |
| `//`     | Floor Division, divides on value by another, then rounds down to the nearest integer            | `9 // 2 = 4`        |
| `%`      | Modulus (remainder of a division)       | `10 % 3 = 1`        |
| `**`     | Exponentiation            | `2 ** 3 = 8`        |

## Order of Operations
Python uses the standard **PEMDAS** order of operations to perform calculations
1. **P**arentheses ()
2. **E**xponentiation **
3. **M**ultiplication (*) & **D**ivision (/) (including Floor Division(//) & Modulo(%)) from left to right
4. **A**ddition (+) & **S**ubtraction (-), from left to right

## Numeric Functions
### Single-Value Functions
| Function & Arguments       | Description                            | Example                          |
|----------------------------|----------------------------------------|----------------------------------|
| `abs(x)`                  | Returns the absolute value of `x` (int or float) | `abs(-5) → 5`                    |
| `round(x, ndigits)`       | Rounds `x` to `ndigits` decimal places (optional) | `round(3.1415, 2) → 3.14`        |
| `pow(x, y)`               | Raises `x` to the power of `y`         | `pow(2, 3) → 8`                  |
| `math.sqrt(x)`            | Returns square root of `x` (must be ≥ 0) | `math.sqrt(16) → 4.0`            |
| `math.ceil(x)`            | Rounds `x` up to nearest integer       | `math.ceil(2.3) → 3`             |
| `math.floor(x)`           | Rounds `x` down to nearest integer     | `math.floor(2.9) → 2`            |


### Multiple-Value Functions
| Function & Arguments               | Description                                      | Example                                      |
|-----------------------------------|--------------------------------------------------|----------------------------------------------|
| `map(abs, iterable)`              | Applies `abs()` to each item in `iterable`       | `list(map(abs, [-5, -3, 2])) → [5, 3, 2]`     |
| `np.round(array, decimals)`       | Rounds each element in `array` to `decimals` places | `np.round([3.1415, 2.718], 1) → [3.1, 2.7]`   |
| `np.power(array, exponent)`       | Raises each element in `array` to `exponent`     | `np.power([2, 3], 2) → [4, 9]`                |
| `min(iterable)` / `max(iterable)`| Finds min/max value in `iterable` (list, tuple, etc.) | `min([4, 7, 1]) → 1`, `max([4, 7, 1]) → 7`    |
| `sum(iterable)`                   | Adds all values in `iterable`                    | `sum([1, 2, 3]) → 6`                          |
| `np.sqrt(array)`                  | Returns square root of each element in `array`   | `np.sqrt([4, 9]) → [2., 3.]`                  |
| `np.ceil(array)`                  | Rounds each element in `array` up                | `np.ceil([2.3, 3.1]) → [3., 4.]`              |
| `np.floor(array)`                 | Rounds each element in `array` down              | `np.floor([2.9, 3.7]) → [2., 3.]`             |
| `statistics.mean(data)`           | Returns mean of numeric `data` (list or tuple)   | `statistics.mean([1, 2, 3]) → 2`              |
