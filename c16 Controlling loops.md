### 16.1 Select the kind of loop

1. when to use a *while* loop - the main issue with respect to while loop is deciding whether to test at the beginning or the end of the loop
    + loop with test at the beginning
    + loop with test at the end

2. When to use a *loop-with-exit* loop - the exit condition appears in the middle of the loop rather at the begining or at the end
    + normal loop-with-exit
    + abnormal loop-with-exit - necessary use of `goto`

3. when to use a *for* loop

4. when to use a *foreach* loop

### 16.2 Controlling the loop

First, minimize the number of factors that affect the loop; 
Second, treat the inside of the loop as if `it were a routine`; 
Don't make the reader look inside the loop to understand the loop control

1. entering the loop - guidelines
    + enter the loop from one location only
    + put initialization code directly before the loop - it's easier to avoid errors during modification if related statements are kept together
    + use while(true) for infinite loops - or for(;;) alternative
    + prefer for loops when they're appropriate
    + don't use a for loop when a while loop is more appropriate

2. processing the middle of the loop - subsections 
    + use { and } to enclose the statements in a loop
    + avoid empty loops
    + keep loop-housekeeping chores at either the beginning or the end of the loop (at the end typically)
    + make each loop perform only one function

3. exiting the loop
    + assure yourself that the loop ends
    + make loop-termination conditions obvious
    + don't monkey with the loop index of a for loop to make the loop terminate
    + avoid code that depends on the loop index's final value
    + consider using safety counters

4. exiting loops early
    + consider using `break` statements rather than boolean flags in a while loop
    + be wary of a loop with a lot of breaks scattered through it
    + use `continue` for tests at the top of a loop
    + use the labeled break structure if your language supports it - like `JAVA`
    + use break and continue only with caution

5. checking endpoints
    + `KP:` willingness to perform this kind of check is a key difference between efficient and inefficient programmers. Efficient programmer do the work of mental simulations and hand calculations because they know that such measures help them find errors.

6. using loop vars
    + use ordinal or enumerated types for limits on both arrays and loops
    + use meaningful var names to make nested loops readable
    + use meaningful names to avoid loop-index cross-talk
    + limit the scope of loop-index vars to the loop itself

7. how long should a loop be?
    + make your loops short enough to view all at once
    + limit nesting to three levels
    + move loop innards of long loops into routines
    + make long loops especially clear

### 16.3 Creating loops easily - from the inside out
    first, in comments; 
    seconds, convert the comments in the body of the loop to code
    ...

### 16.4 Correspondence between loops and arrays 
