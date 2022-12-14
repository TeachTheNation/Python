# Introduction

## Overview

In this module, we will look at why we need computers as well as give an introduction to variables.

## Why do we need computers?

Most of us use computers as part of our everyday lives, either for work or for personal use, but why do we use them?

Most people think that computers will solve all our problems, however, computers do not solve the problems, we do.

**"The computer isn't stupid, it will do exactly what you tell it to. The computer is as stupid as you are."**

In Teach The Nation To Code, you will hear the phrase **a computer is a stupid machine** many times.
This is because computers will only ever do exactly what they are told to do, they cannot do any more than that by themselves.

So then, why do we need computers?
The answer is for two reasons: speed and accuracy.
These two reasons are what makes computers incredibly useful in helping to solve problems.

### Speed

If you were asked to calculate 
> 378 x 183 = ?

It would take a while to work out, for even the quickest Mathematician this might take 10-20 seconds, a computer will do it in a couple of milliseconds.

Now let's take this to another level, if you were asked to calculate
> 378472398472 x 2473984729183 = ?

This would take you a good few minutes if not more. Computer will once again calculate this in milliseconds.

### Accuracy

If a group of 100 people were asked to calculate
> 53686293 x 738972939081 = ?

Even with as much time as you need, the chances are we would still get some different answers, whereas 100 computers would all give the same answer.

## Why do we need variables?

Let's say we have some complicated information which we need to use over and over again.
For example, a long number such as the value of Pi

`3.14159265358979323846`

Instead of writing this out multiple times within a program, we can instead store it in an easily accessible location (computer memory). This is where variables come in, to make some value re-usable. This saves user effort of writing it over and over again.

A variable is a callable keyword which references a place in the computers memory where the information is stored.
We do not know where in the memory this information is stored, and we don't need to, since the address is attached to the variable (invisible to us).

```python
pi = 3.14159265358979323846
print(pi)
print(pi)
print(pi)
print(pi)
```
First line declares a variable ***pi*** which gets assigned a value of ***3.14159265358979323846***.
In the next four lines, we ask Python to print to the terminal the value of the variable `pi`, now which is easier writing out the whole value of **Pi** to be printed four times, or ask computer to print the value that is assigned to the variable ***pi***. The answer seems obvious doesn't it?

## Working with variables

### Assignment

We store a value in a variable using the **assignment operator** (`=`).

The **value** on the right hand side, is stored in the computers memory location referenced by the **variable name** on the left hand side.

```python
pi = 3.14159265358979323846
```

### Reassignment

So far, you have not really seen why a variable is called a variable.
This is due to the ability of a variable to change the value it was initially assigned, to a new one. 

Let's say that you have a variable but you want to change its value, you can do that, the process is exactly the same, using the **assignment operator**.

```python
a = 10
b = 20
a = 40
print(a)
```

This would print to your terminal the value of **a** as `40`. On line one the variable `a` has been assigned a value of `10`. In the next line variable `b` has been assigned the value of `20`. But now pay attention to the third line where variable **a** is again getting a value assigned, this time `40`, and what this means is that the initial value of `10` is now lost forever and the new value of `40` takes its place. Finally the result is printed as `40`.

### Expressions

Another part of Python's functionality is the ability to do Mathematical calculations using variables.
To do this we use the **mathematical operators**.

| Operator | Name |
| ---| --- |
| + | Addition |
| - | Subtraction |
| * | Multiplication |
| / | Division |

These are the standard operators but there are many more.

Let's see some examples:

```python
a = 10
b = 20
c = 50 + 50
d = a + b
print(d)
```

First line creates a variable `a` and assigns it a value of `10`. Second line creates another variable called `b` and assigns it the value of `20`.

On the third line, Python will do the calculation `50 + 50` and then store the result `100` in another variable called `c`.

Fourth line calculates right hand side of the assignment operator `=`, by taking the value assigned to variable `a` where the value assigned is `10` and `b` with the value assigned as `20`, adds them together and stores the new value of `30` under a variable `d`.

Finally the value assigned to variable `d` is printed.

### Execution

It is important to understand what Python does with the code you write.

In a simplified way, like most programming languages, Python starts at the top of the file and works it's way down one line at a time until it reaches the last line and then stops.

What would be printed to your terminal based on the example below?

```python
a = 10
b = 20
c = a + b
a = 40
print(c)
```

Well, let's go through it as Python would.
1. First, we assign the value of `10` to the variable `a`.
2. Next, we assign the value of `20` to the variable `b`.
3. Then, we find the value of `a` (`10`), the value of `b` (`20`) and add them together (`30`) and store it in the variable `c`.
4. Then, we reassign the value of `a` to be `40`.
5. Finally, we find the value of `c` (`30`) and print it to the terminal.

So, the final line prints `30` to the terminal. Surprised why it's not `60`? This is due to the previously mentioned rule of Python going top to bottom, one line at a time. When the value was being calculated for variable `c`, the value of `a` was `10` and only when the result was calculated and assigned to `c` did the value of `a` change to the new value of `40`. This is why the final print was `30`.

### Specificity

The programs we've written so far are good, but they're not very re-usable.

Let's make a very simple program for calculating the combined score for all your science exams.
We will store the value of our **biology**, **chemistry** and **physics** marks in variables, then add them all together and store the total in a variable.

```python
a = 60
b = 70
c = 80
d = a + b + c
```

Although this will function exactly as we want, if we look back at it in a few weeks time, we will have no idea what `a`, `b`, `c` & `d` represent.

This is why we should always give our variables **meaningful names**!

Let's rewrite the previous program.

```python
biology = 60
chemistry = 70
physics = 80
total = biology + chemistry + physics
```

This is much easier for us to understand than the previous program.

## Inputs

So far, the assumption was that the person writing the program is the one who will be using it; this is not always the case.

Let's look at the exam calculator from before.

If someone, who is not the person who wrote the program, wanted to use it, they wouldn't be able to put their own values in. Would they then have to write a new application every time they wanted to use it? Hopefully at this point you're thinking that this sound like a bad solution.
This situation happened because the values in the program are **hard-coded**. 

***Hard-coded*** means that the values are set in stone and will not change no matter how many times you will run this application. 

To make the program usable by anyone, we will use the **input()** function to allow the user to enter their own marks.

```python
biology = input()
chemistry = input()
physics = input()
total = biology + chemistry + physics
```

Every time Python gets to the input() function, it will wait for the user to enter a value and hit return, if return is not pressed Python will continue to wait for it indefinately and nothing else will happen until return press action takes place.
Input function allows the person writing the program to pass a meaningful message about what is expected of the user. To pass some text when awaiting user input you will need to enter the text between the opening and closing parentheses of the input() function, and ensure that the text is surrounded with qoutation marks.

So our final program would look like this:

```python
biology = input("Please enter your Biology marks: ")
chemistry = input("Please enter your Chemistry marks: ")
physics = input("Please enter your Physics marks: ")
total = biology + chemistry + physics
```

## Recap

* Computers are used for the sake of speed and acuracy.

* Variable points to the location in our computer's memory where the value is stored, you gain access to the value stored by using the variables name under which the value is stored. The value stored by the variable can change.

* You should always use meaningful names for variables

* If you want to get input from the user use the `input("Example text to be displayed")` function

## Tutorial

In this tutorial, we will create a program which will take in English, Maths, and Science scores and then calculates their average score.

1. First, we need to store the scores inside variables to use later on.
```python
english = 50
maths = 60
science = 70
```
2. Now, we need to calculate the average. 
To do this, we need the **total marks** which we can store in a variable, and then we will divide the total by 3 in order to get the average.
We will store the final result in another variable.
```python
total = english + maths + science
average = total / 3
```
3. Lastly, we will print the average to the terminal with a nice message.
```python
print("Your average score is :")
print(average)
```
4. The final program will look like this:
```python
english = 50
maths = 60
science = 70
total = english + maths + science
average = total / 3
print("Your average score is :")
print(average)
```

## Exercises

Try to improve the program we created to allow the user to enter their own scores.

<details><summary>Hint</summary>

Take a look at the **Data Types** module for more information.

</details>
