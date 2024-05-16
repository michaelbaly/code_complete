
### 12.1 Numbers in general
Guidelines to make use of numbers less error-prone:
* Avoid "magic numbers"
* Use hard-coded 0s and 1s if you need to
* Anticipate divide-by-zero errors
* Make type conversions obvious
* Avoid mixed-type comparision
`KP:` Heed your compiler's warnings

### 12.2 Integers
1. check for integer division
2. check for integer overflow
3. check for overflow in intermediate results

### 12.3 Floating-point numbers
1. Avoid additions and subtractions on numbers that have greatly different magnitudes
2. Avoid equality comparisons
    + one effective approach is to determin a range of accuracy that is acceptable and then use a boolean function to determin whether the values are close enough.
3. Anticipate rounding errors
    + change to a var type that has greater precision
    + change to binary coded decimal (BCD) var
    + change from floating-point to integer var
4. Check language and lib support for specific data types

### 12.4 Characters and strings
1. Avoid magic characters and strings
2. Watch for off-by-one errors
3. Know how your language and environment support Unicode
    + if you decide to use Unicode strings, decide where and when to use them.
4. Decide on an internationalization/localization strategy early in the lifetime of a program.
    + `key consideration:` whether to store all strings in an exteranl resource and whether to create separate builds for each language or to determine the specific language at run time.
5. If you know you only need to support a single alphabetic language, consider using an `ISO 8859` character set
6. If you need to support multiple languages, use Unicode
7. Decide on a consistent conversion strategy among string types

Strings in C

`KP:` C++ standard template lib string class has eliminated most of the traditional problems with strings in C. For programmers working with C strings, some ways to avoid common pitfalls:
* Be aware of the difference between string pointers an character arrays.
    + In C, assignments do not copy string literals to a string var
    ```
    strPtr = "Some text string"
    ```
    + Use a naming convention to indicate whether the var are arrays of characters or pointers to strings
* Declare C-style strings to have length `CONSTANT + 1`
* Init strings to null(`\0`) to avoid endless strings
* Use arrays of characters instead of pointers in C
* Use strncpy() instead of strcpy() to avoid endless strings

### 12.5 Boolean vars
1. Use boolean vars to document your program - `boolean expression`
2. Use boolean vars to simplify complicated tests.
3. Create your own boolean type, if necessary (not defined with the platform)

### 12.6 Enum types
1. Use enumerated types for readability
2. Use enumerated types for reliability
3. Use enumerated types for modifiability
4. ... as an alternative to boolean vars
5. Check for invalid values
6. Define the first and last entries of an enumeration for use as loop limits
7. Reserve the first entryin the enum type as invalid
8. Define precisely how First and Last ele are to be used in the project coding standard, and use them consistently.
9. Beware of pitfalls of assigning explicit values to ele of an enumeration

### 12.7 Named constants
1. Use named constants in data declarations
2. Avoid literals, even `safe` ones
3. Simulate named constants with appropriatedly scoped vars or classes
4. Use named constants consistently

### 12.8 Arrays
1. Make sure that all array indexes are within the bounds of the array
2. Consider using containers instead of arrays, or think of arrays as sequential structure - `sets/stacks/queues,etc`
3. Check the end points of arrays
4. If an array is multidimensional, make sure its subscripts are used in the correct order.
5. Watch out for index cross-talk - switching loop indexes is called `index cross-talk`
6. In C, use the `ARRAY_LENGTH()` macro to work with arrays

### 12.8 Creating your own types
Guidelines for creating your own types:
1. create types with functionally oriented names - use type names that refer to the real-word problem
2. avoid predefined types
3. don't redefine a predefined type
4. define substitute types for portability
5. consider creating a class rather than using a typedef

---
### checklist
