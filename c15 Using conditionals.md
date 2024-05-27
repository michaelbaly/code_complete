### 15.1 *if* statements

1. plain *if-then* statements

    Guidelines when writing if statements:
    + `KP:`write the nominal path through the code first; then write the unusual cases 
    + make sure that you branch correctly on equality - use `>` instead of `>=` to avoid off-by-one error
    + put the normal case after the if rather than after the else
    + follow the if clause with a meaningful statement
    + consider the else clause
    + test the else clause for correctness
    + check for reversal of the if and else clauses

2. chains of *if-then-else* statements
    + simplify complicated tests with boolean function calls
    + put the most common cases first
    + make sure that all cases are covered

### 15.2 *case* statements

1. choosing the most effective ordering of cases
    + order cases alphabetically or numerically
    + put the normal case first
    + order cases by frequency

2. tips for using case statements
    + keep the actions of each case simple
    + don't make up phony vars able to use the case statement
    + use the default clause only to detect legitimate defaults
    + use the default clause to detect errors
    + in C++ and Java, avoid dropping through the end of a case statement
    + in C++, clearly and unmistakably identify flow-throughs at the end of a case statement

