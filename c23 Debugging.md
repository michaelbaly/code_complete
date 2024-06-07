Debugging is the process of identifying the root cause of an error and correcting it.

### 23.1 Overview of debugging issues

#### 1. role of debugging in software quality
* it's a way to diagnose defects
#### 2. variations in debugging performance
![alt text](image-14.png)

#### 3. defects as opportunities - you can:
* learn about the program you're working on
* .. the kinds of mistakes you make
* .. the quality of your code from the point of view of somehone who has to read it
* .. how you solve problems
* .. how you fix defects

#### 4. an ineffective approach
The devil's guide to debugging - common approaches:
* find the defect by guessing
* don't waste time trying to understand the problem - find is enough
* fix the error with the most obvious fix

Debugging by superstition
* `KP:`Even if an error at first appears not to be your fault, it’s strongly in your interest to
assume that it is

### 23.2 Find a defect

#### The scientific method of debugging
1. stabilize the error
2. locate the source of the error
    * a. gather the data that produces the defect
    * b. analyze the data that has been gathered, and form a hypothesis about the defect
    * c. determine how to prove or disprove the hypothesis, either by testing the program or by examining the code
    * d. prove or disprove the hypothesis by using the prodedure identified in 2.c
3. fix the defect
4. test the fix
5. look for similar errors

#### Tips for find defects
* use all the data available to make your hypothesis 
* refine the test cases that produce the error
* exercise the code in your unit test suite
* use available tools
* reproduce the error several different ways
    ![alt text](image-15.png)
* generate more data to generate more hypothesis
* use the results of negative tests
* brainstorm for possible hypotheses
* keep a notepad by your desk, and make a list of things to try
* narrow the suspicious region of the code
* be suspicious of classes and routines that have had defects before
* check code that's changed recently
* expand the suspicious region of the code
* integrate incrementally
* check for common defects
* talk to someone else about the problem
* take a break from the problem

Brute-Force Debugging

#### Syntax errors
* Don't trust line numbers in compiler message
* Don't trust compiler messages
* don't trust compiler's second message
* divide and conquer
* find misplaced comments and quotation marks

### 23.3 Fixing a defect
* `KP:` understand the problem before you fix it
* understand the program, not just the problem - global not local
* confirm the defect diagnosis
* relax - relax long enough to make sure your solution is right
* save the original source code
* fix the problem, not the symptom
* change the code only for good reason
* make one change at a time
* check your fix
* add a unit test that exposes the defect
* look for similar defects

### 23.4 Psychological considerations in debugging

#### How `psychological set` contributes to debugging blindness 
* `psychological set` - seeing what you expect to see
```
First, it speaks to the importance of good programming practices
Second, select parts of the program to examine when an error is found
```
#### How `psychological distance` can help
* Def. - as th ease with which two items can be differentiated.

### 23.5 Debugging tools - obvious and not-so-obvious

#### Source-code comparators
#### Compiler warning message
KP: one of the simplest and most effective debugging tools is your own compiler.
* set your compiler's warning level to the highest, pickiest level possible, and fix the errors it reports
* treat warnings as errors
* initiate projectwide standard for compile-time settings

#### Extended syntax and logic checking

#### Execution profilers
* examine the output of an executio profiler to satisfy yourself that your program spends a reasonable amount of time in each area

#### Test framework/scaffolding

#### Debuggers
* `KP:` the most effective combination is good thinking and a good debugger

---
checklist
