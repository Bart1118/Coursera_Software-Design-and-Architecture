## Coupling and Cohesion

The metrics you will use to evaluate design complexity are ***coupling*** and ***cohesion***. ***Coupling*** focuses on complexity between a module and other modules. ***Cohesion*** focuses on complexity within a module. These two ideas will help you to better apply object-oriented design principles and achieve a more manageable system. When you design your system, you combine various modules together. Think of a bad design like ***puzzle pieces***, where your modules are the pieces. You can only connect a puzzle piece to another specific puzzle piece and nothing else. On the other hand, let's think of a well-designed system like ***Lego blocks***. You can connect any two Lego blocks without much trouble, and all Lego blocks are compatible with one another. When designing your system, you want to make it like Lego. That way, you can easily connect and reuse modules together. 

***

### Coupling

***Coupling*** for a module captures the complexity of connecting the module to other modules. If your module is highly reliant on other modules, you would say this module is tightly coupled to others. This is like having ***puzzle pieces***. 

On the other hand, if your module finds it easy to connect to other modules, this module is loosely coupled to others. This is like ***Lego***. You want coupling for your module to be loose or low, not tight. 

When evaluating the coupling of a module, you need to consider ***degree***, ***ease***, and ***flexibility***. 

***

***Degree*** is the number of connections between the module and others. With coupling, you want to keep the degree small. For instance, if the module needed to connect to other modules through a few parameters or narrow interfaces, then degree would be small and coupling would be loose. 

***Ease*** is how obvious are the connections between the module and others. With coupling, you want the connections to be easy to make without needing to understand the implementations of the other modules. 

***Flexibility*** is how interchangeable the other modules are for this module. With coupling, you want the other modules easily replaceable for something better in the future. 

Again, like Lego. Coupling only concerns complexity between a module and other modules, but you also need to consider complexity within the module. That's where you would look at ***cohesion***. 

***

### Cohesion

***Cohesion*** represents the clarity of the responsibilities of a module. If your module performs one task and nothing else or has a clear purpose, your module has ***high cohesion***. 

On the other hand, if your module tries to encapsulate more than one purpose or has an unclear purpose, your module has ***low cohesion***. 

***

Suppose we have a class called sensor that has two purposes, getting humidity and getting temperature sensor readings. Here we have a get method that takes a zero flag if you wanted to return the humidity value, and takes the one flag if you want it to return the temperature value. 

![[Pasted image 20230307152641.png]]

Since the sensor class doesn't have a clear single purpose, it suffers from low cohesion. 

![[Pasted image 20230307152825.png]]

Since it is unclear what control flag means, we would have to read inside the method itself in order to know what values to give it. This is not respecting encapsulation which also shows our method is unclear and lacks ease. This lack of ease makes get method harder to use and in turn makes any caller tightly coupled to it. 

![[Pasted image 20230307153526.png]]

Let's look at a new design of the same system. The sensor class is now replaced with a humidity sensor glass and the temperature sensor class. 

Each of these classes has one clearly defined purpose. Since each has a clear purpose, you can say that these classes are highly cohesive. 

The get method is now not hiding any information like before. We don't have to break encapsulation to look inside the method. You could reasonably assume that humidity sensors get method returns humidity and temperature sensors get method returns temperature. This makes another module that uses either be loosely couple. 

## Separation of Concerns

One goal of software design principles is to help us create a system that is flexible, reusable and maintainable. One of these principles is called separation of concerns. So, what is a concern? 

A concern is a very general notion, basically it is anything that matters in providing a solution to a problem. Let's think of a supermarket, the concerns in a supermarket could be, how do I butcher meat? How do I bake bread, how do I accept payment? And how do I stock the shelves? These concerns matter when running the business to serve their customers. 

But, what do you notice in how a supermarket is organized to deal with these concerns? There are separate departments that focus on each concern. Each concern poses unique sub-problems. And each department knows what to do and how to address their specific concerns. The organization of a supermarket applies separation of concerns. 

A software system solves a problem in a similar fashion. The problem might be complex with a large number of concerns. Or it might be simple with the small number of concerns. There are concepts that can be abstracted from the problem space. How these abstractions are implemented in the software can lead to more concerns. Some of these concerns may involve what information the implementation represents, what it manipulates, and what gets presented at the end. 

It's easy to get lost and tangled up in all these concerns and their sub-problems. We need to be organized, so that we can think about and address these concerns effectively. As a software solution is designed and constructed, we express how we can address the different sub-problems by separating them into separate sections. 

You might have noticed, that separation of concerns, is a key idea that applies throughout object oriented modelling and programming. The concerns that matter are addressed separately when applying the design principles of abstraction, encapsulation, decomposition, and generalization. 

Each concept in the problem space leads to a separate ***abstraction*** with its own relevant attributes and behaviors. These attributes and behaviors are ***encapsulated*** into their own section of code called a class. The view of a class by the rest of the system and its implementation are separated. So that the details of implementation can change, while the view through an interface can stay the same. A whole class can also be ***decomposed*** into multiple classes. We may recognize commonalities among classes, which are then separated and ***generalized*** into a super class. Separation of concerns is an ongoing process throughout the design process. 

***

![[Pasted image 20230308152947.png]]

Let's illustrate some operation of concerns with an example. In this snippet of code, the SmartPhone class, has attributes called camera and phone along with all of the associated behaviors. However, there is low cohesion in the SmartPhone class, because we have behaviors that are not related to each other. The camera behaviors do not need to be encapsulated with the behaviors of the phone in order for the camera to do its job. 

Furthermore our smartphone components do not offer us any modularity. We cannot access the camera or the phone separately if we were to build another system that required only one or the other. We cannot replace our current camera with a different camera, or replace it with a completely different object, without removing the code for the camera completely in this class. 

So what changes can we make to our SmartPhone class in order to make it more cohesive, and give each component of our smartphone distinctive functionalities. Well, let's check what our smartphone class is concerned about and separate them out. Our SmartPhone class has ***two concerns***. One, act as a ***traditional telephone**, and two, be able to use the ***built-in camera*** to take pictures. Now that we have identified these two different concerns, we can separate them out into their own more cohesive classes and encapsulate all the details about each into functionally distinct and independent classes. 

The SmartPhone class will reference ***instances*** of our newly created classes, so that the smartphone can act as a coordinator of the camera and the phone. This will let our smartphone provide access to all the behaviors of the camera and the phone without having to know how each component behaves. 

Let's now take a look at what our new smartphone design looks like after we applied separation of concerns. 

![[Pasted image 20230308154623.png]]

First, we will extract the attributes and behaviors of both the camera and TraditionalPhone into two separate interfaces. Then, we can implement these interfaces correspondingly with the FirstGenCamera class and the TraditionalPhone class. Here is what the code looks like. 

![[Pasted image 20230308154812.png]]

As you can see, we have separated the camera and phone functionalities into different classes, each of which implements a certain interface. 

![[Pasted image 20230308154911.png]]

Next, let's redesign the code for our SmartPhone class, so that it refers to instances of the camera and phone classes. 

This allows our smartphone to provide the functions of both the camera and the phone, while keeping the functionalities of either one separate and hidden from each other. The camera and phone know nothing about the other but are still composed by this SmartPhone class. 

Also, we can have a smartphone constructor with camera and phone as parameters. Then we can create a new instance of the SmartPhone class by passing in a instances of classes that implemented the camera and phone interfaces. Note that we leave it as a separate responsibility of who will instantiate the appropriate phone and camera objects. The smartphone class does not actually need to know. Finally, the smartphone class has methods that forward the responsibilities of using the camera and phone to these objects. 

We use separation of concerns throughout this example by separating out the general notions of camera and phone through applying ***generalization*** and defining two ***interfaces***. Separating out the functionality for a first gen camera and traditional phone by applying ***abstraction*** and ***encapsulation***, and defining two ***implementing classes***. And finally, by applying ***decomposition*** to the smartphone, so the constituent parts are separated from the whole. 

![[Pasted image 20230308161335.png]]

Our goal is to create flexible reusable, and maintainable code. Separation of concerns creates more cohesive classes using ***abstraction***, ***encapsulation***, ***decomposition***, and ***generalization***. This creates a system that is easier to maintain because each class is organized so that it only contains the code that it needs to do its job. Modularity is increased in turn, which allows developers to reuse and build up individual classes without affecting others. In our smartphone example, it is clear where the boundaries of each class are. 

However, real-world problems may not be so obvious. Deciding how to ***abstract***, ***encapsulate***, ***decompose*** and ***generalize*** to address the many concerns for a given problem is at the core of designing modular software. 

