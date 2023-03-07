## Coupling and Cohesion

The metrics you will use to evaluate design complexity are ***coupling*** and ***cohesion***. ***Coupling*** focuses on complexity between a module and other modules. ***Cohesion*** focuses on complexity within a module. These two ideas will help you to better apply object-oriented design principles and achieve a more manageable system. When you design your system, you combine various modules together. Think of a bad design like ***puzzle pieces***, where your modules are the pieces. You can only connect a puzzle piece to another specific puzzle piece and nothing else. On the other hand, let's think of a well-designed system like ***Lego blocks***. You can connect any two Lego blocks without much trouble, and all Lego blocks are compatible with one another. When designing your system, you want to make it like Lego. That way, you can easily connect and reuse modules together. 

### Coupling

***Coupling*** for a module captures the complexity of connecting the module to other modules. If your module is highly reliant on other modules, you would say this module is tightly coupled to others. This is like having ***puzzle pieces***. 

On the other hand, if your module finds it easy to connect to other modules, this module is loosely coupled to others. This is like ***Lego***. You want coupling for your module to be loose or low, not tight. 

When evaluating the coupling of a module, you need to consider ***degree***, ***ease***, and ***flexibility***. 

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