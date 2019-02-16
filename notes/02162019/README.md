* declarations
* expressions
* statements

DECLARATION

store a piece of data into some sort of container...which we call a variable

x = 2
       ^ datatype
          - number: numeric values ie from algebra
          - string: anything within quotes, represents arbitrary sequences of character
          - boolean: true/false
          - list: a collection of numbers, strings, booleans or other lists
          - dictionary: a collection of numbers, strings, booleans, etc BUT indexed with a keyword
        
mylist = ['a', 'b', 'c']
myname = 'taq'

EXPRESSIONS

operate on your datatypes

1 + 1 = 2
'+' => operator


my_age = 28
num_years = 10
my_future_age = my_age + num_years

my_first_name = 'Taq'
my_last_name = 'Karim'
my_fullname = my_first_name + my_last_name 
                          => 'TaqKarim'

arithmetic operators:
+
-
* => multiplication
/ => division
% => modulus, this gives you the remainder
    4 % 2 = 0 
** => exponent, 4 ** 2 = 16

string operators:
+ => concatenation 

logical operators:
== , this means "is equal to"
>=
<=
!=, this means "is NOT equal to"



STATEMENTS

allow the programmer to determine "control flow"

my_height = 61
if my_height >= 65:
    can_I_go_on_ride = True 
else:
    can_I_go_on_ride = False

-------------------------------------

my_height = 61
can_I_go_on_ride = (my_height >= 65)

while True:
    print "hi"


counter = 0
while counter < 3:
    print counter
    counter = counter + 1
print("tada!")

counter | counter < 10 | counter = counter + 1
-------------------------------------------------------
     0      | 0 < 3 = True | 1
-------------------------------------------------------
     1      | 1 < 3 = True | 2
-------------------------------------------------------
     2      | 2 < 3 = True | 3
-------------------------------------------------------
     3      | 3 < 3 = False
"tada"


