### 31.1 Layout fundamentals

#### The fundamental theorem of formatting
+ `KP:` use the one shows the structure better rather the looks better

#### Human and computer interpretations of a program

#### How much is good layout worth?
* `KP:` structure helps experts to perceive, comprehend, and remember important features of programs.

#### Layout as religion
* good programmer should be open-minded about their layout practices and accept practices proven to be better than the ones they're used to.

#### Objectives of good layout
Good layout scheme:
* accurately represent the logical structure of the code
* consistently represent the logical structure of the code
* improve readability
* withstand modifications

How to put the layout objectives to use
* `KP:` use the criteria for a good layout scheme to ground a discussion of layout so that the subjective reasons for preferring one style over another are brought into the open.

### 31.2 Layout Tech.

#### White space

#### Parentheses

### 31.3 Layout styles
* pure blocks
* emulating pure blocks
* using *begin-end* pairs to designate block boundaries
* endline layout


### 31.4 Laying out control structures

#### Fine points of formatting control-structure blocks
Guidelines:
* avoid unindented begin-end pairs
* avoid double indentation with begin and end

#### Other considerations
* use blank lines between paragraphs
* format single-statement blocks consistently
* for complicated expressions, put separate conditions on separate lines
* avoid gotos
* no endline exception for case statements


### 31.5 Laying out individual statements
#### Statement length - 80 characters
* line longer than 80 chars are hard to read
* 80-chars discourages deep nesting
* liner longer than 80 often won't fit on 8.5" * 11" paper

#### Using spaces for clarity
* use space to make logical expressions readable
* use space to make array references readable
* ... to make routine arguments readable 

#### Formatting continuation lines
* make the incompleteness of a statement obvi .
* keep closely realted elements together
* indent routine-call continuation lines the standard amount
* indent control-statement ...
* do not align right sides of assignment statements
* indent assignment-statement continuation lines the standard amount

#### Using only one statement per line

#### Laying out data declarations
* use only one data declaration per line
* declare vars close to where they're first used
* order declarations sensibly - group by type
* in C++, put * next to the var name in pointer declarations or declare pointer types


### 31.6 Laying out comments
Comments done well can greatly enhance a program's readability
* indent a comment with its corresponding code
* set off each comment with at least one blank line


### 31.7 Laying out routines
* use blank lines to separate parts of a routine
* use standard indentation for routine arguments

### 31.8 Laying out classes

#### Laying out class interfaces

#### Laying out class implementations

#### Laying out files and programs
* put one class in one file
* give the file a name related to the class name
* separate routines within a file clearly
* sequence routines alphabetically
* in C++, order the source file carefully

---
checklist