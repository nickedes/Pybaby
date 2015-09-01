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
    ```