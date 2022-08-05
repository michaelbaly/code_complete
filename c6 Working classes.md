## 6.1 Fundations : ADTs
* Understanding ADTs is essential to understanding OOP
### Example of need for an ADT

### Benefits of using ADTs
1. hide implementation details
2. changes don't affect the whole program
3. make the interface more informative
4. easier to improve performance
5. the program is more obviously correct
6. the program becomes more self-documenting
7. don't have to pass data all through your program
8. able to work with real-world entities rather than with low-level implementation

### More example
1. build or use **typical low-level data types** as ADTs; treat yourself to the highest possible level of abstraction
2. treat common objects such as file as ADTs
3. treat even single items as ADTs
4. refer to an ADT independently of the medium it's stored on

### Handling multiple instances of data with ATDs in none-object-oriented evn
* Three ways to handle ADT interface
1. explicitly identify instances each time you use ADT service.
2. explicitly provide the data used by the ADT service.
3. Use implicit instances(**with great care**)

### ADTs and classes

## 6.2 Good class interface
* high-quality class <- a **good interface**
### Good abstraction
* Guidelines
1. present a consistent level of abstraction in the class interface --- mixed level of abstraction should be avoid
2. be sure you understand what abstraction the class is implementing
3. provide services in pairs with their opposites
4. move unrelated information to another class
5. make IFs programmatic rather than semantic when possible
6. don't add public members that are inconsistent with the IF abstraction
7. consider abstraction and cohesion together

### Good encapsulation
* ENC is the *enforcer* that prevents your know the details
1. minimize accessibility of classes and members
2. don't expose member data in public
3. avoid putting private implementation details into a class's IF
4. don't make assumptions about the class's users
5. avoid friend classes
6. don't put a routine into the public interface **just because** it uses only public routines
7. favor read-time convenience to write-time convenience
8. be very, very wary of semantic violations of ENC
9. watch for coupling that's too tight

## 6.3 Design and implementation issues
### Containment ("has a" relationships)
* Containment is the work-horse technique in OOP
1. implementation "has a" through containment
2. implement "has a" through private inheritance as a last resort
3. be critical of classes that contain more than about seven data members
### Inheritance ("is a" relationships)
* inheritance is the idea **one class is a specialization of another class**. it helps avoid repeating code
---
* when to use inheritance:
  - For each member routine, will the routine be visible to derived classes ?...
  - For each data member, will it be visible to derived classes ?
* ins and outs:
1. implement "is a" through public inheritance
2. design and document for inheritance or prohibit it
3. adhere to the LSP --- *Subclasses must be usable through the base class IF without need for the user to know the difference*
4. be sure to inherit only what you want to inherit
```
inherited routines cames in:
  1. abstract overridable routines --- inherit IF but not its implementation
  2. overridable routines --- inherit IF and default implementation, and allow to override default imp.
  3. non-overridable --- inherit IF and not allow to override routine's imp.
```
4. don't override a non-overridable member function
5. move common IF,data,and behavoir as high as possible in the inheritance
6. be suspicious of classes of which there's only one instance
7. be suspicious of base classes of which there's only one derived class
8. be suspicious of classes that override a routine and do nothing inside the derived routine
9. avoid deep inheritance trees
10. prefer polymorphism to extensive type checking
11. make all data private, not protected

#### Multiple inheritance

#### Why are there so many rules for inheritance ?
* to manage complexity
* when to use inheritance and when to use containment
1. if multiple classes share common data but not behavoir, create a common object that those classes can contain
2. if ... share common behavoir but not data, derive them from a common base class that defines the common routines
3. if ... share common data and behavoir, inherit from a common base class that defines the common data and routines
4. inherit when you want base class to control your IF, contain when you want to control your IF

---
### Member functions and data
* **Guidelines** for implementing member functions and member data **effectively**

1. keep the number of routines in a class as small as possible
2. disallow implicitly generated member functions and operators you don't want
3. minimize the number of different routines called by a class
4. minimize indirect routine calls to other classes
5. in general, minimize the extent to which a class collaborates with other classes

### Constructors
* Guidelines
1. initialize all member data in all constructors, if possible
2. enforce the singleton property by using a **private** constructor
3. prefer deep copies to shallow copies until proven otherwise

## 6.4 Reasons to create a class
* Good reasons to create a class:
1. model real-world objects
2. model abstract objects
3. **reduce complexity**
4. isolate complexity
5. hide implementation details
6. limit effects of changes
7. hide global data
8. streaming parameters passing
9. make central points of control --- similiar to information hiding ,but more heuristic power
10. facilitate reusable code --- NASA's example
11. plan for a family of programs --- what the whole family of programs might look like?
12. package related operations
13. accomplish a specific refactoring

### classes to avoid
* avoid creating god classes
* eliminate irrelevant classes
* avoid classes named after verbs

### summary

## 6.5 language-specific issues
* class-related areas that vary significantly **depending on th language**
* ...

## 6.6 Beyond classes: packages
