# Lists and Dicts

Lists and dicts help us store compound data.

## Lists

A list, as it sounds like, is used to store multiple bits of data in the same variable

```python
test_scores = [100, 68, 95, 84, 79, 99]
```

Here, we store multiple test scores within a single list. We can access individual scores by **index**:

```python
print(test_scores[0]) # 100
print(test_scores[3]) # 84
```

We use the `len` function to get the total length of items in that list

```python

print(len(test_scores)) # 6

```

We can update a list by

```python
list_ = []

list_.append(1) # [1]
list_.append(2) # [1,2]
```

Here's some **[useful list methods](https://docs.python.org/3/tutorial/datastructures.html)** in python.

## Tuples

Tuples are a special subset of lists - they can only have two values and they are *immutable* - in that they cannot be changed after creation.

We write tuples as:

```python
score_1 = ('Taq', 100)

# OR

score_2 = 'Sue', 101
```

Tuples are denoted with the `()`.

We read tuples just like we would read a list:

```python
print(score_1[0]) # 'Taq'
```

## Sets

Sets are special lists in that they can only have **unique** elements

```python
set_1 = {1,2,3,4,5} # this is a set, notice the {}
set_2 = {1,1,1,2,2,3,4,5,5,5} # this is still a set
print(set_2) # {1,2,3,4,5}

print(set_1 == set_2) # True
```

Sets are not indexed, so you cannot access say the 3rd element in a set. Instead, you can:

```python
print(2 in set_1) # True
print(9 in set_1) # False
```

Here's a **[helpful list](https://snakify.org/en/lessons/sets/#section_4)** of set operations.

## Dicts

Dicts, or dictionaries, are key value pairs that act as another method for storing complex data.

```python
students = {
  'taq': [86, 45, 98, 100],
  'sue': [100, 100, 100, 100],
  'jon': [38, 49, 90, 87],
}
```

In the example above, we associate a "key" - 'taq', 'sue', etc -  to values, in this case arrays representing test scores. Values can be any valid python datatype, keys must be strings.

We can access each item in the list by:

```python
print(students['taq']) # [86, 45, 98, 100]
```

Attempting to find a key that does not exist leads to error:

```python

print(students['foo']) # KeyError
```

Instead, better to:

```python

print(students.get('foo', [])) # []

```

We can update a dictionary as follows:

```python
students['new_student'] = [99, 98, 99, 100]
```

Now, dict has 4 keys. We can also retrieve keys, values or items of dict as follows:

```python

student.keys() # ['taq', 'sue', 'jon', 'new_student']
student.values() # [[86, 45, 98, 100], [100, 100, 100, 100], etc ]
student.items() # [('taq', [86, 45, 98, 100]), ('sue', [100, 100, 100, 100]), etc]

```

## Iterating Lists / Dicts

In programming, we define iteration to be the act of running the same block of code over and over again a certain number of times. In simplest terms, this can be defined as:

```python
for i in range(11, 15):
    print(i, i ** 2)
    
# the above will print:
# 11 121
# 12 144
# 13 169
# 14 196
# 15 225
```

However, we can iterate over lists and dicts! Neato!

List iteration ex:

```python
test_scores = [100, 68, 95, 84, 79, 99]
for score in test_scores:
  if score > 85:
    print(score, "passed!")
  else:
    print(score, "failed!")
    
# 100 passed!
# 68 failed!
# 95 passed!
# 84 failed!
# 79 failed!
# 99 passed!

```

Dict iteration ex:

```python
students = {
  'taq': [86, 45, 98, 100],
  'sue': [100, 100, 100, 100],
  'jon': [38, 49, 90, 87],
}

def avg(list_of_grades):
  sum = 0
  for grade in list_of_grades:
    sum = sum + grade
  
  return sum / len(list_of_grades)
  
for student, grades in students.items():
  avg_student = avg(grades)
  if avg_student > 70:
    print(f"{student} passed with avg of {avg_student}")
  else:
    print(f"{student} failed with avg of {avg_student}")
```

Want index number in array loop?

```python
test_scores = [100, 68, 95, 84, 79, 99]
for idx, score in enumerate(test_scores):
  print(idx, score)
```

## 🚗 Practice: Shopping List Calculator VI

Write a function **`compute_total`** that takes a **list** of tuples like so: **`('orange juice', 4.00)`**, iterates over them and returns the total cost including tax.

## 🚗 Practice: Shopping List Calculator VII

Write a function **`compute_total_with_dict`** that takes a **dict** like so: **`{'orange juice': 4.00}`**, iterates over them and returns the total cost including tax.

## 🚗 Practice: Shopping List Calculator VIII

Write a function **`compute_total_with_quant_1`** that takes a **list** of tuples like so: **`('orange juice', (4.00, 3))`**, iterates over them and returns the total cost including tax.

## 🚗 Practice: Shopping List Calculator IX

Write a function **`compute_total_with_quant_2`** that takes a **dict** like so: **`{'orange juice': (4.00, 3)}`**, iterates over them and returns the total cost including tax.

## 🚗 Practice: Shopping List Calculator X

Let's improve our calculator! Remember **[this](https://github.com/mottaquikarim/Python101/tree/master/Basic_Data_Types#-practice-shopping-list-calculator-i)** problem? Let's do it again, but this time - instead of hardcoding the variables, let's use a loop. Based on the inputs below, develop a problem where user can interactively add as many shopping list items as he wants and see the running total:

(The *>* is computer prompt, *<* is user response)

```
> How many items?
< 2
> 1. Enter name of item:
< Eggs
> 1. Enter price of item:
< 2.00
> 1. Enter quantity of item:
> 6

> 2. Enter name of item:
< Steak
> 2. Enter price of item:
< 14.00
> 2. Enter quantity of item:
> 1

> Your total is: 26.00
> Tax is: 2.28
> Total total is: 28.28

```
