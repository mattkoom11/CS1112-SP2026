---
title: PA02 Monsters and Aliens
layout: default
parent: Homework
nav-order: 3
---

# PA02: Monsters and Aliens

**Due by 11:00pm on Wednesday, February 11th, 2026** <br>    

## Objective
The objective of this assignment is to introduce students to the concept of conditional statements in Python while exploring a fun monsters and aliens theme. By the end of this assignment, students should be able to understand and implement if, else, and elif statements to make decisions based on different scenarios.

[instruction](../../instruction/PA02__Monsters_and_Aliens.pdf)
## Task

Note. This assignment can be completed in two different ways, when conditional statements are referred to in the write-up, they can either be, (i) if-elif-else statements, or (ii) match-case statements, depending on your choice of implementation.

You must match our file name, `monsters_and_aliens.py`, exactly.
If you do not match our filename exactly, our autograder will be unlikely to find it, and it will therefore be unable to generate useful feedback to aid you on your submission.

### Instructions

1. Imagine a world filled with monsters and aliens! Your task is to write a Python program that interacts with users and determines the appropriate response based on the characteristics of the creatures they encounter.

2. Write a Python program called `monsters_and_aliens.py` that prompts the user to enter the name of a creature and stores it in a variable called "creature_name"

3. Using conditional statements, write code that performs the following tasks:
    - If the `creature_name` is "monster", print the message "Watch out! Monsters are strong and dangerous."
    - Else if the `creature_name` is "alien", print the message "Be cautious! Aliens are intelligent and mysterious."
    - Else if the `creature_name` is "unknown", print the message "Unknown creature. Approach with caution!"
    - (Else) If the input is not "monster", "alien" or "unknown", print the message "Not a valid type. The three types are monster, alien, and unknown."

4. Test your program with different creature names ("monster", "alien", "unknown", or something else) to verify that it produces the correct output for each scenario.

5. Extend your program to include additional characteristics for a monster and an alien. That is, add to the bodies of the previous if-elif-elif-else statements. (Hint: Remember you can have nested if-statements! Don't forget the proper indentation!):
    - If the `creature_name` is "monster" (and after printing the appropriate message from step 3), prompt the user to enter the size of the monster (small, medium, or large), and print a corresponding (and different) message for each based on its size. The monster size should be stored in a variable called "monster_size".
        - If the "monster_size" input is anything other than "small", "medium", or "large", print your own message conveying how scary the monster still is.
    - If the `creature_name` is "alien" (and after printing the appropriate message from step 3), prompt the user to enter the number of eyes the alien has (0, 1, or 2) and print a corresponding (and different) message for each of the 3 values. The number of eyes should be stored in a variable called "eyes".
        - If the "eyes" input is anything other than 0, 1, or 2, print your own fun fact about aliens.

6. Test your program with various scenarios, including different creature names, sizes, and number of eyes, to ensure it behaves as expected.

Keep the following in mind as you write your code, as you will be graded on these aspects:

- Don't forget your header at the top of your .py file (see section 2.1)
- Cite your resources clearly or state you did not use any
- Use appropriate variables names throughout your program
- To ensure the autograder can grade your submission, be sure to match the provided print statements EXACTLY, including spacing and punctuation! When asked to come up with your own print statements (like in step 5), you may print any appropriate message.
- Include comments throughout your code to explain what you are doing (see the example in-line comments below:)

```python
food = "apple" # This is a string that represents apple
if food == "pear": # if the food item is a pear
   # if food is a pear, output that pears are not apples
   print("Pears are delicious, but they're not apples!")
elif food == "apple": # if the food item is an apple
   # if food is an apple, output that apples are my favorite snack
   print("Found the apple! Apples are my favorite snack!")
   # ...
```
For Resources, include URLs to any online resources where you studied or reviewed code that is specific to these problems, including any physical textbooks you referenced. Include any other resources you used here. Note on resources: Please feel free to refer to the lecture slides, demos, and in-class labs to complete this assignment (all located on Canvas).

Absolutely <b>no collaboration with any fellow students (who are not current CS 1112 course TAs) is allowed.</b> Your work must represent individual effort. You must write your own code: not just type it, but also compose it yourself as your own original work.

You must cite any and every source you consult, other than those explicitly provided by the course itself. If you work with, obtain or receive help from another source (Internet website, textbook, TA, tutor, online video, etc.), nothing should be copied or retyped into the submitted solution. References must be documented in a comment in the code on the assignment. Any copied work is an Honor Code violation.

### Gradescope

#### Submitting on Gradescope

1. Go to Gradescope (linked in Canvas course website)
2. Click on PA01 – Turtle Drawing in the assignment list on Gradescope
3. Upload your Python program as `my_turtle.py`.
4. Click Browse Files to upload a screenshot of your drawing that was produced by using the turtle library
5. Click the upload button at the bottom right corner to submit both files!
6. Remember to include your name, computing ID, and resources in your comments!! (See section 3.1 of this document.

You should submit your code to Gradescope. If you are having trouble with your submission, you should double check the following common problems:

1. Make sure you are only submitting two (2) files, a screenshot of the drawing and file called `my_turtle.py` *exactly*

*This assignment will be graded by hand, and therefore will not have a Gradescope autograder. That is, you will not see a score as soon as you submit.*

Note: If you face any difficulties or have questions, please reach out to the instructor or teaching assistants for assistance.