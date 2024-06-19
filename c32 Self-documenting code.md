### 32.1 External documentation
1. unit development folders - UDF, or software-development folder - SDF, is an informal docs that contains notes used by a developer during construction. the `main purpose` of a UDF is to provide a trial of design decisions that aren't documented elsewhere.

2. detailed-design document - is the low-level design document. it describe the calss-level or routine-level design decisions, the alternatives that were considered, and the reasons for selecting the approaches that were selected.

### 32.2 Programming style as documentation
Internal docs is found within the programming listing itself.

### 32.3 To comment or not to comment
`KP:` Comments should explain, at higher level of abstraction than the code, what you're trying to do.

### 32.4 Keys to effective comments

#### Kinds of comments - six categories:
1. repeat of the code
2. explanation of the code
3. marker in the code - isn't intended to be left in the code, a note to the developer that the work isn't done yet.
4. summary of the code
5. description of the code's intent
6. information that cannot possibly be expressed by the code itself.

#### Commenting efficiently
Effective commenting isn't that time-consuming. 
Guidelines:
* use styles that don't break down or discourage modification - `KP:` The point is that you should pay attention to how you spend your time. If you spend a lot of time entering and deleting dashes to make plus signs line up, you’re not programming;
you’re wasting time. Find a more efficient style.

* use the pseudocode programming process to reduce commenting time. - if you outline the code in comments before you write it, you win in several ways.

* integrate commenting into your development style - commenting down later takes more time, Code that requires that much concentration is a warning sign

* performance is not a good reason to avoid commenting - running the code through a tool that strips out comments as part of the build process

#### Optimum number of comments

### 32.5 Commenting techniques

#### Commenting individual lines
The single line is complicated or had an error once
Guidelines:
* avoid self-indulgent comments
```
MOV AX, 723h ; R. I. P. L. V. B.
```
* avoid endline comments on single lines - most endline comments just repeat the line of code, which hurts more than it helps.

* avoid endline comments for multiple lines of code - doesn't show which lines the comment applies to.

When to use endline comments - three exceptions
* use endline comments to annotate data declarations
* avoid using endline comments for maintenance notes
```
for i = 1 to maxElmts – 1 -- fixed error #A423 10/1/05 (scm)
```
* use endline comments to mark ends of blocks

#### Commenting paragraphs of code
* write comments at the level of the code's intent
* focus your documentation efforts on the code itself
* focus paragraph comments on the why rather than the how
* use comments to prepare the reader for what is to follow
* make every comment count
* document surprises

### 32.6 IEEE standards