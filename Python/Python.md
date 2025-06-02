# Python
 __string__ **string** <br> _string_ *string* 
 > intending    $+$ $-$ for entering maths symbols

`--Type with no bold--`


```python
## print("Hello World")
# multipl line comment ''' or """
"""
a -  add one cell above
b - add one cell below
dd - delete the cell
z - undo
r - raw cell
m - markdown
y - code
"""
w = 5
print(id(w))    # adress of w
a = int(input("Enter a number : "))
print("Inputed number is ",a,"is a",type(a))
print("Number inputed is a Int? ",isinstance(a,int))
print("The adress of the variable inputed is : ",id(a))
```

    140715044579896
    Enter a number :  25
    Inputed number is  25 is a <class 'int'>
    Number inputed is a Int?  True
    The adress of the variable inputed is :  140715044580536
    

# String 


```python
# dir(str) - gives all the method for string
fname="Thomas"
lname="Mathew"
fullname=" "+fname+" "+lname  # concatenation
print(fullname)
print(fullname[2],fullname[-2],sep="\t")
print(fullname[0:6])      # slicing from 0 to 5
print(fullname[0::2])     # slicing with step size 2
print(fullname[0::-1])    # gives empty string
print("Thomas" in fullname)
age = 22
print("{} is a programmer at age of {}.".format(fname,age))    # formatting 
print(len(fname))
for s in fname:
    print(s,end=" ")
if "Thomas" in fullname:
    print("\n\tHi")
# Upper() & lower() 
# capitalize() - only first letter of first word to capital
# strip() removes white spaces before & anfer the text
print(fname.upper())
print(fullname.replace("a","A"))
print(fullname.replace("Thomas Mathew","no name"))  # helps edit the data
fullname = fullname.replace("Thomas Mathew","no name")
print(fullname.split())
y,z = fullname.split()
print(y)
print(fullname.strip())
```

     Thomas Mathew
    h	e
     Thoma
     hmsMte
     
    True
    Thomas is a programmer at age of 22.
    6
    T h o m a s 
    	Hi
    THOMAS
     ThomAs MAthew
     no name
    ['no', 'name']
    no
    no name
    


```python
fullname = "Muhammed sayees"
print(fullname)
fullname = "".join(reversed(fullname))
print(fullname)
print(fullname[::-1],"------------- Reversed in the previous line and now turned back")
par = "Natural Language Processing with python and R and Java"
print(par.partition("and"))       # Split the sentense at the first specified word
print(par.count("a"))
a = "             &&&&&&&&    ****Funny Statement*********     %&&&&&&     "  
print(a.strip())                  # Strip applications
print(a.strip(" &"))
print(a.strip(" &*%"))
print(par.title())                # Every word first letter capital
print(par.capitalize())  
```

    Muhammed sayees
    seeyas demmahuM
    Muhammed sayees ------------- Reversed in the previous line and now turned back
    ('Natural Language Processing with python ', 'and', ' R and Java')
    8
    &&&&&&&&    ****Funny Statement*********     %&&&&&&
    ****Funny Statement*********     %
    Funny Statement
    Natural Language Processing With Python And R And Java
    Natural language processing with python and r and java
    

# List
> - Square Brackets []


```python
lists=["job",1,2,3,"hj"]   # empty list -> l = []   or   l = list()
for i in lists:
    print(i,end="  ")
print("\n"+lists[4])
print(lists[0:3])
print(lists)
a = lists
id(a) == id(lists)  # refer the same element,i.e, a and b will have same val no matter what chane is made
print("\n----------------------Insertion and Deletion----------------------------")
lists.append(10)    # add new element to the end
lists.extend([6,7]) # add multiple elements
lists.insert(0,2)   # insert 2 at loc 0
print(lists) 
lists.remove("hj")  # delete the element
lists.pop(0)        # delete element at loc 0
del lists[6]        # delete from loc 6 or "del lists" deletes the whole list
print(lists)
print("\n-------------------Printing Methods-------------------------------")
print(lists[-1:-6:-2])
print(lists[-3:])
print(a)
a[2:5] = []
print(a)
print("\n-----------------Lenth and Nested List---------------------------------")
print(len(a))    # length 
x = [lists,a]    # nested list
print(x)
print("x[1][0] =",x[1][0])
print("\n--------------------List with Same Elements------------------------------")
b = [2]*5
print(b)
print(2 in b)
print("\n----------------------Matrix ----------------------------")
matrix= [[1,9,3,4,4],[2,3,4,5,6]]
print(matrix[1][2])
print(matrix)
print("\n----------------------Operations on list----------------------------")
print(lists)
print(lists.count("job"))
print(lists.index("job"))
a.reverse()
print(a)
# print(a.sort())  --  can't sort, different data types
a.clear()
print(a)
```

    job  1  2  3  hj  
    hj
    ['job', 1, 2]
    ['job', 1, 2, 3, 'hj']
    
    ----------------------Insertion and Deletion----------------------------
    [2, 'job', 1, 2, 3, 'hj', 10, 6, 7]
    ['job', 1, 2, 3, 10, 6]
    
    -------------------Printing Methods-------------------------------
    [6, 3, 1]
    [3, 10, 6]
    ['job', 1, 2, 3, 10, 6]
    ['job', 1, 6]
    
    -----------------Lenth and Nested List---------------------------------
    3
    [['job', 1, 6], ['job', 1, 6]]
    x[1][0] = job
    
    --------------------List with Same Elements------------------------------
    [2, 2, 2, 2, 2]
    True
    
    ----------------------Matrix ----------------------------
    4
    [[1, 9, 3, 4, 4], [2, 3, 4, 5, 6]]
    
    ----------------------Operations on list----------------------------
    ['job', 1, 6]
    1
    0
    [6, 1, 'job']
    []
    

### Tuple  
> - immutable
> - Parenthesis()


```python
t = 3,4,5,'hj'      # no bracket required or t = (3,4,5,'hj')
print(t)
u = t,(1,9,4,11)    # nested tuple
print(u)
tt = ("Hellow",)    # single element use a comma
print(tt)
print(len(u))
print(t[-1])
a = t + tt
print(a)
print(tt*3)
print(3 in t)
print(3 not in t)
del a               # delete whole tuple
```

    (3, 4, 5, 'hj')
    ((3, 4, 5, 'hj'), (1, 9, 4, 11))
    ('Hellow',)
    2
    hj
    (3, 4, 5, 'hj', 'Hellow')
    ('Hellow', 'Hellow', 'Hellow')
    True
    False
    

# Set  
> - mutable-initial elements cannot be changed but can add and delete elements
> - no duplicate element
> - no index (no order)
> - Curly Brackets / Braces {}


```python
s = {1,2,3,4,"hellow"}
print(s)
s.add("hi")        # add element
s.update({6,7,8})  # add multiple elements
print(s)
s.remove(1)        # remove 1 and error if not found
s.discard(2)       # remove 2 and no error if not found
print(s)
# union
a = {3,4,5,6,7,8,"abbc"}
b = s.union(a)
print(b)
c = s | a
print(c)
# intersection
d = s & a
print(d)
e = s.intersection(a)
print(e)
e.clear()          # Delete all elemnets
print(e)  
del e              # completely deleted
```

    {1, 2, 3, 4, 'hellow'}
    {1, 2, 3, 4, 6, 7, 8, 'hellow', 'hi'}
    {3, 4, 6, 7, 8, 'hellow', 'hi'}
    {3, 4, 5, 6, 7, 8, 'abbc', 'hellow', 'hi'}
    {3, 4, 5, 6, 7, 8, 'abbc', 'hellow', 'hi'}
    {3, 4, 6, 7, 8}
    {3, 4, 6, 7, 8}
    set()
    

# Dictionary
> -  no duplicate
> - other same as list
> - Curly Brackets{}


```python
d = {"k1":"val1","k2":"val2","k3":"val3","k4":"val4","k4":"val4"}
print(d)
print(d["k3"])
print(d.keys())
print(d.values())
print(d.items())
print("k1" in d)
d["k1"] = 5
print(d["k1"])
d.update({5:True,6:"abc"}) # add element and key
print(d)
d.pop(5)           # delete the key and item associated 
d.popitem()        # delete last element 
print(d)
d.clear()
print(d)
del d
```

    {'k1': 'val1', 'k2': 'val2', 'k3': 'val3', 'k4': 'val4'}
    val3
    dict_keys(['k1', 'k2', 'k3', 'k4'])
    dict_values(['val1', 'val2', 'val3', 'val4'])
    dict_items([('k1', 'val1'), ('k2', 'val2'), ('k3', 'val3'), ('k4', 'val4')])
    True
    5
    {'k1': 5, 'k2': 'val2', 'k3': 'val3', 'k4': 'val4', 5: True, 6: 'abc'}
    {'k1': 5, 'k2': 'val2', 'k3': 'val3', 'k4': 'val4'}
    {}
    

# Conditional statemnets
> The tab after a conditional statement or loop known as **Indentation** 


```python
a=5
b=6
"""
mulitiple line
comment
"""
if a==5 and b==6:                 # comment-> single line
    print("True 1")
elif a==b or a>=b:                 
    print("True 2")
else:
    print("False")
print(not(a>b))                   # not operation
for i in range(0,10,2):
    print(i,end=" ")
else:
    print("\nLoop ended")         # for loop can have a else statement
for i in range(10):
    pass                          # If loop have no body using a pass can prevent any errors
```

    True 1
    True
    0 2 4 6 8 
    Loop ended
    


```python
age = int(input("Enter the age :")) # validation int()
if age > 17 :
    print("Adult")
else :
    print("Not Adult")
print("Out of \"if-else\" statement.")
```

    Enter the age : 25
    Adult
    Out of "if-else" statement.
    

# Match 
> __same as switch__


```python
day = 8
while day>7:
    day = int(input("Enter a number : "))
    match day:
        case 1:
            print("Sunday")
        case 2 | 3 | 4 | 5 | 6:
            print("Working Day")
        case 7:
            print("Saturday")
        case _:
            print("Please enter a valid number! (Between 1 to 7)")

```

    Enter a number :  2
    Working Day
    

# Lambda Function
>  Small anonymous function typically used for short, simple functions that are not reused elsewhere in your code.


```python
add = lambda x,y:x+y
print(add(5,9))
add10 = lambda a:a+10
print(add10(5))
# example -a function that triple any values
def my_tri(n):
    return lambda a: a*n
num = my_tri(3)
print(num(10))
```

    14
    15
    30
    

# Break and Continue 


```python
i = 10
while i >= 1:
    if i == 5:
        break       # end all loops it is inside of
    else:
        print(i,end="  ")
    i -= 1
i = 11
print("\n")
while i >= 1:
    i -= 1
    if i == 5:
        continue   # end curent itteration and start the next one(skip one step)
    else:
        print(i,end="  ")
else :             # while can have else as there is no do while in python
    print(f"\nCompleted while loop with value of i as {i}")
```

    10  9  8  7  6  
    
    10  9  8  7  6  4  3  2  1  0  
    Completed while loop with value of i as 0
    

# Functions


```python
def name(fname,lname):
    fullname=fname + " " + lname
    return fullname
fullname = name("Thomas","Mathew")
print(fullname)
def rec(a):                   # recursion :- function that calls itself
    if a>0:
        res = a + rec(a-1)
        # print(res)
    else:
        res = 0
    return(res)
print(rec(6))
```

    Thomas Mathew
    21
    

## Arbitary Arguments, *args


```python
def selection(*kid):                   
    print("Selected",kid[2])
selection("Aju","Appu","Vavva","Kunj")
```

    Selected Vavva
    

## Keyword Arguments
>send arguments with the key = value syntax.


```python
def s(a1,a2,a3):
    print(a3)
s(a3 = 3,a2 = 2,a1 = 1)
def ss(**a):       # can give Arbitrary Keyword Arguments, **kwargs
    print(a['a2'])
ss(a1 = 1,a2 = 2,a3 = 3)

```

    3
    2
    

## Other function types


```python
def s(a = "23"):    # default value will be taken if argument is empty
    print(a)
s(5)
s() 
def a(b):           # list as parameters
    for i in b:
        print(i,end=" ")
c = [123,344,456,678,890]
a(c)
```

    5
    23
    123 344 456 678 890 

# Python Classes and Objects

**Class** 
>Blueprint or template for creating an object.  
>- Attributes (data)  
>- Methods (functions that act on the data)

**Object**  
>An instance of a class. It holds actual data and can use the class methods.

## `__init__()` - Constructor 
> -  function to assign values to object properties, or other operations that are necessary to do when the object is being created.
> -  executed when the class is being initiated.


**Self Parameter**
> -  The self parameter is a reference to the current instance of the class, and is used to access variables that belong to the class.
> -  It does not have to be named self, you can call it whatever you like, but it has to be the first parameter of any function in the class


```python
class human:
    def __init__(self, name, sex, age):
        self.name = name            # -> proprties name, sex, age
        self.sex = sex
        self.age = age
person = human("Sayees","Male",21)
print(person.name)
print(person.sex)
print(person.age)
person.name = "Zoro"  # modify object properties
print("New name :",person.name)
print(person)         # can't print this way
class mmm:
    pass              # pass the class, no error even tho no body for class
```

    Sayees
    Male
    21
    New name : Zoro
    <__main__.human object at 0x000002BEF3C0AFD0>
    


```python
class human:
    def __init__(self, name, sex, age):
        self.name = name
        self.sex = sex
        self.age = age
    def __str__(self):             # function defines what to print when the object is printed
        return f"{self.name} is a {self.sex}, {self.age} year's old."     
p1 = human("Muhammed","Male",25)
print(p1)
```

    Muhammed is a Male, 25 year's old.
    

## Object Methods
> - Can access or modify object state.


```python
class hum:
    def __init__(per, name, age):     # self or any name preffered 
        per.name = name
        per.age = age
    def func(per):
        print(f"{per.name} is inside the object function")
p1 = hum("Zoro",25)
p1.func()
del p1.name    # delete object property
del p1         # delete object
```

    Zoro is inside the object function
    

## Class Method
> - Can access/modify class-level data, not instance data.


```python
class hum:
    cont = 25     # class level data
    
    @classmethod   # must define
    def print_c(cls, a):
        cls.count = a
        print(f"Count = {cls.count}")
hum.print_c(25)
```

    Count = 25
    

## Static Methods
> - Behave like regular functions inside a class.
> - Don’t take self or cls.


```python
class hum:
    @staticmethod
    def add(a, b):
        return a + b

print(hum.add(35,40))
```

    75
    

# Inheritance 


```python
class human:
    def __init__(self, fname, lname):
        self.fname = fname
        self.lname = lname
    def print_n(self):
        print(self.fname,self.lname)

class student(human):                      # child class declaration; here parent class = human & child class = student
    pass
p1 = student("Freddy","Mercury")
p1.print_n()
```

    Freddy Mercury
    


```python
class human:
    def __init__(self, fname, lname):
        self.fname = fname
        self.lname = lname
    def print_n(self):
        print(self.fname,self.lname)

class student(human):                     
    def __init__(self, fname, lname, school):  # child __init__() overides the parent function
        self.fname = fname
        self.lname = lname
        self.school = school
p1 = student("Freddy","Mercury","Cbse")
p1.print_n()
```

    Freddy Mercury
    

## Super function


```python
class human:
    def __init__(self, fname, lname):
        self.fname = fname
        self.lname = lname
    def printn(self):
        print(self.fname,self.lname)
class student(human):                     
    def __init__(self, fname, lname, school): 
        super().__init__(fname,lname)             # Call the parent class constructor
        self.school = school
    def pri(self):
        print(self.fname,self.lname,"is studying in",self.school)
        
p1 = student("Freddy","Mercury","Cbse")
p1.pri()
```

    Freddy Mercury is studying in Cbse
    

# Iteratos
> - The `__iter__()` method acts similarly; you can perform operations (like initialization), but it must always return the iterator object itself.

> - The `__next__()` method also allows you to perform operations and must return the next item in the sequence.



```python
l = ["Apple","Orange","Banana"]
it = iter(l)    # Built-in Iterator
print(next(it))
print(next(it))
print(next(it))

for i in l:    # Python handles the iterator automatically
    print(i)
a = "abcd"
b = iter(a)
print(next(b))
print(next(b))
print(next(b))
print(next(b))
```

    Apple
    Orange
    Banana
    Apple
    Orange
    Banana
    a
    b
    c
    d
    


```python
class number:
    def __init__(self, limit):
        self.limit = limit
    def __iter__(self):
        self.count = -1  # can be also given in the init function
        return self
    def __next__(self):
        if self.count < self.limit:
            self.count +=1
            return self.count
        else :
            raise StopIteration        # raise error
c = number(5)
for num in c:
    print(num,end = " ")
print()
myc = number(6)
myiter = iter(myc)
for i in myiter:
    print(i,end=" ")
```

    0 1 2 3 4 5 
    0 1 2 3 4 5 6 

# Polymorphism
> - In programming it refers to methods/functions/operators with the same name that can be executed on many objects or classes.
> - Example: **len()** - return length of string, number of elements in tuple and no of key-value pairs in dictionary. 


```python
class car:
    def __init__(self, name, brand):
        self.name = name
        self.brand = brand
    def move(self):
        print("Drive")
class boat:
    def __init__(self,name,brand):
        self.name = name
        self.brand = brand
    def move(self):
        print("Sail")
class plane:
    def __init__(self,name,brand):
        self.name = name
        self.brand = brand
    def move(self):
        print("Fly")

car1 = car("Aulto","Suzuki")
boat1 = boat("Ibiza", "Touring 20") 
plane1 = plane("Boeing", "747")  
for i in (car1,boat1,plane1):
    i.move()
```

    Drive
    Sail
    Fly
    

## Polymorphism in Inheritance 


```python
class transport:                      # Parent class
    def __init__(self, name, brand):
        self.name = name
        self.brand = brand
    def move(self):
        print("Drive")
class car(transport):                 # Child class 1
    pass
class boat(transport):                # Child class 2
    def move(self):
        print("Sail")
class plane(transport):               # Child class 3
    def move(self):
        print("Fly")
car1 = car("Aulto","Suzuki")
boat1 = boat("Ibiza", "Touring 20") 
plane1 = plane("Boeing", "747")  
for i in (car1,boat1,plane1):
    print(i.name,"-",i.brand)
    i.move()
```

    Aulto - Suzuki
    Drive
    Ibiza - Touring 20
    Sail
    Boeing - 747
    Fly
    

# Python Scope
## Local Scope
> A variable created inside a function belongs to the local scope of that function, and can only be used inside that function.
## Global Scope
> A variable created in the main body of the Python code is a global variable and belongs to the global scope.
> Global variables are available from within any scope, global and local.
## Global Keyword
> - If you need to create a global variable, but are stuck in the local scope, you can use the **global** keyword.
> - The global keyword makes the variable global.
> - Use the global keyword if you want to make a change to a global variable inside a function.
## Nonlocal Keyword
> - The **nonlocal** keyword is used to work with variables inside nested functions.
> - The nonlocal keyword makes the variable belong to the outer function.


```python
x = 500
print(x)
def fun():
    global x
    x = 300
    print(x)
fun()
print(x)
```

    500
    300
    300
    


```python
def fun():
    x = "Hello"
    print(x)
    def fun1():
        nonlocal x
        x = "Hi"
        print(x)
    fun1()
    return x
print(fun())
```

    Hello
    Hi
    Hi
    


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```
