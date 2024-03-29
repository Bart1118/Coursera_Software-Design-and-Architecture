## Inheritance Issues

Object-oriented modeling, tries to take concepts in a problem space and model them in a piece of software. 

Given how complicated a problem can be, we need to refine our models through design principles, ***abstraction***, ***encapsulation***, ***decomposition*** and ***generalization***.

Each of these principles requires you to make a decision on how they apply to your system. 

+ What attributes and behaviors do you need to model in a class through abstraction? 

+ How are these attributes and behaviors grouped together and accessed through encapsulation? 

+ Can my classes be simplified into smaller parts using decomposition? 

+ Are there common things across my objects that can be generalized? 

These principles are meant to guide the choices that you make when designing an object-oriented system. 

Some design decisions will be easier to make than others. 

For example, a car can have attributes such as color, make, and model. It has behaviors, like acceleration and steering. The car can be decomposed into its parts, like engine, transmission, and battery. But how does everything relate to each other? Can we generalize any parts of the car? Generalization and inheritance are some of the more difficult topics to master in object-oriented programming and modeling. 

Well inheritance is a powerful design tool that can help you create clean, reusable, and maintainable software systems. Misusing inheritance can lead to poor code. That happens when design principles are used improperly, creating more problems than they are meant to solve. 

So how do we know if we're abusing inheritance? Well, there are a few points to be aware of when implying inheritance. 

1. First, you need to ask yourself, am I using inheritance to simply share attributes or behavior without further adding anything special in my subclasses? If the answer is yes, then you're misusing inheritance. This is an indication of misuse, because there is no point for the subclasses to exists since the superclass already is enough. 

2. The second indication of improper use of generalization is, if you break the Liskov Substitution Principle. The principle states that ***a subclass can replace a superclass, if and only if, the subclass does not change the functionality of the superclass.*** 

Let's take a look at this example. This is our generalized Animal class, it knows how to eat, walk, and run. Are you able to see how we can introduce a subclass that would break the Liskov Substitution Principle? What if we had this type of animal? 

![[Pasted image 20230310180028.png]]

![[Pasted image 20230310180127.png]]

A whale doesn't know how to run and walk. Running and walking are behaviors of land animals. The Liskov Substitution Principle is violated here, because the whale class overrides the animals classes running and walking functions and replaces them with swimming behaviors. The whale no longer behaves in the way we would expect it superclass to behave. 

An example of bad inheritance can be seen in the Java Collections Library. Have you ever used the stack class in Java? A stack is understood as first in and last out data structure. It has a small number of well defined behaviors like peak, pop and push. This is not the case in the Java stack class, because the stack class inherits from the vector class. This means that the stack class is able to return an element at a specified index, retrieve the index of an element and even insert an element into a specific index. These are not behaviors expected from a stack, but because of poor use of inheritance, they are allowed in Java. 

***

If inheritance does not suit your need, consider whether decomposition is more appropriate. A smartphone is a good example of where decomposition works better than inheritance. A smartphone has characteristics of a phone and a camera. Here is one design. 

It does not make sense for us to Inherit from the phone and then add camera methods to the subclass smartphone. We should be using decomposition to extract out the camera responsibilities, and put them in their own class. 

![[Pasted image 20230310181234.png]]

The smartphone now indirectly provides the responsibilities of the camera in the phone. To separate part classes, the smartphone doesn't need to know how these classes work. 

Inheritance could be a difficult design principle to apply, but it is still a very powerful technique. Inheritance lets you define some classes that are tailor made for your system, while defining common attributes and behaviors in the superclass. Remember, that a common goal is to build reusable, flexible, and maintainable systems. Inheritance is simply one technique to help you reach that goal. It is important to understand that a technique is beneficial when used properly, but can cause headaches if not. 