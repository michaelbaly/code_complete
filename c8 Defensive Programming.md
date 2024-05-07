## Key point

1. In defensive programming, the main idea is that if a routine is **passed bad data**, it won't be hurt, even if the bad data is another routine's fault.

### 8.1 Protecting your program from invalid inputs


### 8.2 Assertions

1. Assertion are especially useful in **large, complicated programs and in high-reliability** programs.
2. During **development**, assertions flush out contradictory assumptions, unexpected conditions, etc., during **production**, they can be compiled out of the code so that the assertions don't degrade system performance.

#### Build your own assertion mechanism

#### Guidelines for using assertions

1. Use error-handling code for conditions you **expect to occur**; use assertions for conditions that should **never occur**.
2. Avoid putting executable code into assertions.
3. Use assertions to **document and verify** preconditions and postconditions. - {p}S{q} where p is precondition and q is postcondition [correctness-tripple].
4. For highly robust code, assert and then handle the error anyway.

### 8.3 Error-handling Tech.
TODO