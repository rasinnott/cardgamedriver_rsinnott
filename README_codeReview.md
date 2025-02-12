# ***__Code Review__***- cardgamedriver

Forked from <https://github.com/rwhitnell/cardgamedriver>


# __Objectives__

This section summarizes the findings and conclusions drawn from the full review that follows.

## - Is as bug-free as possible:

\-body here-

## - Clarifies its purpose so you and others can understand it in the future

\-body here-

## - Can be maintained without simply starting over

\-body here-

# __Review Guidlines__

## - Documentation

- [ ] body

## - Code structure

- [ ] body

## - Variables

- [ ] body

## - Arithmetic operations

- [ ] body

## - Loops and conditional statements

- [ ] body

## - General programming practice

- [ ] body

## - Other code review items

- [ ] body

# __Reviewing implementation of a specification and class definitions__


## - Run the program and compare the output to what’s described about the driver program in the specifications.

body

## - Look through each class in the code to see what it does and how that implements the specifications.

body

## - Identify all code review items from the list above that may be relevant to this project. Add the list of relevant items to your codereview.md file.

body


## - For each code review item you’ve identified, add text to your codereview.md file that does the following.

- [ ] Evaluates whether the project appears to satisfy the item under review. For example, if there are loops in any of the methods, is the index initialization done correctly?
  - [ ] Include sample output to whatever extent it helps support your conclusions.


- [ ] For any unsatisfactory items, recommends changes that would bring the code into compliance and why you expect those changes to work.


- [ ] You can describe these changes completely in the codereview.md file, or you can modify the existing code. If you modify code, do the following:
  - [ ] Comment out the original code instead of deleting it.
  - [ ] Add comments to the code that describe the changes you’ve made.
  - [ ] Add a note to the codereview.md pointing to the code you’ve changed.


## - Tracking down a bug and proposing a fix.

- [ ] -- Run the code so that it generates the error several times. In each case, look at the information printed out with the exception, particularly which lines of code it’s pointing to. Is it always the same line or same region of the program? If so, that will give you some clues about where to start looking.
- [ ] -- What is the specific error that occurs, based on what the exception tells you? How could the lines that the exception points to cause that error? For example, if the error was dividing by zero (which it’s not in this case), how could the variables in the lines of code you’re looking at end up resulting in divide by zero?
- [ ] -- What conditions could arise that cause that error? How could the illegal argument that’s causing the error be generated occasionally as the program runs, causing it to crash?
- [ ] -- How would you propose fixing the program? That might be because there is a clear logical error in the program code that led to this problem. It may also be because the specifications need to be updated to account for this issue, and then the code needs to be changed.


## Once you’ve worked through the process of identifying the problem and considering solutions, do the following.

- [ ] -- In your codereview.md file, describe why the error occurs. In doing so, be sure to describe why it only occurs occasionally and, most of the time, the program runs without error.
- [ ] -- Describe your proposed fix to address the error. If necessary, describe what you would change in the project specifications.
- [ ] -- Implement your change in the code. Be sure to add a comment at any point where you change code from the original version.


### **Challenge**s

- [ ] -- I’m about 99.9% certain that this program creates garbage in the Java sense: objects that no longer have a variable referencing them at some point as the code runs. (This situation is also known as a *memory leak*.) While Java garbage collection will address these objects, it’s still better if it doesn’t happen in the first place. I think I know where one memory leak occurs, but there might be more. Identify one or more memory leaks, provide an analysis of the code that shows how the leak occurs, and propose and/or implement modifications to fix the leak.
- [ ] -- As I was doing my final testing of the code in preparing this assignment, the program threw an exception in the `Blackjack` class that had never occurred before. See if you can recreate that exception and then address using the same set of steps as above. This particular exception was an `IndexOutOfBoundsException`. And, of course, you might find others, and you can choose to address those as well.


