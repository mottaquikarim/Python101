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
