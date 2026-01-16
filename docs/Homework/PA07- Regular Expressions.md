---
title: PA07 Regular Expressions
layout: default
parent: Homework
nav-order: 8
---

# PA07: Regular Expressions (RegEx)

**Due by: 11:00pm on Wednesday, April 15th, 2026**

## Objective: 
The objective of this assignment for students is to learn how to work with regular expressions for a practical application. By the end of the assignment, students should be able to:

- Write regular expressions to match specific strings
- Analyze regular expressions and understand what the regular expression can match

Regular expressions, often also known as regex, is a powerful tool used to define search patterns. They provide a flexible and concise way to match, search, and manipulate text based on specific rules and patterns. Regular expressions utilize special syntax to define set of rules for matching patterns, making them a fundamental tool for text processing and manipulation.

In the following assignment there will be three distinct sections in the following order:

- Section 1: Write the regular expression that will match the strings described. Write down any assumptions you are making along with the regular expression.
- Section 2: Given regular expressions (regex), provide three (3) different example strings that will be matched (completely) by that regular expression. (Note: the entire string should be matched by the regular expression, and not just a part of it)
- Section 3: Given regular expressions (regex), which of the provided strings will be matched (completely) by that regular expression. (Note: the entire string should be matched by the regular expression, and not just a part of it) Select all that apply.

## 1 Section 1.

Write the regular expression that will match the strings described below. Write down any assumptions you are making along with the regular expression.

### 1.1 Question 1

Match all strings that are exactly 7 characters long and the 2nd character is a digit. Assume all other acceptable characters are word characters.

```python
q1 = re.search("REPLACE THIS WITH YOUR REGULAR EXPRESSION", txt)
```

Strings it should MATCH:
a = "a2c6M_x"
b = "1234567"
c = "A5BCDEF"
d = "_1___8_"

Strings it should NOT MATCH:
a = "b7!qQr5"
b = "abcdefg"
c = "a2c6N_x1"
d = "S3a2b4_nm"

### 1.2 Question 2

Match all numeric strings where the 3rd number in the string is even and the last number in the string is 1 or 5. There is no restriction on the length of the string. All characters in this string are digits. Assume 0 (zero) is an even number.

```python
q2 = re.search("REPLACE THIS WITH YOUR REGULAR EXPRESSION", txt)
```

Strings it should MATCH:
a = "7148765"
b = "1123333355553331"
c = "7761"
d = "7785"

Strings it should NOT MATCH:
a = "7228262"
b = "7238265"
c = "7238261"
d = "21"

### 1.3 Question 3

Match all strings that have the lower-case letters "u", "v", and "a" in the string in this ORDER. There can be other u's and v's and a's in the string, but at least there should be at least one "u" followed by a "v" followed by an "a". These three letters should not necessarily be consecutive, although they could be. There can be any number of characters between them, or none at all. As an example it should match the string "uva" as well as the string "xxuy82yvzzuzza3333v". Assume all other acceptable characters are upper- and lower-case letters as well as numerical digits (0 through 9).

```python
q3 = re.search("REPLACE THIS WITH YOUR REGULAR EXPRESSION", txt)
```

Strings it should MATCH:
a = "uva"
b = "1u2v3a4"
c = "A5uBCDvaEF"
d = "1234uva"

Strings it should NOT MATCH:
a = "UVA"
b = "1U2V3A4"
c = " uva "
d = "u_v_a888"

### 1.4 Question 4

Match all strings that end in "Go Hoos!" The string could have any number of characters before this, or none. Assume all other acceptable characters are upper- and lower-case letters, numerical digits (0 through 9), the underscore ("_") and the space character.

```python
q4 = re.search("REPLACE THIS WITH YOUR REGULAR EXPRESSION", txt)
```

Strings it should MATCH:
a = "To celebrate we yelled Go Hoos!"
b = "Go Hoos!"
c = "aa44_Go Hoos!"
d = "___Go Hoos!"

Strings it should NOT MATCH:
a = "go hoos!"
b = "go hoos"
c = "Go Hoos! "
d = "bbb Go Hoos! rrr"

### 1.5 Question 5

Match all strings where the first character is not a whitespace character, and the substring "fun" appears anywhere in the string (after the first character). For example, it should match the string "Python is a fun programming language". Assume all other acceptable characters are upper- and lower-case letters, numerical digits (0 through 9), the underscore ("_") and the space character.

```python
q5 = re.search("REPLACE THIS WITH YOUR REGULAR EXPRESSION", txt)
```

Strings it should MATCH:
a = "We like to have fun on the weekends"
b = "qqqfunny123"
c = "fun"
d = "fun FUN fun"

Strings it should NOT MATCH:
a = " hoos Are fun"
b = " Go Hoos!"
c = "Go hoos!"
d = "fun#"

## 2 Section 2.

Given the following regular expressions (regex), provide three (3) different example strings that will be matched (completely) by that regular expression. (Note: the entire string should be matched by the regular expression, and not just a part of it.)

For each question in this section, replace the strings with your answers in the python file:

```python
return ["FIRST_STRING", "SECOND_STRING", "THIRD_STRING"]
```

### 2.1 Question 1

Analyze the following regular expression (regex). Once you have decided what kind of strings it would match, provide three (3) different example strings that will be matched (completely) by this regular expression.

Regular expression: `"^(ab)?[A-Z]{3}[5-9]"`

### 2.2 Question 2

Analyze the following regular expression (regex). Once you have decided what kind of strings it would match, provide three (3) different example strings that will be matched (completely) by this regular expression.

Regular expression: `"\([24789]{2,4}\):(eagle|falcon|kestrel)\sArea:\s[1-9]"`

### 2.3 Question 3

Analyze the following regular expression (regex). Once you have decided what kind of strings it would match, provide three (3) different example strings that will be matched (completely) by this regular expression.

Regular expression: `"^Virginia!?\swa\shoo\swa+"`

### 2.4 Question 4

Analyze the following regular expression (regex). Once you have decided what kind of strings it would match, provide three (3) different example strings that will be matched (completely) by this regular expression.

Regular expression: `"[a-z]*PY[a-z]*[^es]$"`

## 3 Section 3.

Given the following regular expressions (regex), which of the provided strings will be matched (completely) by that regular expression. (Note: the entire string should be matched by the regular expression, and not just a part of it.) Select all that apply.

For each question in this section, place the letter(s) in a list that correspond to the strings that you believe will be completely matched by the regular expression. At the end of each function, return that list of strings (don't forget the quotations around the characters!). For example:

```python
return = ["x", "y"]
```

### 3.1 Question 1

Analyze the following regular expression (regex). Which of the following strings will be completely matched by the regular expression? Select all that apply.

Regular expression: `"\[\([0-9]{1-2},[0-9]{1-2}\),\s\([0-9]{1-2},[0-9]{1-2}\)\]"`

a = "[(1,4),(66,77)]"
b = "[(2,3), (4,7)]"
c = "(7,1), (1,7)"
d = "[(36,0), (5,29)]"

### 3.2 Question 2

Analyze the following regular expression (regex). Which of the following strings will be completely matched by the regular expression? Select all that apply.

Regular expression: `"1[0-2]/\d?\d/2023|0?[1-9]/\d?\d/2024"`

a = "9/1/2023"
b = "11/1/2023"
c = "9/1/20248"
d = "10/3/2025"

### 3.3 Question 3

Analyze the following regular expression (regex). Which of the following strings will be completely matched by the regular expression? Select all that apply.

Regular expression: `"\+44\s\(0\)\d{2}\s\d{4}\s\d{4}"`

a = "+44 (0)20 1234 5678"
b = "+44 (0)21 1232 5678"
c = "+44 (1)21 1232 5678"
d = "+44 (1)211232 5678"

### 3.4 Question 4

Analyze the following regular expression (regex). Which of the following strings will be completely matched by the regular expression? Select all that apply.

Regular expression: `"\["[^"]+",\s"[^"]+"\]"`

a = "["Apple", Bananas]"
b = "['apple', 'Bannanas']"
c = "["APple", "Bandanas"]"
d = "add string"

## 4 Additional Information

Keep the following in mind as you write your code, as you will be graded on these aspects:

- Don't forget your header at the top of your `.py` file (see section 5.1)
- Cite your resources clearly or state you did not use any
- Use appropriate variables names throughout your program
- Include comments throughout your code to explain what you are doing (see example below:)

```python
exp = re.search("[a-z]*", txt) # This matches 0 or more lowercase letters
```

Still having some issues submitting? Please keep the following in mind:

- Ensure your ONLY edited what we asked you to edit in the Python file
- Ensure you did not add any additional code to the Python file
- Ensure you remove any print-statements before you submit (you can add them while testing, but remove them before submitting!)
- Don't forget to:

```python
import re
```

## 5 Submission and Collaboration Policy

### 5.1 Your Submission–Comment Header

Your `.py` file should contain the following information (header) at the top of your file:

```
# NAME: e.g. I. Lv. Sneks
# COMPUTING ID: e.g. ils3py@virginia.edu
# PA NUMBER and NAME: e.g. PA## - Name of the Assignment
# Resources used (if applicable):
```

For Resources, include URLs to any online resources where you studied or reviewed code that is specific to these problems, including any physical textbooks you referenced. Include any other resources you used here. Note on resources: Please feel free to refer to the lecture slides, demos, and in-class labs to complete this assignment (all located on Canvas).

Absolutely no collaboration with any fellow students (who are not current CS 1112 course TAs) is allowed. Your work must represent individual effort. You must write your own code: not just type it, but also compose it yourself as your own original work.

You must cite any and every source you consult, other than those explicitly provided by the course itself. If you work with, obtain or receive help from another source (Internet website, textbook, TA, tutor, online video, etc.), nothing should be copied or retyped into the submitted solution. References must be documented in a comment in the code on the assignment. Any copied work is an Honor Code violation.

### 5.2 Gradescope

You must match our file name, `regex.py`, exactly.
If you do not match our filename exactly, our autograder will be unlikely to find it, and it will therefore be unable to generate useful feedback to aid you on your submission.
ONLY make edits to the file as described!

#### 5.2.1 Submitting on Gradescope

1. Go to Gradescope (linked in Canvas course website)
2. Click on PA07 – Regular Expressions in the assignment list on Gradescope
3. Upload your Python program as `regex.py`.

Note: If you face any difficulties or have questions, please reach out to the instructor or teaching assistants for assistance.