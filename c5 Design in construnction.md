## 5.1 Design Challenges
### Design is a wicked problem
* The Tacoma Narrows Bridge

### Design is a sloppy process

### Design is about tradeoffs and priorities
* fast response rate OR minimizing development time ?

### Design involves restrictions
* time, resource are limitted.

### Design is nondeterministic
* dozens of ways to design

### Design is heuristic process

### Design is emergent
* evolve and improve through design reviews, informal discussions, experience writing the code, etc.

## 5.2 Key design concepts
* Good design depends on understanding a handful of key concepts. This section discuss the **role of complexity**, **desirable characteristics** of design, and **levels** of design.

### Software's primary technical imperative: *managing complexity*.

### Importance of managing complexity
* Dijkstra's quote

* Once you understand that all other technical goals are secondary to managing complexity, many design considerations become straightforward.

### Desirable characteristics of s design

#### Internal design characteristics:
1. minimal complexity
2. ease of maintenance --- design the system to be **self-explanatory**
3. loose coupling --- hold connections to a mimimum
4. extensibility --- enhance a system without causing violence to the underlying structure.
5. Reusability --- reuse in other system
6. high fan-in --- a system has been designed to make good use of utility classes at the *low levels* in the system.
7. low-to-medium fan-out --- means having a given class use a low-to-medium number of other classes.
8. portability --- easily move it to another env
9. leanness --- the fatal question "it's easy, so what will we hurt by putting in in ?"
10. stratification --- trying to keep the levels of decomposition stratified so that you can view the system at any single level and get a consistent view.
11. standard techniques

### Levels of design
+ level1 --- software system
+ level2 --- division into subsystems or packages (database, user interface, business rules, command interpreter, report engine, etc.); **rules** about how the various subsystems can communicate are **particular important**.
+ level3 --- division into classes
+ level4 --- division into routines
+ level5 --- internal routine design

## 5.3 Design building blocks: heuristics

### Find real-world objects
* the steps in design objects --- 1 to 5

### Form consistent abstractions
* good programmers create abstractions at the **routine-interface level, class-interface level, and package-interface level**.

### Encapsulate implementation details
* encapsulation helps to manage complexity by forbidding you to look at the complexity.

### Inherit - when inheritance simplifies the design

### Hide secrets(information hiding)
1. secrets and right to privacy
2. an example
3. two categories of secrets
   - hiding complexity
   - hiding sources of changes
4. barriers to information hiding
   - excessive distribution of information
   - circular dependencies --- A -> B -> C -> A (avoid such loops)
   - class data mistaken for global data --- thinking of class data as global data and avoiding it because you want to avoid the problems associated with global data.
   - perceived performance penalties --- to create a **highly modular design** at coding level
   - value of information hiding --- get into the habit of asking "what should I hide?"

### Identify areas likely to change
#### Steps should follow:
1. identify items that seem likely to change
2. separate itmes that are likely to change
3. isolate itmes that seem likely to change

#### anticipating different degrees of changes

### Keep coupling loose
* Coupling discribes **how tightly** a class or routine is related to other classes or routines.
  - Goal: small, direct, visible, and flexible relations --- known as *loose coupling*
* Coupling criteria --- evaluating coupling between modules:
  - size: number of connections between modules
  - visibility: prominence of connection between two modules
  - flexibility: how easily you can change the connections between modules

* Kinds of coupling
  - simple-data-parameter coupling
  - simple-object coupling
  - object-parameter coupling

* Semantic coupling --- it's dangerous because changes undetectable by the compiler

[***] **Classes and routines are first and foremost intellectual tools for reducing complexity. If they're not making yoru job simpler, they're not doing their jobs.**

### Look for common design patterns
* Patterns provide several benefits:
  1. reduce complexity by providing ready-made abstractions
  2. reduce errors by institutionalizing details of common solutions
  3. provide heuristic value by suggesting design alternatives
  4. streamline communication by moving the design dialog to a higher level

* Overall, design patterns are a powerful tool for managing complexity

### Other heuristics
* Aim for strong cohesion
* Build hierarchies
* ...
* Draw a diagram
* Keep your design modular --- like a "black box"

### Summary of design heuristics

### Guidelines for using heuristics
* Poly's generalized problem-solving approach --- focus on problem solving in mathematics
  1. understanding the problem
  2. Devising a plan --- Find the connection between the data and the unknown
  3. Carrying out the plan
  4. Looking Back --- examine the solution

## 5.4 Design practices
### Iterate
* Design is an iterative process. You don't usually go from point A only to B; you go from A to B and back to A.
### Divide and conquer
### Top-down and bootom-up design approaches
* Argument for top-down
1. guiding principle: human brain can concentrate on only a certain amount of details at a time
2. continuing decomposing **until** it seems as if it would be easier to code the next level than to decompose it.
* Argument for bottom-up
1. what the system needs to do ?
2. identify concrete objects and responsibilities from #1
3. identify common objects and group them using ...
4. continue with next level or go back

* Summary: top-down tends to start simple, but sometimes low-level complexity ripples bck to the top which in turn make things more complex; bottom-up tends to start complex, but **identifying that complexity early**.

### Experimental prototyping
* You can't fully define design problem until you've partially solved it.
* Addressing these questions at low cost --- experimental prototyping.
* specific question provides a mor solid basis for *prototyping*
* *throwaway* code
---

### Collaborative design
* several forms ...
* **the goal**: quality assurance or to foster creativity and to increse the number of design alternatives ?

### How much design is enough?
* Design formality and level of details needed -- Table 5-2

`
I've never met a human being who would want to read 17,000 pages of documentation, and if there was, I'd kill him to get him out of the gene pool.
    --- Joseph Costello
`

### Capturing your design work
* Insert design doc into code itself
* Capture design discussions and decisions on a wiki
* Write e-mail summaries
* Use a digital camera
* Save design flip charts
* Use CRC(class, responsiblity, collarborator) cards
* Create UML diagram at appropriate levels of detail

## 5.5 Comments on popular methodologies
* Additional resources
