# Basic Data Types

Let's discuss data types, variables, and naming.

### Variables

A data type is a unit of information that can be stored and retrieved using a program language. We store data into, and retrieve data from, **variables**.

### Creating a Variable

```python

first_prime = 2

```

### Reading a Variable

```python

print(first_prime) # expect to see 2

```

### Naming Variables

In python, the best practice is to **snake_case** variables, where we delimit spaces within variable names with the `_` character.

```python
this_is_snake_cased = 1
```

## Integers

```python

example_int = 1
example_int_type = type(1) # <class 'int'>

```

## Floats

Floats are defined as decimals

```python

example_float = 1.001
example_float_type = type(1.001) # <class 'float'>

```

## Int/Float Operators

We can operate on integers/floats in the following ways

```python
example_int = 1

another_int = example_int + 5 # addition
another_int = example_int * 5 # multiplication
another_int = example_int - 5 # subtraction
another_int = example_int / 5 # division
another_int = example_int % 5 # modulus operator
```

## Strings

Sequences of characters are called "strings"

```python

my_name = 'Taq Karim'
your_name = "John Smith" # single or double quotes are valid

string_type = type("testing") # <class 'str'>

```

## String operators

We can "add" strings

```python
print("this string" + "that string") # what does this output?
```

We cannot add strings to non strings

```python
print("this will not work" + 4) # 4 is not stype str
```

As a convenience, we can format strings like so:

```python
a = 1
b = 2

formatted_string = f"{a} is {b}" # notice how a, b are formatted into string even tho they are ints

print(formatted_string) # "1 is 2"
```


## Booleans

Booleans represent true/false

```python

is_it_winter = True
is_it_warm_out = False

boolean_type = type(True) # <class 'bool'>

```

We use booleans primarily in conditional statements

## Nonetype

`None` represents variables that have not yet been defined.

```
print(type(None)) # <class 'NoneType'>
```

## Typecasting

Sometimes, we need to convert one datatype to another. Typecasting allows us to convert between types

```python

# convert string to int
int('10') # 10 - but as type int
int('tasdfa') # throws a ValueError

```

```python

# convert int to str
str(10) # '10' - but as type str

```

```python

# convert int to bool
bool(10) # True
bool(0) # False
```

To check the type of a data type:

```python

# check types
isinstance(-1, bool) # False
isinstance(False, bool) # True

# ..etc

```

## 🚗 Practice: Shopping List Calculator I

Create five variables, set them to strings that represent 5 common shopping list items

```python
item_name_1
item_name_2
item_name_3
item_name_4
item_name_5
```

Create five more variables, set them to floats that represent the prices of each of the items above

```python
item_price_1
item_price_2
item_price_3
item_price_4
item_price_5
```

Create five more variables, set them to ints that represent the **quantity** of each of the items above

```python
item_quant_1
item_quant_2
item_quant_3
item_quant_4
item_quant_5
```


Print to the console the name and price of each item defined above as follows:

```
1 Coco Puffs = $8.95.
```

where:
* `1` would be `item_quant_1`
* `Coco Puffs` would be `item_name_1`
* `8.95` would be `item_name_2`

## 🚗 Practice: Shopping List Calculator II

Given the code above, now implement the "calculator" part

Write a program that will output not only the:

```
1 Coco Puffs = $8.95.
```

from above, but will also calculate the total price *and* price with tax. Sample output:

```
1 Coco Puffs = $8.95.
2 Pop tarts = $5.00. # this means price of pop tarts is 2.50
1 Eggs = $3.25.
1 Steak = $12.00
1 Milk = $2.25.

TOTAL: $31.45 # this is calculated by adding the above
TAX: $2.594625. # this is calculated by 8.25% of TOTAL

TOTAL: $34.04 # use round() to solve this
```

## 🚗 Practice: Shopping List Calculator III

Update the code above to solicit **user** input for name, price, quantity. The `input()` command will help us solve this:

```
item_name_1 = input('Name your first item') # this will ask user to input value of item_name_1
```

