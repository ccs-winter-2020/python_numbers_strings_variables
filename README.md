Let's start by taking a look at Python's simplest built-in data types:

* booleans: True or False
* integers: wholes numbers, e.g. 14 or 39
* floats: numbers with decimal points, e.g. 4.32 or 98.2
* strings: sequences of text characters, e.g. 'The dish ran away with the spoon.'

Each type has specific rules for its usage and is handled differently by the computer.

## Variables

Programming languages allows you to define variables, labels that refer to values stored in the computer's memory. In Python, you use `=` to assign a value.

The following is a two-line Python program that assigns the value of `'Adam'` to the variable name `student` and then prints the value currently associated with student:

## Variable Type

In Python, if you want to know the type of a thing - a variable or literal value - use `type(thing)`.

## Varible Names

Variable names may only contain these characters:

* Lowercase letters (a through z)
* Uppercase letters (A through Z)
* Digits (0 through 9)
* Underscore (_)

Names cannot begin with a digit. Also, variable names that begin with an underscore are treated in special ways. Names that begin and end with two underscores, `__` are reserved for use within Python, so do not use them when defining variable names.

## Reserved Words

Do not use any of the following for varaible names:
```
False         def           if            raise
None          del           import        return
True          elif          in            try
and           else          is            while
as            except        lambda        with
assert        finally       nonlocal      yield
break         for           not
class         from          or
continue      global        pass
```
## Numbers

Python has built-in support for `integers` (whole numbers) and `floats` (numbers with decimal points).

You can calculate combinations of numbers with math operators:
```
+     addition

-     subtraction

*     multiplation

/     floating point division

//    integer (truncating) division

%     modulus (remainder)

**    exponentation
```
## Python Exceptions

* Don't put a 0 in front of another digit
* Do not divide by zero eith eitehr kind of division

## Things to Know

* You can mix literal integers and variables
* The expression on the right side of the `=` is calculated first, then assigned to the varialbe on the left
* You can combine arithmetic operators with the assignment operator by putting the arithmetic operator before the `=`

```
>>> a = 4

>>> a += 2

>>> print(a)

6
```

* Use `divmod` when you want both the truncated quotient and remainder of a division expression.

```
>>> divmod(9,5)

(1,4)
```
## Mathematical Precedence

Precendence rules apply to mathmatic expressions in Python. For example, multiplication takes precendence over addition. In the following example, `3` is multiplied my `4` first, then the result is then subtracted from `8`:
```
8 - 3 * 4
```
When in doubt, you can wrap your code in parentheses:
```
8 - (3 * 4)
```
## Integer Type Conversion

To change other Python data types to an integer, use the `int()` function. This will keep the whole number and discard any fractional part.

* When booleans `True` and `False` are converted to integers, they represent `1` and `0` respectively
* Converting floating-point numbers to integers lops off everything following the decimal
* Text strings containing only digits can be converted to integers

* **If you try to convert something that doesn't look like a number, you'll get an excpetion.**

## Floats

Floating-point numbers (called floats) differ from integers in that they have decimal points.

## Float Type Conversion

To change other Python data types to a float, use the `float()` function.

* When booleans `True` and `False` are converted to integers, they represent `1.0` and `0.0` respectively
* Converting integers to floating-point numbers adds a decimal point
* Text strings containing characters that would be a valid float can be converted

## Strings

In Python a string is:

* Any sequence of characters
* Immutable - you can't change a string in place
* Enclosed in either single quotes, `''`, or double quotes, `""`

Having two kinds of quote characters allows you to create strings containing quote characters.

```
"'Hello, is anyone there?,' she asked as she walked through the door."
```

You can also use triple quotes, `'''`. Their most common use is for creating multiline strings.

## String Type Conversion

To change other Python data types to a string, use the `str()` function.

## Character Escaping

You can *escape* the meaning of some characters within strings in order to achieve certain effects by preceding a character with a backslash, `\`

* `\n` begins a new line
* `\t` adds a tab
* `'It\'s time to eat!'` specifies a literal quote inside the string

**If you need a literal `\`, type two of them, `\\`**

## String Concatenation

Python lets you combine literal strings or string variables with the `+` operator. You can also combine literal strings (not string variables) by having one after the other.

## String Duplication

You can duplicate a string using the `*` operator.

## String Extraction

To get a single character from a string, specify its offset in square brackerts. An offset is the number of positions a character is to the right from the start of the string.

**If you specify an offset that is the length of the string or longer, you'll get an exception.**

## Strings Are Immutable

Strings are *immutable* - you can't change them in place. The following code, for example, will give you an exception:
```
name = 'Sally'
name[0] = 'W'
```
Instead, you need to use some combination of string fuctions, such as `replace()` or `slice()`:

## Slice Method

You can extract a substring from a string using the `slice` method. You define a slice using square brackets, a *start* offset, and *end* offset, and an optional *step* size.

* If you do not specify a start, slice uses 0
    * `[:end]` specifies from the beginning to the end offset minus 1
* If you do not specify an end, slice uses the end of the string
    * `[start:]` specifies from the start offset to the end
* If you do not specify a start and stop, slice will return the entire sequence
    * `[:]` extracts the entire string sequence from start to end
* The step size indicates how many characters to skip
    * `[start:end:step]` extracts from the start to the end minus1, skipping characters by the step
* A positive step goes from left to right
* A negative step goes from right to left

## Length Method

You can use `len()` to return the length of certain data types. When you pass `len()` a string, it returns the number of characters in the string.
```
>>>len('Happy')

5
```
## Split Method

You can split a string into a list of smaller strings using the built-in string `split()` function.

## Join Method

The `join()` method is the opposite of `split()`. It collapses a list of strings into a single string.

## More string methods

(String Methods)[https://docs.python.org/3/library/stdtypes.html#string-methods]
