## what performance is and how important it is 

### 25.1 Performance overview

#### Quality characteristics and performance
* `Users are more interested in tangible program characteristics than they are in code quality`
* `KP:` performance is only loosely related to code speed. to the extent that you work on your code's speed, you're not working on other quality characteristics. Be wary of sacrificing other characteristics to make your code faster. Your work on speed might hurt overall performance rather than help it.

#### Performance and code tunning
* Think about efficiency from each of these viewpoints:
    + program requirmens
    + program design
    + class and routine design
    + operating-system interactions
    + code compilation
    + hardware
    + code tunning

* program requiremnts - follow strictly by requirement other than performance
* program design - if you know a program's size and speed are important, design the program's architecture so that you can reasonably meet your size and speed goals.
    + Setting individual resource goals makes the system's ultimate performance predictable.
    + the mere act of making goals explicit improves the likehood that they'll be achieved.
    + `KP:` you can set goals that don't achieve efficiency directly but promote efficiency in the long run
* class and routine design - key point at this level is `choice of data types and algorithms`.
* OS interactions
* code compilation - good compilers turn clear, high-level language code into optimized machine code.
* hardware
* code tunning - in ways that make it run more efficiently.

### 25.2 Introduction to code tunning

#### The pareto principle - `80/20 rules`
* 20 percent of a program's routines consume 80 percent of its execution time
* old wives' tales - common misapprehensions:
    + reducing the lines of code in a high-level language improves the speed or size of the resulting machine code - `false`
    + certain operations are probably faster or smaller than others - `false`, there's no room for "probably" when you're talking about performance.
    + you should optimize as you go - `false`, main problems:
        * it's almost impossible to identify performance bottlenecks before a program is working completely.
        * in the rare cases in which developers identify the bottlenecks correctly, they overkill the bottlenecks they've identified and `allow others to become critical`.
        * focusing on optimization during initial development detracts from achieving other program objectives; if you need to optimize before a program is complete, `minimize the risks` by building perspective into your process
    + a fast program is just as important as a correct one - `false`

#### When to tune
* use a high-quality design. make the program right. make it modular and easily modifiable so that it's easy to work on later. when it's complete and correct, check the performance. if the program lumbers, make it fast and small. don't optimize until you know you need to.

#### Compiler optimizations

### 25.3 Kinds of fat adn molasses

#### Common sources of inefficiency
1. input/output operations - overall, the effect of in-memory access is significant enough to make you think twice about having I/O in a speed-critical part of a program
2. paging 
3. system calls - if the system calls are expensive, consider:
    + write your own services
    + avoid going to the system
    + work with the system vendor to make the call faster
4. interpreted languages
5. errors

#### Relative performance costs of common operations


### 25.4 Measurement
* because small parts of a program usually consume a disproportinate share of the run time, measure your code to find the `hot spots`
* `KP:` experience doesn't help much with optimization either. a person's experience might have come from an old machine, language, or compiler - when any of those things changes, all bets are off.
* if it's not worth measuring to know that it's more efficient, it's not worth sacrificing clarity for a performance gamble.

#### Measurement need to be precise
* make sure that you're measuring only the execution time of the code you're tunning.


### 25.5 Iteration
keep trying, even after you find one that works

### 25.6 Summary of the approach to code tunning
1. develop the software by using well-designed code that's easy to understand and modify
2. if performance is poor,
    * a. save a working version of the code so that you can get back to the "last known good state"
    * b. measure the system to find hot spots.
    * c. determine whether the weak performance comes from inadequate design, data type, or algorithms and whether code tunning is appropriate. if code tunning isn't appropriate, go back to step 1.
    * d. tune the bottleneck identified in step (c)
    * e. measure each improvement one at a time
    * f. if an improvement doesn't improve the code, revert to the code saved in step (a)
3. Repeat from step 2
---
checklist