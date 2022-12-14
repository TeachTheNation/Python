# Data Types

## Overview
Information comes in various shapes and forms. 

We can categorise the kinds of data we need to use in our code by classifying them into **data types**.

A **data type** is an attribute about data that tells computer how a programmer intends to use the data.

Data types define the operations that can be done on the data, the meaning of the data, and the way values of that type can be stored.

We have already seen a few data types in action: `str` and `int`.

### Numeric and Non-Numeric types
The difference between **numeric** and **non-numeric** data is that we can use numeric data in calculations and apply mathematical operators on them, as we’ve already seen in the Introduction section.

### ***Strings***
A **String** is declared by encasing any other text in a set of inverted commas (`''`) or speech marks (`""`).

In it's simplest form String is a block of text.

There are a number of things to keep in mind when using Strings in Python:

- It is known as a `str`
- `input()` function after reading users input gives the value as `str` data type
- We can **concatenate** Strings by using (`+`):
```python
sentence1 = 'hello my friends '
sentence2 = 'my name is Python'
print(sentence1 + sentence2)
```

- Within the print function, we can combine Strings with other data types by using (`,`):
```python
print("This sentence is split into",3,"parts.")
```

- We can write Strings over multiple lines by using (`\n`):
```python
print("My \n name \n is \n Python")
```

### ***Integers and Floats***
These are the two main **numeric data types** in Python. They are `float` and `int`.

The key difference between the two is that the former uses decimal points, while the latter does not.

### ***Booleans***
A **Boolean** is a data type that is usually treated as non-numeric. 

It can only hold one of two values: `true` or `false`. 

In Python, it is symbolised by the term `bool`.

Booleans are used for logical tests:

- Is a giraffe taller than a rhinoceros? The answer is `true`.
- Strawberrys colour is blue? `false`.

They are used in tandem with conditional statements which you will learn in later sections.

## Tutorial

Data types of variables are set when the variable is assigned a value:

***Note: The data type of a variable is not fixed. If a different value is assigned to the variable, the data type is updated as well.***

```Python
# Variable                    Data Type
#--------------------------------------------
stringVariable  = "Hello World"       # str
integerVariable = 19                  # int
floatVariable   = 19.4                # float
booleanVariable = True                # bool
```
***Note: Hash symbol(#) in Python is used when writing comments about the code. Python ignores any text after a # in a line.***

We can also set specific data types to variables like so:

```Python
stringVariable  = str("Hello World")
integerVariable = int(19)
floatVariable   = float(19.4)
booleanVariable = bool(True)
```
