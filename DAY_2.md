#### DAY 2-Types of data

### Keywords and identifiers 
Certain rules persist while writing keywords
- no space in between
- should not start with a number
- underscore between two names / second word first letter caps etc


### Indentation
### Comment 
Not a part of programming execution. Represented by #. Just for reading purpose. If there are multiple comments, then triple quotes ''' can be used

- variable size, so python dynamically allocate this, convenient for programmers but a delay in processing (not that much affected). For other language, fixed memory.

() - mostly depicts function

#### Data type
##### Numerals
- integer
- float
- complex - contain real and imaginary part eg: (3+4j)
To know which of the following are used, there is a type function. **type( )**

##### Data
Can use both "", '', but should always be in between them
then only the type function shows **string**

**len( ) -used to know the length of the word (space is also considered as a character). 

- eg:  len(Adita) output is 5


### Sequence Type
- list- collection of elements grouped together. Can be of any type including string, float, int etc. For c++ it should be of single type
- List represented by square bracket **[0, 1, 2, 3, 4]**
- eg: vowels = **['a', 'b', 'c', 'd']**
- **len ( ) of list gives individual characters**


### Mutable - Can be changed
List can be changed, string cannot be changed

**indexing** - all elements are indexed starting from 0
**.append** - command for appending a new element into a list
my_tuple similar to list but immutable, once you create, cannot add, or change or remove

### Range
immutable sequence of nos
if 1 nos - range(4) = 0,1,2,3
if 2 nos - range (0,4) = start, stop (0 is the start, 4 is stop, does not include 4)
if 3nos -  range(0,10,2) = 

### Mapping type
##### 1. Dictionary
- collection of data and key value pairs
- unordered, mutable
- each key in a dictionary must be unique, while values can be duplicated
eg: "Institute" : "ICT"
"City" : "Trivandrum"
- represented by { }

**data.keys**( ), **data.values**( )
"Institute",    "ICT"
"City"             "Trivandrum"

##### 2. Set
- unordered collection of nos
- no duplication of repetition of elements allowed
- even if elements repeated, it will not be read
- set is used to find unique elements.
- eg: list = [2, 3, 2, 4, 8, 8, 7, 9, 5, 4, 1, 0, 0, 5, 6 ,8]
     set(list) = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}


#### 3. Boolean Type
- can be either true or false
- used as conditional statements

#### 4. None type


### Operations
1.Arithmetic
2.Comparison
3.Logical
4. Membership Operators
5.Identity


#### 1.Arithmetic
Addition, Subtraction, Multiplication, Division
- In division // gives the answer without reminder
- Modulus -% - to find reminder of a division
- Exponential - **


#### 2.Comparison
== equal
!= not equal
< greater
<= greater or equal

#### 3.Logical Operations
AND - (BOTH TRUE) THEN TRUE
OR -  (ANY ONE TRUE) THEN TRUE
NOT- (INVERSE)


#### 4.Membership Operations
Also work in string
print("a" in ["a", "b", "c"])
output = true


#### CONDITIONAL STATEMENTS
If condition:
	print()
else condition
	print()
elif condition
	print()

This was some of the keywords and Types of data while working with python.
