# 📘 Python - Data Types

## Single Value Data Type
### Numeric
Represent numeric values
- `Integer(int)`: 5
- `Float(float)`: 5.24
- `Complex(complex)`: 5 + 2j

### Text
Represent sequences of characters, usually text
Usually in between quotation ', or "
- `String`: 'snowboard' / "snowboard"

### Boolean
Represents True and False values
- `Boolean(bool)`: True, False

### None
Represent the absence of a value
- `NoneType`: None

## Multiple Values Data Type
### Sequence
Represents sequences of values, usually text or numeric
- `List(list)`: [1, 3, 4, 6]
- `Tuple(tuple)`: ('snowboard', 'skis')
- `Range(range)`: range(1, 20)

### Mapping
Maps keys to values for efficient information retrieval
- `Dictionary(dict)`: {'snowboard': 25, 'skies': 15}

### Set
Represents a collection of unique, non-duplicate values
- `Set(set)`: {'snowboard', 'skies'}
- `Frozen Set(fronzenset)`

## Type() Function
- The `type()` function returns the data type of the object passed to it

```py
type(1) # int
type('snowboard') # str
type(True) # bool
type(None) # NoneType
type([1, 3, 5]) # list
type({'a': 3, 'b': 5}) # dict
```

## Type Conversion
- Convert data types by using "\<data type>(object)"

```py
int('123') # Convert the text string of '123' into an integer data type
int([1, 2, 3]) # Result in TypeError: int() argument must be a single-like data type, not multiple-values data type
```

## Iterables
Iterables are data types that can be iterated, or looped through, allowing you to move from one value to the next

### Iterable data types
- `Sequence`
- `Mapping`
- `Set`
- `Text` - While text strings are treated as a single value, individual characters in a text string can be iterated through

### Mutability
### Mutable Data Types
- Flexible, can add, remove, change values in the object
- `List`
- `Dictionary`
- `Set`

### Immutable Data Types
- To modify a value must delete and create the entire object
- `String`
- `Float`
- `Integers`
- `Boolean`
- `Tuples`
- `Fronzenset`

