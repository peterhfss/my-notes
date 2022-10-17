# Indentation , Identifiers , Statements, Expressions and Comments

Python has concepts that are similar to other languages to script and that are also strongly typed.

These two modes can execute programs in Python :

## Programmation in interactive mode

In the terminal, we can write the command python that when executed will show the interpreter of Python.

One time the interpreter Python was started, we can write code python and execute it to show the result in the terminal.

## Programmation in script mode

This mode is different because when we wish to execute a file containing code python, we should inform as a parameter name of the file, and in the end, your extension is .py, after the command python in the terminal.

## Identifiers

In Python, the identifiers are used to identify a variable, function, class, module, or other objects. To declare an identifier, it should begin with a letter A-Z or a-z, or an underline(_), and then by many letters, underline, and numbers(0 - 9). Python is case-sensitive, in this case, the identifiers Age and age are not the same.

> Not allowed the use these character in identifiers : @ , $, and %.

There are conventions of nomenclatures for identifiers in Python:

* For names of classes, should begin with an upper letter, and the other identifiers begin with a lower letter;

* To identify that an identifier is private, should begin with a single underline to the left;

* To identify that an identifier is  strongly private, should begin with two underlines to the left;

* To identify that an identifier will be a name special defined, should containing with two underlines to the left and to right too.

## Statements

The statements in Python finish with a new line, however using the character (\), the statement should continue in another line :

```python
# Using  character ( \ )
media = value1 + \
        value2 + \
        value3 
```
Different from other languages, Python doesn't use the (;) in the final of statements, but when writing multiple statements in a single line, we need to use it this way : 

```python
# Using  character ( ; )
import sys; x = 'foo'; sys.stdout.write(x + '\n')
```

## Expressions

Expressions are codes that combine values, variables, operators, and functions to produce a result.

```python
x = 5 + 5
print(x) # 10
```

## Reserved words

Also following other languages, Python has words reserved, and don't are allowed to use them in variables, constants, or any other identifiers.

<div style="display: flex;justify-content: center;">

|        |          |         |          |        |
| :---:  |   :---:  |  :---:  |  :---:   | :---:  |
|  False |   await  |   else  |  import  |  pass  |
|  None  |   break  |  except |    in    |  raise |
|  True  |   class  | finally |    is    | return |
|   and  | continue |   for   |  lambda  |   try  |
|   as   |    def   |   from  | nonlocal |  while |
| assert |    del   |  global |    not   |  with  |
|  async |   elif   |    if   |    or    |  yield |


</div>

## Comments

To add comments in Python, use character hash(#) :

```python

# This is a comment in Python

```

Also, we can write comments on multiples lines : 

```python
"""

This is a multiline
comment

"""

```

