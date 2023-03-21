### 1. Which of these terms are used to describe coupling? **Choose the 3 correct answers.**

- [x] degree

- [x] ease

- [ ] frequency

- [x] flexibility

- [ ] exposed

### 2. Which is the most desirable?

- [ ] high cohesion, tight coupling

- [ ] low cohesion, tight coupling

- [x] high cohesion, loose coupling

- [ ] low cohesion, loose coupling

### 3. What are some keywords you might use for information hiding in Java? **Select the three correct answers.**

- [x] private

- [ ] abstract

- [x] protected

- [x] \[none\]

### 4. What are the best ways to promote Conceptual Integrity in your software? **Choose the two correct answers.**

- [ ] Good commenting

- [x] Regular code reviews

- [ ] Delegating development of different components to different teams

- [x] Planning the architecture of the system

### 5. **Information Hiding** is closely related to one of the core design principles of object-oriented design. Which one?

- [ ] abstraction

- [ ] decomposition

- [x] encapsulation

- [ ] generalization

### 6. Which of these sequence diagrams is correct?

![[Pasted image 20230321145842.png]]
![[Pasted image 20230321145856.png]]
![[Pasted image 20230321145906.png]]
![[Pasted image 20230321145913.png]]

- [ ] **a)**

- [x] **b)**

- [ ] **c)**

- [ ] **d)**

### 7. What are elements of a state in a State diagram (see diagram)? **Choose the three correct answers.**

![[Pasted image 20230321145930.png]]

- [ ] events

- [x] state name

- [x] activities

- [ ] responsibilities

- [x] state variables

### 8. When is **Model Checking** conducted?

- [ ] After deployment

- [ ] During planning

- [x] After development

- [ ] During development

### 9. What are the phases of Model Checking? **Choose the 3 correct answers.**

- [x] Modeling Phase.

- [x] Analysis Phase

- [ ] Counterexample Phase

- [x] Running Phase

- [ ] Model Simulation

### 10. During model checking, what is the name for a violation of the desired properties of the model?

- [ ] Model Gap

- [x] Counterexample

- [ ] Error

- [ ] Redevelopment

### 11. When two processes cannot run because they are waiting on the same resource, it's called…

- [ ] State lock

- [x] Deadlock

- [ ] Transition lock

- [ ] Mutual lock

### 12. Choose the **three** examples of inheritance used **poorly**:

- [x] Inheritance is used to share behaviour without specializing
> Correct! If inheritance is merely used to share behaviour and not much more, consider skipping it altogether and just using the superclass.

- [ ] The subclasses inherit methods from the superclass and have their own specific, related methods.

- [x] A method in the superclass is overwritten with different behaviour by a subclass.
> Correct! This violates Liskov's Substitution Principle, which states that a superclass should be able to be substituted by a subclass without error.

- [x] A subclass inherits methods from the superclass and adds extra, new, unrelated functionality
> Correct! If your subclass inherits some behaviour and adds unrelated functionality, it is not very coherent. You should consider decomposing these responsibilities into different interfaces.