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

***Composition*** is an exclusive containment of parts, otherwise known as a strong has-a relationship. What this means is that the whole cannot exist without its parts. If loses any of its parts, the whole ceases to exist. If the whole is destroyed, then all of its parts are destroyed too. Usually, you can only access the parts through its whole. Contained parts are exclusive to the whole. Compare this to the relationship between a house and a room. A house is made up of multiple rooms. However, if you were to remove the house, its rooms would cease to exist. You cannot have a room without its house. 

![[Pasted image 20230301165720.png]]

Let's examine a composition relationship using UML. This UML class diagram describes the relationship between a house and a room, that a house object has one or more room objects. The filled in diamond next to the house means that the house is the whole in the relationship. If the diamond is filled in, it means that has-a relationship is strong. The two related objects cannot exist without each other. The ***filled diamond*** denotes the relationship is composition. 

![[Pasted image 20230301170010.png]]

Here is an example of composition using Java. In this example, the brain is created at the same time that the human object is. The brain does not need to be instantiated anywhere else, nor does it need to be passed into the human object on creation. The brain is automatically created with the human. The two parts, human and brain, are tightly dependent with one not being able to exist without the other. 

## Generalization with Inheritance in Java and UML

![[Pasted image 20230301173526.png]]

Like the other design principles, UML will let you model generalization and inheritance of the classes in your system. Showing inheritance is very simple in a UML class diagram. You simply connect two classes with a solid lined arrow. This indicates, that two classes are connected by inheritance. The superclass is at the head of the arrow, and the subclass is at the tail. The standard way to draw inheritance into your UML diagrams, is to have the arrow pointing upward. This means that the superclasses are always toward the top, and the subclasses are always toward the bottom.

## Generalization with Interfaces in Java and UML