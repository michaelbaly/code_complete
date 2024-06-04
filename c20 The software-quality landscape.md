### 20.1 Characteristics of software quality
External characteristics (`user care about`):
* correctness
* usability - the ease with which users can learn and use a system
* efficiency - minimal use of system to perform its required functions
* integrity - the degree to which a system prevents unauthorized or improper access to its programs and its data
* adaptability - the extent to which a system can be used, without modification, in applications or environments 
* accuracy - the degree to which a system is free from error
* robustness - the degree to which a system continues to function in the presence of invalid inputs or stressful environmental conditions

Internal ... (`programmers care about`):
* maintainability - the ease with which you can modify a software system to change or add capabilities, improve performance, or correct defects
* flexibility 
* portability - the ease with which you can modify a system to operate in an environment
* reusability
* readability
* testability - the degree to unit-test and system-rest
* understandability 


### 20.2 Techniques for improving software quality
Software quality assurance is a planned and systematic program of activities designed
to ensure that a system has the desired characteristics.
* software-quality objectives - from both external and internal characteristics
* explicit quality-assurance activity - the organization must show programmers that `quality is a priority`
* testing strategy
* software-engineering guidelines - should control the technical character of the software as it's developed
* informal technical reviews - before formal review
* formal technical reviews
* external audits

1. development process
    + change-control procedures
    + measurement of results

2. setting objectives - The `surprising implication` is that people actually do what you ask them to do

### 20.3 Relative effectiveness of quality techniques

1. percentage of defects detected - The strong implication is that if project developers are striving for a higher defectdetection rate, they need to use a combination of techniques
    + `KP:`the upshot is that defect-detection methods work better in combination than they do singly.

2. cost of finding defects - Most studies have found that inspections are cheaper than testing

3. cost of fixing defects - That isn’t true because the longer a defect remains in the system, the `more expensive it becomes to remove`.

The bottom line is that an effective software-quality program must include a combination of techniques that apply to all stages of development. Here’s a recommended combination for achieving higher-than-average quality:
* Formal inspections of all requirements, all architecture, and designs for critical
parts of a system
* Modeling or prototyping
* Code reading or inspections
* Execution testing
 
### 20.4 When to do quality assurance
It’s a good idea to catch `requirements and architecture errors` before they affect later activities.

`KP:`Defects creep into software at all stages. Consequently, you should emphasize qualityassurance work in the early stages and throughout the rest of the project.

### 20.5 The general principle of software quality

`KP:` improving quality reduces development costs

---
checklist