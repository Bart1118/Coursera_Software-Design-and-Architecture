# Final Exam

Quiz • 30 min

### 1. The first stage of the two-stage design process is \_\_\_\_\_\_\ design.

> Hint: This stage has activities like creating CRC cards, talking with the customer about their requirements, and creating mockups. 

conceptual
> The correct answer is concept or conceptual design. This is the stage before technical design, where you will solicit customer requirements and use this to create a working conceptual design, using mockups and other early design techniques.

### 2. The second stage of the two-stage design process is ________ design.

> Hint: This is when you will define the structure of the code and start turning your mockups into classes.

technical
> The correct answer is technical design. This is the stage at which the developers will start to turn the conceptual design into a more precise technical design. They could do this by using the UML design language, by specifying which methods will be coded for each class, etc.

### 3. Which of these conceptual design techniques will help you analyze the problem space to determine classes for your object-oriented software? **Choose the two correct answers.**

- [ ] requirements

- [x] CRC
> Correct. CRC Cards will help you identify classes.

- [x] mockups
>Correct. Mockups will help you visualize your problem space in the earliest stages.

- [ ] tradeoffs

### 4. During conceptual design, once the problem is mapped into components, what are the other two critical pieces of information that you must specify for these classes or components? **Choose the two correct answers.**

- [ ] methods

- [ ] abstract data types

- [x] responsibilities

- [x] collaborators

### 5. You are writing the CRC card for a Bear component. Choose the **two** responsibilities.

- [ ] camper

- [x] den

- [x] eat berries

- [ ] hunger

### 6.You are writing the CRC card for a Bear component. Choose the three collaborators.

- [x] bear

- [ ] guitar

- [x] tree

- [ ] computer

- [x] den

### 7. You create an object that represents a **user**, storing important information about them such as their preferences. What kind of object is this?

- [ ] client

- [x] entity

- [ ] control

- [ ] boundary

### 8. You create an object that represents a **dialog box**. It creates buttons and text fields, etc, for the user to interact with, and it logs those interactions. What kind of object is this?

- [x] boundary

- [ ] entity

- [ ] interaction

- [ ] display

- [ ] control

### 9. You create an object that compares values from two different sources. It then updates the smaller value to be equal to the larger one. What kind of object is this?

- [ ] repository

- [ ] update

- [ ] entity

- [x] control

### 10. Which of these is an example of a quality tradeoff?

- [x] Adding security knowing it will reduce speed

- [ ] Not delivering key features so that deadlines can be met

- [ ] Limiting features knowing that they can be added later

- [ ] Adding preferences that allow users to switch some features on and off

### 11. What is the term for reducing a class or object to its inputs and outputs in modelling?

- [ ] filter thinking

- [x] black box thinking

- [ ] pipe thinking

- [ ] process thinking

### 12. Which one of these classes is in most need of being decomposed?

- [ ] Student

- [ ] Book

- [ ] Store

- [ ] Order

### 13. In order to provide good encapsulation, fill-in-the-blanks on this UML class diagram: (Replace the underscores _ from top to bottom with minus signs ("-") or plus signs ("+"); your answer will be a string of six + or - signs with no spaces)

![[Pasted image 20230324183520.png]]

--++++

### 14. You are writing a simple soccer video game. Select the best example of proper abstraction:

![[Pasted image 20230324183614.png]]

  

- [x] **a)**

- [ ] **b)**

- [ ] **c)**

- [ ] **d)**

### 15. Which design principle enables developers to follow the guideline **D.R.Y.** ("Don't Repeat Yourself"):

- [x] generalization

- [ ] encapsulation

- [ ] decomposition

- [ ] abstraction

### 16. Which of these UML class diagrams shows an association relationship?

![[Pasted image 20230324183926.png]]

  

- [ ] **a)**

- [x] **b)**

- [ ] **c)**

- [ ] **d)**

### 17. Which of these UML class diagrams depicts an aggregation ("has-a") relationship between the two classes?

![[Pasted image 20230324184028.png]]

- [x] **a)**

- [ ] **b)**

- [ ] **c)**

- [ ] **d)**

### 18. Which of these UML class diagrams depicts a composition, or a strong "has-a" relationship?

![[Pasted image 20230324185607.png]]

- [ ] **a)**

- [ ] **b)**

- [ ] **c)**

- [x] **d)**

### 19. Select the object pairing that has an **association** relationship:

- [x] Hiker - Trail

- [ ] Tree - Root

- [ ] Coffee - Water

- [ ] Book - Page

### 20. Select the object pairing that has an **aggregation** relationship:

- [ ] Book - Page

- [x] Stapler - Staple

- [ ] Pie - Crust

- [ ] Car - Road

### 21. Select the object pairing that has a **composition** relationship:

- [ ] Bear - Forest

- [ ] Tea - Sugar

- [x] Book - Page

- [ ] Record Player- Record 

### 22. Choose the **two answers** that correctly complete the following sentence:

**"We say that a class has low cohesion if..."**

- [ ] ...connects to many other classes.

- [x] ...it tries to encapsulate too many unrelated responsibilities.
> Correct. Cohesion is the degree to which a class is directed toward one purpose. Giving it unrelated responsibilities reduces cohesion.

- [ ] ...it does not have all the necessary parts, i.e. it is incomplete.

- [x] ...its purpose is unclear.
> Correct. Cohesion is how well a class is directed toward a clear, singular purpose.

### 23. Two classes are tightly coupled. What are some ways you might be able to tell? **Choose the two correct answers.**

- [ ] They can easily be swapped with different implementations of the same class

- [x] In order to understand one class, you need to open up the other to look at the implementation
> Correct. This is usually a sign that the coupling is too tight; instead, the interfaces should be clear and interactions limited.

- [ ] Their interactions are limited and controlled

- [x] They are very highly reliant on each other
> Correct. Coupling refers to how deeply integrated different components are. Tight coupling means the components are deeply integrated, which is not desirable because it makes it more difficult to make changes. 

### 24. How can you apply the principle of Separation of Concerns in object-oriented programming?

- [x] Separate objects or components according to their role in the software
> Correct! Each object or component should have a fairly specific role or concern in the software which is separate from the concerns of other objects. 

- [ ] Split developers into teams that each deal with different parts of the software

- [ ] Ensure classes are only concerned with their own data

- [ ] Separate data and actions (methods) into different classes

### 25. Which of these violates **Liskov's Substitution Principle**?

- [ ] subclasses specify the abstract methods of the superclass

- [ ] the subclass adds behaviour

- [ ] the superclass is too general

- [x] an operation in the superclass is replaced by a different operation in the subclass
> Correct! This directly violates Liskov's substitution principle, which is a useful test to identify poor uses of inheritance. 

### 26. For which of these situations would you use a sequence diagram?

- [ ] To show all of the different processes of your program.

- [ ] To show the different modes that your program can be in.

- [ ] To show the relationship between classes

- [x] To show the collaborative behaviour of objects in your program.

### 27. Choose the correct state diagram for a car which has a state called "HasGas:"

![[Pasted image 20230324190013.png]]

  

- [ ] **a)**

- [ ] **b)**

- [x] **c)**
> Correct! The state goes at the top, variables in the middle, and activities (including exit and entry activities) in the bottom.

- [ ] **d)**

### 28. Which of these elements represents a termination in a UML State diagram?

![[Pasted image 20230324190050.png]]

- [x] **a)**

- [ ] **b)**

- [ ] **c)**

- [ ] **d)**

### 29. What is the purpose of model checking?

- [ ] To verify that the conceptual model of your software matches the customer's requirements.

- [ ] To test for user-reported bugs

- [ ] To verify that the technical implementation matches conceptual mockups

- [x] To check the software for errors before release

### 30. What is an abstract data type?

- [ ] a data-centric class

- [x] a type of data defined by the developer rather than the language.

- [ ] variables that are assigned a type (i.e. integer, double) but does not yet have a value assigned.

- [ ] a data type that cannot be used directly but must be implemented as an interface