*Live and Learn and Pass It On.*
# Pybaby
These babies want to learn Python

#What?

Python is

1. Easy to learn
2. Object oriented
3. Elegant syntax and dynamic typing

# Get started

1. Comments

    ```python

    # this is the first comment
    spam = 1  # and this is the second comment
              # ... and now a third!
    text = "# This is not a comment because it's inside quotes."
    ```

2. Using Python as a Calculator

    ```python
    >>> 2 + 2
    4
    >>> 50 - 5*6
    20
    >>> (50 - 5*6) / 4
    5.0
    >>> 8 / 5  # division always returns a floating point number
    1.6
    >>> 17 / 3  # classic division returns a float
    5.666666666666667
    >>>
    >>> 17 // 3  # floor division discards the fractional part
    5
    >>> 17 % 3  # the % operator returns the remainder of the division
    2
    >>> 5 * 3 + 2  # result * divisor + remainder
    17
    # With Python, it is possible to use the ** operator to calculate powers
    >>> 5 ** 2  # 5 squared
    25
    >>> 2 ** 7  # 2 to the power of 7
    128
    # The equal sign (=) is used to assign a value to a variable. Afterwards,
    # no result is displayed before the next interactive prompt:
    >>> width = 20
    >>> height = 5 * 9
    >>> width * height
    900
    >>> n  # try to access an undefined variable
    >>> # see error
    >>> 
    >>> # mixed type operands convert the integer operand to floating point:
    >>> 3 * 3.75 / 1.5
    7.5
    >>> _
    7.5
    >>> # the last printed expression is assigned to the variable _.
    >>> # Basic classes - Oop
    >>> num = int()
    >>> type(num)
    <class 'int'>
    >>> # The int() returns an integer object constructed from a number or 
    >>> # string x, or return 0 if no arguments are given.
    >>> int()
    0
    >>> num
    0
    >>> int(3)
    3
    >>> char = str()
    >>> char
    ''
    >>> type(char)
    <class 'str'>
    >>> str()
    ''
    >>> str(2)
    '2'
    >>> str(234)
    '234'
    ```
    Note: Python 2.7 uses integer divison by default (3/2=1), one needs to import the following to use float divison as default.
    ```python
    >>> from __future__ import divison
    >>> 3/2
    1.5
    >>> 3//2
    1
    ```
    

3. Strings

    ```python
    >>> 'spam eggs'  # single quotes
    'spam eggs'
    >>> 'doesn\'t'  # use \' to escape the single quote...
    "doesn't"
    >>> "doesn't"  # ...or use double quotes instead
    "doesn't"
    >>> '"Yes," he said.'
    '"Yes," he said.'
    >>> "\"Yes,\" he said."
    '"Yes," he said.'
    >>> '"Isn\'t," she said.'
    '"Isn\'t," she said.'
    >>> s = 'First line.\nSecond line.'  # \n means newline
    >>> s  # without print(), \n is included in the output
    'First line.\nSecond line.'
    >>> print(s)  # with print(), \n produces a new line
    First line.
    Second line.
    >>> # Strings can be concatenated (glued together) with the + operator,
    >>> # and repeated with *
    >>> # 3 times 'un', followed by 'ium'
    >>> 3 * 'un' + 'ium'
    'unununium'
    >>> # try
    >>> 2 * 'one' + 3 * 'two'
    'oneonetwotwotwo'
    >>> # Two or more string literals next to each other are automatically 
    >>> # concatenated.
    >>> 'Py' 'thon'
    'Python'
    >>> # If you want to concatenate variables or a variable and a literal, 
    >>> # use +
    >>> prefix = 'Py'
    >>> prefix + 'thon'
    'Python'
    >>> # Put several strings within parentheses to have them joined together.
    >>> num = ('one''two''three')
    >>> num
    'onetwothree'
    >>> # Strings can be indexed (subscripted), with the first character
    >>> # having index 0
    >>> word = 'Python'
    >>> word[0]  # character in position 0
    'P'
    >>> word[5]  # character in position 5
    'n'
    >>> # Indices may also be negative numbers, to start counting from the
    >>> # right
    >>> word[-1]  # last character
    'n'
    >>> word[-2]  # second-last character
    'o'
    >>> word[-6]
    'P'
    >>> # Note that since -0 is the same as 0, negative indices start from -1.
    >>> # slicing allows you to obtain substring.
    >>> word[0:2]  # characters from position 0 (included) to 2 (excluded)
    'Py'
    >>> word[2:5]  # characters from position 2 (included) to 5 (excluded)
    'tho'
    >>> word[:2] + word[2:]
    'Python'
    >>> word[:4] + word[4:]
    'Python'
    >>> word[:2]  # character from the beginning to position 2 (excluded)
    'Py'
    >>> word[4:]  # characters from position 4 (included) to the end
    'on'
    >>> word[-2:] # characters from the second-last (included) to the end
    'on'
    >>> # Python strings cannot be changed — they are immutable.
    >>> word[0] = 'J'
    >>> # gives error
    >>> # If you need a different string, you should create a new one:
    >>> 'J' + word[1:]
    'Jython'
    >>> word[:2] + 'py'
    'Pypy'
    >>> s = 'supercalifragilisticexpialidocious'
    >>> # String length
    >>> len(s)
    34
    ```

4. Lists

    ```python
    >>> squares = [1, 4, 9, 16, 25]
    >>> squares
    [1, 4, 9, 16, 25]
    >>> squares[0]  # indexing returns the item
    1
    >>> squares[-1]
    25
    >>> squares[-3:]  # slicing returns a new list
    [9, 16, 25]
    >>> # All slice operations return a new list containing the requested 
    >>> # elements. This means that the following slice returns a new (
    >>> # shallow) copy of the list:
    >>> squares[:]
    [1, 4, 9, 16, 25]
    >>> # Lists also support operations like concatenation:
    >>> squares + [36, 49, 64, 81, 100]
    [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
    >>> # Instead of modifying the original list you can also do
    >>> new_squares=squares+[121,144,169]
    >>> #Does not modify squares.
    >>> # Unlike strings, which are immutable, lists are a mutable type
    >>> cubes = [1, 8, 27, 65, 125]  # something's wrong here
    >>> 4 ** 3  # the cube of 4 is 64, not 65!
    64
    >>> cubes[3] = 64  # replace the wrong value
    >>> cubes
    [1, 8, 27, 64, 125]
    >>> # Add to lists
    >>> cubes.append(7 ** 3)  # and the cube of 7
    >>> # Assignment to slices is also possible, and this can even change the
    >>> # size of the list or clear it entirely
    >>> letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
    >>> letters
    ['a', 'b', 'c', 'd', 'e', 'f', 'g']
    >>> # replace some values
    >>> letters[2:5] = ['C', 'D', 'E']
    >>> letters
    ['a', 'b', 'C', 'D', 'E', 'f', 'g']
    >>> # Length of lists -- no. of elements in the list.
    >>> len(letters)
    7
    >>> # now remove them
    >>> letters[2:5] = []
    >>> letters
    ['a', 'b', 'f', 'g']
    >>> # clear the list by replacing all the elements with an empty list
    >>> letters[:] = []
    >>> letters
    []
    >>> # It is possible to nest lists.
    >>> a = ['a', 'b', 'c']
    >>> n = [1, 2, 3]
    >>> x = [a, n]
    >>> x
    [['a', 'b', 'c'], [1, 2, 3]]
    >>> x[0]
    ['a', 'b', 'c']
    >>> x[0][1]
    'b'
    >>> # Swap
    >>> a,b = 1,2
    >>> a, b = b, a
    >>> a, b
    (2, 1)
    >>> a = [66.25, 333, 333, 1, 1234.5]
    >>> print(a.count(333), a.count(66.25), a.count('x'))
    2 1 0
    >>> # Insert an item at a given position. Below inserts at position 2
    >>> a.insert(2, -1)
    >>> a.append(333)
    >>> a
    [66.25, 333, -1, 333, 1, 1234.5, 333]
     >>> #Extending a list is easy.
    >>>a=[1,2,3]
    >>>a.extend([4,5,6])
    >>>a
    [1, 2, 3, 4, 5, 6]
    >>> a.index(333)
    1
    >>> a.remove(333)
    >>> a
    [66.25, -1, 333, 1, 1234.5, 333]
    >>> a.reverse()
    >>> a
    [333, 1234.5, 1, 333, -1, 66.25]
    >>> a.sort()
    >>> a
    [-1, 1, 66.25, 333, 333, 1234.5]
    >>> # Pop - Removes the item at the given position in the list, and return 
    >>> # it. If no index is specified, a.pop() removes and returns the last 
    >>> # item in the list.
    >>> a.pop()
    1234.5
    >>> a
    [-1, 1, 66.25, 333, 333]
    >>> #You can also check for list membership using in keyword
    >>> 1 in a
    True
    >>> 15 in a
    False
    ```

5. Dicts
    Dictionary as an unordered set of key: value pairs, with the requirement that the keys are unique (within one dictionary).

    Dictionaries are indexed by keys, which can be any `immutable` type; strings and numbers can always be keys. Tuples can be used as keys if they contain only strings, numbers, or tuples; if a tuple contains any mutable object either directly or indirectly, it cannot be used as a key. You can’t use lists as keys, since lists can be modified in place using index assignments, slice assignments, or methods like append() and extend().


    ```python
    # Initializing
    >>> first = dict()
    >>> first
    {}
    >>> type(x)
    <class 'dict'>
    >>> # initialize dict
    >>> tel = {'jack': 4098, 'sape': 4139}
    >>> # add a key-value pair
    >>> tel['guido'] = 4127
     >>> # display all key-values
    >>> tel
    {'sape': 4139, 'guido': 4127, 'jack': 4098}
    >>> # Value corresponding to a key in dict
    >>> tel['jack']
    4098
    >>> # Remove a key 
    >>> del tel['sape']
    >>> tel['irv'] = 4127
    >>> tel
    {'guido': 4127, 'irv': 4127, 'jack': 4098}
    >>> # to be discussed later.
    >>> list(tel.keys())
    ['irv', 'guido', 'jack']
    >>> sorted(tel.keys())
    ['guido', 'irv', 'jack']
    >>> 'guido' in tel
    True
    >>> 'jack' not in tel
    False
    >>> # another way of init
    >>> # The dict() constructor builds dictionaries directly from sequences 
    >>> # of key-value pairs:
    >>> dict([('sape', 4139), ('guido', 4127), ('jack', 4098)])
    {'sape': 4139, 'jack': 4098, 'guido': 4127}
    >>> # dict comprehensions can be used to create dictionaries from 
    >>> # arbitrary key and value expressions:
    >>> {x: x**2 for x in (2, 4, 6)}
    {2: 4, 4: 16, 6: 36}
    >>> # When the keys are simple strings, it is sometimes easier to specify 
    >>> # pairs using keyword arguments:
    >>> dict(sape=4139, guido=4127, jack=4098)
    {'sape': 4139, 'jack': 4098, 'guido': 4127}
    ```

6. Control flow

    ```python
    >>> x = int(input("Please enter an integer: "))
    Please enter an integer: 42
    >>> if x < 0:
    ...     x = 0
    ...     print('Negative changed to zero')
    ... elif x == 0:
    ...     print('Zero')
    ... elif x == 1:
    ...     print('Single')
    ... else:
    ...     print('More')
    ...
    More
    ```

7. Defining Functions

    ```python
    >>> def fib(n):    # write Fibonacci series up to n
    ...     """Print a Fibonacci series up to n."""
    ...     a, b = 0, 1
    ...     while a < n:
    ...         print(a, end=' ')
    ...         a, b = b, a+b
    ...     print()
    ...
    >>> # Now call the function we just defined:
    ... fib(2000)
    0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987 1597
    ```

8. Sets
    A set is an unordered collection with no duplicate elements. To create an empty set you have to use `set()`, not `{}`; the latter creates an empty dictionary.

    ```python
    >>> basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'}
    >>> print(basket)                      # show that duplicates have been removed
    {'orange', 'banana', 'pear', 'apple'}
    >>> 'orange' in basket                 # fast membership testing
    True
    >>> 'crabgrass' in basket
    False
    >>> a = set('abracadabra')
    >>> b = set('alacazam')
    >>> a                                  # unique letters in a
    {'a', 'r', 'b', 'c', 'd'}
    >>> b
    
    >>> a - b                              # letters in a but not in b
    {'r', 'd', 'b'}
    >>> a | b                              # letters in either a or b
    {'a', 'c', 'r', 'd', 'b', 'm', 'z', 'l'}
    >>> a & b                              # letters in both a and b
    {'a', 'c'}
    >>> # Similarly to list comprehensions, set comprehensions are also 
    >>> # supported:
    >>> a = {x for x in 'abracadabra' if x not in 'abc'}
    >>> a
    {'r', 'd'}
    ```

9. Tuples 
    A tuple consists of a number of values separated by commas

    ```python
    >>> t = 12345, 54321, 'hello!'
    >>> t[0]
    12345
    >>> t
    (12345, 54321, 'hello!')
    >>> # Tuples may be nested:
    ... u = t, (1, 2, 3, 4, 5)
    >>> u
    ((12345, 54321, 'hello!'), (1, 2, 3, 4, 5))
    >>> # Tuples are immutable:
    ... t[0] = 88888
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    TypeError: 'tuple' object does not support item assignment
    >>> # but they can contain mutable objects:
    ... v = ([1, 2, 3], [3, 2, 1])
    >>> v
    ([1, 2, 3], [3, 2, 1])
    ```

    Though tuples may seem similar to lists, they are often used in different situations and for different purposes. Tuples are immutable, and usually contain an heterogeneous sequence of elements that are accessed via unpacking or indexing. Lists are mutable, and their elements are usually homogeneous and are accessed by iterating over the list.

    ```python
    >>> empty = ()  # empty tuple
    >>> singleton = 'hello',  # <-- note trailing comma
    >>> len(empty)
    0
    >>> len(singleton)
    1
    >>> singleton
    ('hello',)
    >>> # sequence/tuple unpacking
    >>> t = 12345, 54321, 'hello!'
    >>> x, y, z = t 
    ```

    This is called, appropriately enough, sequence unpacking and works for any sequence on the right-hand side. Sequence unpacking requires that there are as many variables on the left side of the equals sign as there are elements in the sequence. Note that multiple assignment is really just a combination of tuple packing and sequence unpacking. 
    Apart from being used for multiple assignments, tuples are provide an easy way to return multiple values from a function.

10. Looping 
    
    ```python
    >>> # Loop thru Dict
    >>> knights = {'gallahad': 'the pure', 'robin': 'the brave'}
    >>> for k, v in knights.items():
    ...     print(k, v)
    ...
    gallahad the pure
    robin the brave
    >>> for i, v in enumerate(['tic', 'tac', 'toe']):
    ...     print(i, v)
    ...
    0 tic
    1 tac
    2 toe
    >>> for x in range(4):
    ...     print(x)
    ... 
    0
    1
    2
    3
    >>> for x in range(10):
    ...     if x % 5 == 0: 
    ...         print(x) 
    ...
    ```
    
    
11. Reading & writing Data

    ```python
    >>> f = open('workfile', 'w') #r, w, a, rb, wb, ab,
    >>> f.read()
    'This is the entire file.\n'
    >>> f.read()
    ''
    >>> f.readline() # reading lines
    'This is the first line of the file.\n'
    >>> f.readline()
    'Second line of the file\n'
    >>> f.readline()
    ''
    >>> for line in f:
    ...     print(line, end='')
    ...
    This is the first line of the file.
    Second line of the file
    >>> f.write('This is a test\n')
    15
    >>> value = ('the answer', 42)
    >>> s = str(value)
    >>> f.write(s)
    18
    >>> f = open('workfile', 'rb+') #file positions
    >>> f.write(b'0123456789abcdef')
    16
    >>> f.seek(5)     # Go to the 6th byte in the file
    5
    >>> f.read(1)
    b'5'
    >>> f.seek(-3, 2) # Go to the 3rd byte before the end
    13
    >>> f.read(1)
    b'd'
    >>> f.close() #close
    >>> f.read()
    Traceback (most recent call last):
      File "<stdin>", line 1, in ?
    ValueError: I/O operation on closed file
    >>> with open('workfile', 'r') as f:
    ...     read_data = f.read()
    >>> f.closed
    True
    >>> json.dumps([1, 'simple', 'list'])
    '[1, "simple", "list"]'
    >>> json.dump(x, f)
    >>> x = json.load(f)
    ```

12. List Comprehensions

    List comprehensions provide a concise way to create lists. Common applications are to make new lists where each element is the result of some operations applied to each member of another sequence or iterable, or to create a subsequence of those elements that satisfy a certain condition.

    ```python
    >>> # For example, assume we want to create a list of squares, like:
    >>> squares = []
    >>> for x in range(10):
    ...     squares.append(x**2)
    ...
    >>> squares
    [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
    >>> # Note that this creates (or overwrites) a variable named x that still
    >>> # exists after the loop completes. We can calculate the list of
    >>> # squares without any side effects using:
    >>> squares = [x**2 for x in range(10)]
    >>> # which is more concise and readable.
    ```

    A list comprehension consists of brackets containing an expression followed by a for clause, then zero or more for or if clauses. The result will be a new list resulting from evaluating the expression in the context of the for and if clauses which follow it. For example, this listcomp
    combines the elements of two lists if they are not equal:

    ```python
    >>> [(x, y) for x in [1,2,3] for y in [3,1,4] if x != y]
    [(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]
    ```

    and it’s equivalent to:

    ```python
    >>> combs = []
    >>> for x in [1,2,3]:
    ...     for y in [3,1,4]:
    ...         if x != y:
    ...             combs.append((x, y))
    ...
    >>> combs
    [(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]
    ```

    Examples

    ```python
    >>> vec = [-4, -2, 0, 2, 4]
    >>> # create a new list with the values doubled
    >>> [x*2 for x in vec]
    [-8, -4, 0, 4, 8]
    >>>
    >>> # filter the list to exclude negative numbers
    >>> [x for x in vec if x >= 0]
    [0, 2, 4]
    >>>
    >>> # apply a function to all the elements
    >>> [abs(x) for x in vec]
    [4, 2, 0, 2, 4]
    >>>
    >>> # call a method on each element
    >>> freshfruit = ['  banana', '  loganberry ', 'passion fruit  ']
    >>> [weapon.strip() for weapon in freshfruit]
    ['banana', 'loganberry', 'passion fruit']
    >>>
    >>> # create a list of 2-tuples like (number, square)
    >>> [(x, x**2) for x in range(6)]
    [(0, 0), (1, 1), (2, 4), (3, 9), (4, 16), (5, 25)]
    >>>
    >>> # the tuple must be parenthesized, otherwise an error is raised
    >>> [x, x**2 for x in range(6)]
      File "<stdin>", line 1, in ?
        [x, x**2 for x in range(6)]
                   ^
    SyntaxError: invalid syntax
    >>>
    >>> # flatten a list using a listcomp with two 'for'
    >>> vec = [[1,2,3], [4,5,6], [7,8,9]]
    >>> [num for elem in vec for num in elem]
    [1, 2, 3, 4, 5, 6, 7, 8, 9]
    ```

13. Unpacking Argument Lists

    The reverse situation occurs when the arguments are already in a list or tuple but need to be unpacked for a function call requiring separate positional arguments. For instance, the built-in `range()` function expects separate start and stop arguments. If they are not available separately, write the function call with the *-operator to unpack the arguments out of a list or tuple:

    ```python
    >>> list(range(3, 6))            # normal call with separate arguments
    [3, 4, 5]
    >>> args = [3, 6]
    >>> list(range(*args))           # call with arguments unpacked from a list
    [3, 4, 5]
    ```

    In the same fashion, dictionaries can deliver keyword arguments with the **-operator:

    ```python
    >>> def parrot(voltage, state='a stiff', action='voom'):
    ...     print("-- This parrot wouldn't", action, end=' ')
    ...     print("if you put", voltage, "volts through it.", end=' ')
    ...     print("E's", state, "!")
    ...
    >>> d = {"voltage": "four million", "state": "bleedin' demised", "action": "VOOM"}
    >>> parrot(**d)
    "-- This parrot wouldn't VOOM if you put four million volts through it. E's bleedin' demised !"
    ```
14. Counters
    Sometimes we need to count the number of occurances of various elements in a collection. With introduction of   collections.Counter(2.7 and above), this is now a child's play.

    ```python
    >>> from collections import Counter
    >>> c=Counter([0,0,1,2,0,5])
    >>> c
    Counter({0: 3, 1: 1, 2: 1, 5: 1})
    >>> # Zero occurs thrice, and rest of them once. By Default, the counters are set to zero.
    ```
15. The None Value
     Python uses a quircky keyword to indicate a nonexistent value. None in Python is similar to null in other languages.

    ```python
    >>> q=None
    >>>q
    >>>
    >>> #Nothig will be returned. REMEMBER None is NOT a value, even though the following return true.
    >>> q==None
    True
    >>> q is None # A better Pythonic convention than ==
    True
    ```
16. Zip

    Zip takes in 2 lists, and returns a list of tuples. Each i-th element of the tuple contains the i-th element from  respective lists. The returned list is truncated in length to the length of the shortest argument sequence.

   ```python
   >>> a=[1,2,3]
   >>> b=[4,5]
   >>># In Python 3 to read the elements use the following syntax
   >>>zipped=list(zip(a,b))
   >>>zipped
   >>> [(1, 4), (2, 5)]
   >>>#For unpacking
   >>> a,b,*c=[1,2,3,4,5,6,7]
   >>> a
   1
   >>> b
   2
   >>> c # c stores rest of the elements.
   [3, 4, 5, 6, 7]
   >>> a=[1,2,3,4]
   >>> b=[x*x for x in a]
   >>>for (a,b) in zip(a,b):
   ...  print(a,b)
   ...
   1 1
   2 4
   3 9
   >>> #One can use the zipped techniques for argument packing.
   >>> c=list(range(4,7)) # range takes 2 aruguments, and returns a list 4,5,6 assigned to c
   >>> args=[4,7]
   >>> c=list(range(*args)) # Same as above.
   ```
17. Conditions   

       Conditional statements in Python are are similar to that of ither languages.   
    ```python
    >>> var=12
    >>> if var==12:
    ...  print (12)
    ... else:
    ...  print(13)
    ... 
    12
    >>> user='c'
    >>> if user =='y':
    ...  print ("Yes")
    ... elif user=='n':
    ...  print("No")
    ... else:
    ...  print("Can't Say")
    ... 
    Can't Say
    >>> for i in [3,5,6,7]:
    ...     if i%2==0:
    ...           break ## comes out of the loop at the first even number
    ...     print(i)
    3
    5
    >>> for i in [3,4,6,7]:
    ...     if i%2==0:
    ...         continue ## move to the next iteration if even number is encountered.
    ...     print (i)
    3
    5
    7
    ```
18. Random Numbers

    ```python
    >>> import random
    >>> random.random() #generate a random number between 0-1
    0.7688075911155139
    >>> random.uniform(1,3) # generate a random number between the range 1-3
    1.3172662652831486
    >>> random.randint(1,3) #same as above but returns only an integer value 
    2
    >>> random.randrange(0, 10, 2) #generates only even numbers
    4
    >>> vowels=['a','e','i','o','u']
    >>>random.choice(vowles) # select randomly from a list
    e
    >>> for _ in range(5):
    ...  print(random.choice(foo))
    ... 
    c
    b
    b
    a
    c
    ```

19.  \*args and \*\*kwargs

    We can use \*args or \*\*kwargs when we are not sure of the number of arguments that will be passed to the functions. While \*args is used for variable non-keyword element, \*\*kwargs are used for varible length keyworded arguments.(i.e arguments of the key-value pair form.)
    ``` python
    >>> def f1(a,*args):
    ...  print ("formal argument=",a)
    ...  print ("Non key worded=",args)
    ... 
    >>> f1(1,2,3,4)
    formal argument= 1
    Non key woreded= (2, 3, 4)
    >>> def f2(*args,**kwargs)
    ...    print("Non Key worded=",args)
    ...    print("Varible length args with key-value=",kwargs)
    ...
    >>> f2(1,2,c=3,d='q')
    Non keyworded=(1,2)
    Variable length args with key-value={'c':3, 'd':'q'}
    >>># The order of agrguments is formal-variable agruments-keyword arguments
    ``` 

