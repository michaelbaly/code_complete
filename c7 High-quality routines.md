## 7.1 Valid reasons to create a routine
* Reduce complexity
* Introduce an intermediate, understandable abstraction
* Avoid duplicate code
* Support subclassing
* Hiding sequences
* Hide pointer operations
* Improve portability
* Simplify complicated boolean tests
* Imporve performance

### Operations that seem too simple to put into routines
* mental block --- *reluctance* to create a simple routine for a simple purpose.
### Summary
---
## 7.2 Design at the routine level
* The goal is to have each routine do one thing well and not do anything else.
* *functional cohesion* is the strongest and best kind of cohesion, occuring when a routine performs one and **only one** operation
* cohensions considered to be less than ideal:
  1. *sequential conhesion* exist when a routine contains operations that must be performed **in a specific order**, that share data from step to step, and that don't make up a complete function when done together
  2. *communicational cohesion* occurs when operations in a routine make use of the same data and aren't related in any other way
  3. *temporal cohesion* occurs when operations are combined into a routine because they are all done at the same time
* cohension considered to be unacceptable:
  1. *procedural cohesion* occurs when operations in a routine are done in a **specified order**
  2. *logical cohesion* occurs when several operations are stuffed into the same routine and one of the operations is selected by a control flag that's passed in. --- "illogical cohension" maybe a better name because operations are unrelated.
  3. *conincidental conhesion* occurs when the operations in a routine have no discernible relationship to each other.
* **focus your attention** on functional cohesion for maximum benefit
---
## 7.3 Good routine names
* Guidelines:
  1. describe everything the routine does
  2. avoid meaningless,vague,or wishy-washy verbs
  3. don't differentiate routine names solely by number
  4. make names of routines as long as necessary
  5. to name a function, use a description of the return value
  6. to name a procedure, use a strong verb followed by an object
  7. use opposites precisely
  8. establish conventions for common operations
---
## 7.4 How long a routine can be?
* be careful if you want to write routines longer than about 200 lines.
## 7.5 How to use routine parameters
* Guidelines for minimizing IF problems:
  1. put parameters in input-modifiy-output order
  2. consider creating your own **in** and **out** keywords
  3. if serveral routines use similar parameters, put the similar parameters in a **consistenet order**
  4. use all the parameters
  5. put status or error variables lasst
  6. don't use routine parameters as working variables --- use local variable instead
  7. document IF assumptions about parameters
  8. limit the number of a routine's parameters ot about seven
  9. consider an input,modify,and output naming convention for parameters
  10. use named parameters
  11. make sure actual parameters match formal parameters
## 7.6 Special consideration in the use of functions

### when to use a function and when to use a procedure
* in short, use a function if the primary purpose of the routine is to return the value indicated by the function name. otherwise, use a procedure

### setting the function's return value
* check all possible return paths
* don't return references or pointers to local data

---

## 7.7 Macro routines and inline routines

### fully parenthesize macro expressions
```
#define cube(a) a*a*a

#define cube(a) (a)*(a)*(a)

#define cube(a) ((a)*(a)*(a))
```
### surround multiple-statement macros with curly braces
```
#define LookupEntry(key, index) \
    index = statement1; \
    index = statement2; \
    index = statement3; \
    ...

#define LookupEntry(key, index) { \
    index = statement1; \
    index = statement2; \
    index = statement3; \
    ...
}
```
### name macros that expand to code like routines so that they can be replaced by routines

### limitations on the use of macros routines
* c++ alternative ways to use macros:
  1. *const*
  2. *inline*
  3. *template*
  4. *enum*
  5. *typedef*

### inline routines
* the theory is that inline can help produce high efficient code that avoids routine-call overhead
* use inline routines sparingly
