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

## Comprehensions
