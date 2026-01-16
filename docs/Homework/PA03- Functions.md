---
title: PA03 Functions
layout: default
parent: Homework
nav-order: 4
---

# PA03 Functions: Introduction to Python Functions

**Due by 11:00pm on Wednesday, February 18th, 2026** <br>    

## Objective
This assignment introduces students to writing functions in Python, including defining functions using the `def` keyword, declaring a function's parameters, returning values from functions, and calling functions within other functions. By the end of this assignment, students should be able to understand how to declare a function, how to use the function parameter(s), how to return a value from that function, and how to call that function, including from within other functions.

## TL;DR
1. Implement seven functions:
    - `is_even(given_value)`
    - `add_string_contents(given_str)`
    - `subtract_string_contents(given_str)`
    - `operate_on_string(given_str)`
    - `right_triangle_area(base, height)`
    - `trapezoid_area(first_base, second_base, height)`
    - `fahrenheit_to_kelvin(fahrenheit_temp)`
2. Use Python docstrings to comment each function thoroughly. Add any additional comments if you wish (within the code)
3. If you create your own variables, make sure they are given a proper name that makes sense in the context
4. Test your submission by doing the following in a file other than the one you submit:
   ```python
   import my_functions
   # test is_even with whatever number you like
   my_functions.is_even(number)
   # test with whatever you like, e.g. "123456"
   my_functions.add_string_contents(numeric_string)
   # ... # more tests, etc. for the other functions
   ```
5. Submit your file `my_functions.py` to Gradescope by 11:00pm on Wednesday, February 18th, 2026.

[instruction](/cs1112basit/instruction/PA03__Functions.pdf)
## Task
You're starting a new class off right when you notice, gee, it seems like I'm being asked to do a lot of busywork. It's almost like you could automate your homework problems instead of doing everything by hand! At this moment, you remember that you can use functions to do just that!

For this assignment, you'll need to implement seven functions in a file called `my_functions.py`. You must use Python docstrings to comment each function thoroughly. Please pay attention the function names, number and type of arguments (referred to herein as "argument format"), and what each function should return:

### `is_even(given_value)` (10 points)
This function should take any number as an argument called `given_value` which may be positive or negative. If `given_value` is even, return 0. If `given_value` is odd, return 1. (Hint: how do I check if a number is even or odd?).

This function should work for any (real) integer. You may assume that our tests will not try to call your function with a string or other nonsensical input, nor will our tests try to call your function with a float argument.

### `add_string_contents(given_str)` (10 points)
Given a string `given_str` that consists of numeric characters, add up each number character in the string and return a numeric total as the result.

Example usage:
```python
add_string_contents("123456") # should return the number 21
                             # (21 = 1 + 2 + 3 + 4 + 5 + 6)
add_string_contents("723")    # should return the number 12 = 7 + 2 + 3
add_string_contents("32091")  # should return the number 15
                             # (15 = 3 + 2 + 0 + 9 + 1)
  ```                         
You may assume that our tests will pass in strings that are not empty and that consist
of only numbers; you do not need to try and check for letters in the strings which can’t be
converted to numbers (that is, we will not test your code with a string like “123x7”). You
may also assume that we will not pass in a minus sign (“-”) as part of the string, so you do
not need to check for this either.
3

# 1.3 subtract_string_contents(given_str) (10 points)

Given a string `given_str` that consists of numeric characters, take the first character and subtract every following character in the string from it, returning a numeric difference as the result. 

Example usage:
```python
subtract_string_contents("123456") # should return a number -19 
                                  # (-19 = 1 - 2 - 3 - 4 - 5 - 6)
subtract_string_contents("723")    # should return 2 = 7 - 2 - 3
subtract_string_contents("32091")  # should return -9
                                  # (-9 = 3 - 2 - 0 - 9 - 1)
```
The same guidance and assumptions given for add_string_contents apply here: you do not need to check for letters in the string, nor do you need to check for minus signs ("-"). Strings we use to test your function will not be empty and, for this function, will be at least three (3) characters long.

# 1.4 operate_on_string(given_str) (20 points)

Given a string `given_str`:

- If the length of the string is even, then add up the contents of `given_str` and return that numeric result. You must use the `is_even` function you previously wrote to check this. (That is, call `is_even` inside this function.) 
- If the length of the string is odd, then take the first character of `given_str` and subtract all following characters from that first character, returning the numeric result. (Hint: you have functions to do all three of these tasks already – see the three previous functions! It should be a matter of choosing what to do based on input).

# 1.5 right_triangle_area(base, height) (10 points)

Given numeric arguments for `base` and `height`, return the numeric value for the area of a right triangle using the following formula:
```python
A = 1/2 * b * h, b = base, h = height

```
You do not need to check whether the arguments are numbers or not; we will only test with numeric arguments.  

# 1.6 trapezoid_area(first_base, second_base, height) (10 points)

Given numeric arguments for `first_base`, `second_base`, and `height`, return the numeric value for the area of a trapezoid using the following formula:
```python
A = ((b1 + b2) * h) / 2, b1 = first base, b2 = second base, h = height  

```

Like with `right_triangle_area`, you may assume that we will test only with numeric arguments, so you do not need to check your input.

# 1.7 fahrenheit_to_kelvin(fahrenheit_temp) (10 points)

Given a temperature argument in degrees Fahrenheit:

1. Convert from Fahrenheit to Celsius using the formula `C = 5/9 * (F - 32)`
2. Convert from Celsius to Kelvin using the formula `K = C + 273` 
3. Return the Kelvin temperature as a numeric value.

You may assume that we will only give you physically sensible arguments (you don't need to worry about your function returning a result below absolute zero, which wouldn't make sense). Be careful with the order of operations here, especially in the Fahrenheit-to-Celsius conversion!

# 1.8 Hints and Tips

As we have mentioned in class, strings in Python can be processed and operated on character-by-character (in technical terms, they are "iterable"). You can do this one of two ways:

- Use a `for` loop with the upper bound being `len(string)`:

```python
for i in range(0, len(string)):
   # access individual characters with string[i] 
   # then, operate accordingly