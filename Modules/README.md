# Modules

We can leverage modules to import useful tools that others wrote for our own implementation purposes.

For example, how would you generate a random number in python?

```python
from random import randint

print(randint(1,10)) # prints random number between 1 and 10
```
**[rtfm](https://docs.python.org/3/library/random.html#random.randint)**

Another example

```python
from calendar import month

print(month(2018, 11)

#    November 2018
# Mo Tu We Th Fr Sa Su
#           1  2  3  4
#  5  6  7  8  9 10 11
# 12 13 14 15 16 17 18
# 19 20 21 22 23 24 25
# 26 27 28 29 30
```

Third example

```python
import datetime
now = datetime.datetime.now()
print(now.year, now.month, now.day, now.hour, now.minute, now.second)
```

## 🚗 Practice: Today's Calendar

Write a function that returns the calendar output above, but for **TODAYs** month and year

## 🚗 Practice: Random Calendar

Write a function that returns calendar output above, but for a **RANDOM** month and year

## 🚗 Challenge: Numbers API

The python **[requests](http://docs.python-requests.org/en/master/)** module is used to make arbitrary web url requests in python. Using the docds in requests, write a function that calls out to **[this API](http://numbersapi.com/#json)** and returns the result in console.

If you want to really have fun, make it interactive where python asks user for a number, you validate that it is a number and then issue a response.

```
> Give me a number
< lol trollin
> Sorry, that is not a number. Give me a number
< 38
> 38 is the number of minutes in the shortest war in history in which Zanzibar surrendered to England in 1896.

```
