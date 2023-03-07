## Abstraction in Java and UML

A UML Class Diagram, or just Class Diagram for short, allows you to represent your design in more detail than CRC cards can but it's still visual. Class Diagrams are much closer to the implementation and can easily be converted to classes in code. Abstraction, which you may recall, is the idea of simplifying a concept in the problem domain to its essentials within some context. Abstraction allows you to better understand a concept by breaking it down into a simplified description that ignores unimportant details. You can first apply abstraction at the design level using UML Class Diagrams then eventually convert the design into code.

![[Pasted image 20230301171054.png]]
<center>CRC Card</center>

Now, if we compare the CRC card to our Class Diagram, you might notice how some of the responsibilities on the card turned into properties in the Class Diagram. 

![[Pasted image 20230301171412.png]]
<center>Class Diagrams</center>

Class Diagrams are very close to implementation, making the translation to Java very easy. Class name in Class Diagram turns into a class in Java. Properties in the Class Diagram turn into member variables. And finally, Operations turn into methods. 

## Encapsulation in Java and UML

Let's take a look at how to apply encapsulation. As you will recall from an earlier lesson on encapsulation, it involves three ideas. First, you bundle data, and functions that manipulate the data, into a self-contained object. Second, you can expose certain data and functions of that object, which can be accessed from other objects. Third, you can restrict access to certain data and functions to only within that object. 

![[Pasted image 20230301171528.png]]
<center>Student Class Diagrams</center>

If you are creating a system that models a university student using encapsulation, you would have all of the student's relevant data defined in attributes of a student class. You would also need specific public methods that access the attributes. In this example, our student's relevant data could be their degree program and GPA. This would be the UML class diagram for the student class. The student class has its attributes hidden from public accessibility. This is denoted by the minus signs before GPA and degree program. These minus signs indicate that a method or attribute is private. Private attributes can only be accessed from within the class. 

Outside this class, instead of being able to directly manipulate the student's GPA attribute, you must set the GPA through a public method setGPA. By only allowing an object's data to be manipulated via a public method, you can control how and when that data is accessed. This control of data is like creating a gate. You only let access to data you allow. With every piece of essential data, you need to create a protective layer from unapproved manipulation.

![[Pasted image 20230301171722.png]]

***Getter*** Methods are methods that retrieve data, and their names typically begin with get and end with the name of the attribute whose value you will be returning. Getters often retrieve a private piece of data. 

![[Pasted image 20230301171736.png]]

***Setter*** Methods change data, and their names typically begin with set and end with the name of the variable you wish to set. Setters are used to set a private attribute in a safe way. 

Data integrity is why you have Getter and Setter Methods.

Outside classes do not care how your methods are implemented. They only care if the methods are returning the expected output or doing their expected responsibility. This means your Getters and Setters do not purely have to return and change private attribute values. They can do more. 

![[Pasted image 20230301171820.png]]

The outside observer does not need to know how your public methods are implemented. Just that they perform as expected. That means you can add additional code to your Getters and Setters if you need to. Overall encapsulation is meant to protect your class and its objects. It also allows for an interface of approved methods for other classes to safely use the class. It allows you to hide implementation details from other classes. 

## Decomposition in Java and UML

Our definition of decomposition is taking a whole thing and dividing it up into different parts. Or, on the flip side, taking a bunch of separate parts with different functionalities and combining them together to form a whole.

There are three types of relationships found in decomposition, ***association***, ***aggregation***, and ***composition***. They define the interaction between the whole and the parts.

***

The first decomposition relationship is ***association***. Association is some relationship. This means that there is a loose relationship between two objects. These objects may interact with each other for some time. For example, an object of a class may use services/methods provided by object of another class. This is like the relationship between person and airline. A person does not generally own an airline, but can interact with one. An airline can also interact with many person objects. There are some persons and some airlines, neither is dependent on the other. 

![[Pasted image 20230301163854.png]]

Let's take a look at what an association relationship looks like using UML class diagram notation. It is helpful to read UML diagrams which each box being called an object. This UML examines the relationship I described between person and airline. The ***straight*** line between two UML objects denotes that the relationship between them is an association. You can see that there is a 0..* found on both sides of the relationship. This means a person object is associated with zero or more airline objects. And an airline object is associated with zero or more person objects. 

The association in this question is between food and wine, students and sports, and kitten and yarn. Each of these relationships is between completely separate entities. If one object is destroyed, the other can continue to exist, unlike human and organ. There can be any number of each item in the relationship. One object does not belong to another.

![[Pasted image 20230301164423.png]]

Now we will look at an association example in code. In this code excerpt, the student is passed a sport object to play. The student does not possess the sport beyond playing it. The relationship is between two completely separate objects. A student can play any number of sports. And any number of students can play a sport. Now it's your turn to come up with some code displaying an association. 

***

***Aggregation*** is a has-a relationship where a whole has parts that belong to it. There may be sharing of parts among the wholes in this relationship. The has-a relationship from the whole to the parts is considered weak. What this means is although parts can belong to the wholes, they can also exist independently. This is like the relationship between an airliner and its crew. An important part of the airliner is its crew. Without the crew, an airliner would not be able to fly. However, the airliner does not cease to exist if there is no crew on board. Same goes for the crew, they are part of the operation of the airliner but the crew does not cease to exist or become destroyed if they are not on board their airliner. These entities have a relationship, but can exist outside of it.

![[Pasted image 20230301163928.png]]

Let's take a look at this example of aggregation using a UML class diagram. This UML class diagram describes the relationship I explained above between airliner and crew. It says that for an airliner object, it has zero or more crew members. Also, a crew member object can be had by zero or more airline objects. The empty diamond denotes which object is considered the whole and not the part in the relationship. This ***empty diamond*** is the symbol for aggregation. The aggregation we can see is between course section and students, pet stores and pets, and bookshelf and books. Each of these are a ***has-a*** relationship. A course has students, students have courses, and so on. But the relationship is weak. If one of the objects in the relationship is destroyed, it still makes sense that the other can continue to exist.

![[Pasted image 20230301164836.png]]

Now I will show a code example for aggregation. In the airliner class, there is a list of crew members. The list of crew members is initialized to be empty. And a public method allows new crew members to be added. The airliner has a crew. This means that an airliner can have zero or more crew members.

***

***Composition*** is an exclusive containment of parts, otherwise known as a ***strong has-a*** relationship. What this means is that the whole cannot exist without its parts. If loses any of its parts, the whole ceases to exist. If the whole is destroyed, then all of its parts are destroyed too. Usually, you can only access the parts through its whole. Contained parts are exclusive to the whole. Compare this to the relationship between a house and a room. A house is made up of multiple rooms. However, if you were to remove the house, its rooms would cease to exist. You cannot have a room without its house. 

![[Pasted image 20230301165720.png]]

Let's examine a composition relationship using UML. This UML class diagram describes the relationship between a house and a room, that a house object has one or more room objects. The filled in diamond next to the house means that the house is the whole in the relationship. If the diamond is filled in, it means that has-a relationship is strong. The two related objects cannot exist without each other. The ***filled diamond*** denotes the relationship is composition. 

![[Pasted image 20230301170010.png]]

Here is an example of composition using Java. In this example, the brain is created at the same time that the human object is. The brain does not need to be instantiated anywhere else, nor does it need to be passed into the human object on creation. The brain is automatically created with the human. The two parts, human and brain, are tightly dependent with one not being able to exist without the other. 

## Generalization with Inheritance in Java and UML

![[Pasted image 20230301173526.png]]

Like the other design principles, UML will let you model generalization and inheritance of the classes in your system. Showing inheritance is very simple in a UML class diagram. You simply connect two classes with a solid lined arrow. This indicates, that two classes are connected by inheritance. The superclass is at the head of the arrow, and the subclass is at the tail. The standard way to draw inheritance into your UML diagrams, is to have the arrow pointing upward. This means that the superclasses are always toward the top, and the subclasses are always toward the bottom.

![[Pasted image 20230301174127.png]]

So a simple inheritance in a UML diagram would have this layout. ***You do not need to put any of the inherited superclasses attributes and behaviors into the subclass.*** The arrow is used to communicate inheritance, which implies that the subclass will have the superclasses attributes and methods. The superclasses are the generalized classes, and the subclasses are the specialized classes. 

![[Pasted image 20230301174522.png]]

A UML class diagram describes a dog class as a subclass, and the Animal class as the superclass. This means that the dog class will inherit from the Animal class. The ***hash symbol*** is used to communicate that the animals attributes are ***protected***. 

In Java, a protected attribute or method can only be accessed by, the encapsulating class itself, all subclasses, all classes within the same package. In Java, a package is simply a means in which the classes can be organized into a namespace that represents those classes.

We know that a subclass will have all attributes and behaviors of the superclass that it inherits from. So we do not need to put the superclass's attributes and behaviors in the subclass in our UML diagram. This is because the inheritance notation tells us that the subclass will already have the attributes and behaviors listed in the superclass.

![[Pasted image 20230301175101.png]]

Now, let's convert the UML model into code for the animal and dog classes, so that we can create Doug from it. Since an animal is a generalization of specific species, we do not want to be able to create an animal object on its own. We use the keyword abstract to declare that this class cannot be instantiated. That means that we cannot create an animal object. 

![[Pasted image 20230301175510.png]]

The Animal class will be the superclass for our dogs subclass, any class that inherits from the Animal class will have its attributes and behaviors. This means that if we were to introduce a cat subclass into our system that inherited from the Animal class, the cat and dog subclasses would both have the same attributes and behaviors as the animal superclass. As you would expect, we do not need to declare any of the attributes and behaviors that the dog class inherits from the Animal class. 

Notice that our code and UML diagram are similar in terms of what attributes and methods are declared in the superclass and subclass. The UML class diagram represents our design. If we do not need to restate the inherited attributes and behaviors in the code, then we also do not need to do it in our UML diagram. 

We declare inheritance in Java using the keyword "extends". 

You instantiate objects from a class by using constructors. With inheritance, if you want an instance of a subclass, you need to give the superclass a chance to prepare the attributes for the object appropriately. 

Classes can have implicit constructors or explicit constructors. 

![[Pasted image 20230301175913.png]]

In this implementation of the Animal class, we have an implicit constructor, since we have not written our own constructor. All attributes are assigned zero or null, when using the default constructor. 

![[Pasted image 20230301180031.png]]

The Animal class in this implementation, has an explicit constructor that will let us instantiate an animal with however many legs we want. Explicit constructors, are use of that we can assign values to attributes during instantiation. 

A subclass's constructor ***must call*** its superclass's constructor, if the superclass has an explicit constructor. This is because explicit constructors of the superclass must be referenced by the subclass. Otherwise the superclass attributes would not be appropriately initialized.

![[Pasted image 20230301180259.png]]

In order to access the superclass's attributes, methods and constructors, the subclass uses the keyword called Super.

![[Pasted image 20230301180440.png]]

Subclasses can override the methods of its superclass, meaning that a subclass can provide its own implementation for an inherited superclass's method. The dog class has overwritten the animal class's walk method. If we were to ask the dog to walk, it would tell us that it would rather lay on the couch instead of performing the behavior implemented in the Animal class.

![[Pasted image 20230301180856.png]]

For Java, only single implementation inheritance is allowed. Well a superclass can have multiple subclasses. A subclass can only inherit from one superclass. For example, the dog and cat subclasses can each only have implementation inheritance with one superclass, which is animal. The animal superclass however, can have any number of subclasses, two in this example.

![[Pasted image 20230301181004.png]]

To implement this in code, we simply have the cat and dog classes extend the Animal class. Now we have a cat and a dog that behave like an animal without having to explicitly write code for them. They also have their own behaviors. 

Note, that a subclass itself can be a superclass to another class. Inheritance can trickle down through as many classes as you want. 

Inheritance will let you generalize related classes into a single superclass and still allow the subclasses to retain the same set of attributes and behaviors. This will help remove redundancy in your code, and make it easier to implement changes. 

## Generalization with Interfaces in Java and UML

A JAVA interface also denotes a type. Unlike a class, however, an interface only declares method signatures, and no constructors, attributes, or method bodies. It specifies the expected behaviors in the method signatures, but does not provide any implementation details. 

In JAVA, an interface is also used for subtyping. If a dog class implements an I animal interface, then a dog object behaves not only like a dog, but it is also expected to behave like an animal by providing all the method bodies for the method signatures listed in the interface. Just like with inheritance, the dog is an animal. However, the difference is that the dog class needs to provide the implementation details for what it means to be an animal. ***So, an interface is like a contract to be fulfilled by implementing classes.*** 

In both inheritance and interfaces, you achieve consistency between the dog type and the animal type so that a dog object is usable anywhere in your program when you are dealing with an animal type. 

Unlike inheritance, interfaces are not a generalization of a set of classes. It is important to understand that interfaces are not classes. They are used to describe behaviors. All that an interface contains are method signatures. 

In JAVA, we use the key word interface to indicate that we are creating one. Standard JAVA naming convention places the letter I before an actual name to indicate an interface. 

![[Pasted image 20230301183723.png]]

This interface describes three different behaviors of an animal, which are moving, speaking, and eating. Notice how we never implement or describe how these behaviors are performed. We only show that an animal has these behaviors. Another thing you might have noticed is that the interface does not encapsulate any of the attributes of an animal. This is because attributes are not behaviors. 

![[Pasted image 20230301183931.png]]

We need to declare that we are going to fulfill the contract as described in the interface. The keyword in JAVA for this action is implements. Our dog class has declared that it will implement or describe the behaviors that are in the interface. When you do this, you must have ***all*** the method signatures explicitly declared and implemented in the class. This means that we must the move, speak, and eat methods in this class. 

![[Pasted image 20230301184244.png]]

Interfaces are drawn in a similar way that classes are drawn in UMLs. Interfaces are explicitly noted in UML class diagrams using guillemets, or French quotes, to surround the words interface. 

![[Pasted image 20230301184533.png]]

The interaction between an interface and a class that is implementing the interface is indicated using a ***dotted arrow***. The class touches the tail end of the arrow and the interface touches the head of the arrow. We combine these notations together with a class to show that a class implements an interface. This indicates that the class implements the interface. The standard way to draw interfaces on your UML class diagrams is to have the arrow pointing upward. This means that the interface is always toward the top, and the classes that implement them are always toward the bottom. 

If we translate the JAVA code to UML, the diagram for our animal interface example looks like this.

![[Pasted image 20230301185517.png]]

This UML class diagram tells us that the Dog class will determine how the behavior that is described in the interface IAnimal will be implemented by repeating the method signature. 

There are several advantages for interfaces. Knowing and understanding what these advantages are will help you to determine if you should use interfaces or use inheritance when you are designing your systems. 

Like abstract classes, which are classes that cannot be instantiated, interfaces are a means in which you can implement ***polymorphism***. In object oriented languages, polymorphism is when two classes have the same description of a behavior, but the implementations of the behavior may be different. This can be seen when we compare a cat and a dog. How would you describe how each of these animals speak? Well, to simply put it, a cat meows and a dog barks. The description of the behavior is the same, both animals can speak. But the actual behavior implementation itself is different. This is known as polymorphism. It is simple to achieve in JAVA using an interface. 

![[Pasted image 20230301185955.png]]

We create our interface the same way as we did before. 

![[Pasted image 20230301190105.png]]

The Cat and Dog class both implement the IAnimal interface, but they each have their own versions of the speak behavior. When we ask Doug the Dog to speak, he knows how to bark, but will not know how to meow like Mittens the Cat. 

Just like with class inheritance, interfaces can inherit from other interfaces. And just like with class inheritance, interface inheritance should not be abused. This means that you should not be extending interfaces if you are simply trying to create a larger interface. Interface A should only inherit from interface B if the behaviors in interface A can fully be used as a substitution for interface B. 

A little confused? This example should clear things up. 

![[Pasted image 20230301190305.png]]

Lets simplify the movement of a vehicle by restricting it s movement so that it can only travel along either the x-axis or y-axis. This interface can be used to describe the behaviors of vehicles on land or on water. 

But what if we need to implement the movement of a plane or a submarine that can also move in the zed-axis? We do not want to add an extra behavior to the interface, because on-land and on-water vehicles do not move along the zed-axis. So what do we do? We can create a second interface that will inherit from our first one. 

![[Pasted image 20230301190423.png]]

Now, we can use the IVehicleMovement3D interface for all vehicles that have three-dimensional movement without having to add the Zed-axis movement to the interface used by the on-land and on-water vehicles. 

***

To understand the next advantage of interfaces, we need to step back to inheritance. There is one other form of inheritance that we haven't looked at called multiple inheritance. This is when a subclass has two or more super classes. While this is possible to do with other object oriented languages, like C++, JAVA doesn't support ***Multiple Inheritance***. 

In JAVA, a class can implement as many interfaces as we want. This is because of the nature of interfaces. Since they are only contracts and do not enforce a specific way to complete these contracts, overlapping method signatures are not a problem. 

![[Pasted image 20230301191455.png]]

A single implementation for multiple interfaces with overlapping contracts is acceptable. There is no ambiguity here because the Person class only has one definition of a speak method, and it is the same implementation for both interfaces. This is JAVA's approach to avoid the issue that is introduced with multiple inheritance. 

![[Pasted image 20230301191725.png]]

Just like with other constructs in object oriented modeling and programming, interfaces will help you to create programs with reusable and flexible code. Although they are a useful technique, remember that you should not be generalizing all behavior contracts into interfaces. They are meant to fulfill a specific need, which is to provide a way for related classes to work consistently. 