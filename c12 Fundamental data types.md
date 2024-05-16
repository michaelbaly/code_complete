
### 11.1 Considerations in choosing good names

1. The most inportant naming consideration

`KP:` the name fully and accurately describe the entity the var represents

2. Problem orientation

`KP:` A good name generally speaks to **the problem** rather than **the solution**.

3. Optimum name length
    + 8 to 20 characters generally (more easy to debug)

4. The effect of scope on var names
    + Use qualifiers on names that are in the global namespace

5. Computed-value qualifiers in var names
6. Common opposites in var names

### 11.2 Naming specific types of data

1. naming loop indexes
2. naming status vars
    + think of a *better name* than flag for *status vars*
3. naming temp vars
    + be leery of "temporay" vars, temp var also needs specific meaning
4. naming boolean vars
    + keep typical boolean names in mind - *done, error, found, success, ok*
    + give boolean vars names that imply *true or false*
    + use positive boolean var names
5. naming enumerated types -  with specific *prefix*
6. naming constants

### 11.3 The power of naming conventions
1. why have conventions ? - conventions offer benefits:
    + they let you take more for granted.
    + they help you transfer knowledge across projects.
    + they help you learn code more quickly on a new project
    + they reduce name proliferation
    + they compensate for language weaknesses
    + they emphasize relationships among related items

2. when you should have a naming conventions
    + when multi programmer are working on a project
    + when you plan to turn a program over to another programmer for modification/maintenance
    + when your programs are reviewed by other programmers in your org.
    + when your program is so large
    + when the program will be long-lived enough
    + when you have a lot of unusual terms and want to have standard terms to use in coding.

3. Degrees of formality

### 11.4 Informal naming conventions
1. Guidelines for a language-independent convention
2. Guidelines for language-specific conventions - c/c++/java
3. Mixed-language programming considerations

### 11.5 Standardized prefixes
1. user-defined type abbreviations (UDT)
2. advantages of standardized prefixes
    + add precision to several ares of naming
    + make names more compact
    + allow you to check types accurately when using ADT(abstract data types) that your compiler can't necessarily check.

### 11.6 Creating short (for readable)
1. General abbreviation guidelines
2. Comments on abbreviation
### 11.7 Kinds of names to avoid
1. avoid misleading names or abbreviations
2. avoid names with similar meanings
3. avoid vars with different meanings but similar names
4. avoid names that sound similar, such as wrap and rap.
5. avoid numerals in names
6. avoid misspelled words in names
7. avoid words that are commonly misspelled in English
8. don't differentiate var names solely by capitalization
9. avoid multiple natural language
10. avoid the names of standard types, variables, and routines
11. don't use names that are totally unrelated to what the var represent
12. avoid names containing hard-to-read characters


---
### checklist
