## Abstraction

abstraction is one of the main ways that humans deal with complexity. Abstraction is the idea of simplifying a ***concept*** in the problem domain to its essentials within some ***context***. Abstraction allows you to better understand a concept by breaking it down into a simplified description that ignores unimportant details 

Abstraction is the idea of simplifying a concept in the problem domain to its essentials within some context. Good abstraction emphasizes the essentials needed for the concept and removes details that are not essential. Also an abstraction for a concept should make sense for the concept's purpose.

In object oriented modeling, abstraction pertains most directly to the notion of a class. When you use abstraction to decide the essential characteristics for some concept, it makes the most sense to define all of those details in a class named after the concept. A class is like a template for instances of a concept. An object instantiated from a class then has the essential details to represent an instance of some concept. 

Overall, abstraction is an important principle you use when solving problems and designing your systems. Some of its benefits are simplifying your class design so they are more focused, succinct and understandable to someone else viewing them. As you have learned though, abstractions are formed within a specific context for perspective and you have to carefully decide what is relevant. If the purpose of your system or the problem changes, don't be afraid to update your abstractions accordingly. Abstractions are not a fixed creation, but are a direct result of the problem for which you created them.

## Encapsulation

Encapsulation involves three ideas. As the name suggests, it's about making a sort of capsule. The capsule contains something inside, some of which you can access from the outside, and some of which you cannot. 

***First***, you bundle attribute values or data, and behaviors or functions, that manipulate those values together into a self-contained object. ***Second***, you can expose certain data and functions of that object, which can be accessed from other objects. ***Third***, you can restrict access to certain data and functions to only within that object. 

In short, encapsulation forms a self-contained object by bundling the data and functions it requires to work, exposes an interface whereby other objects can access and use it, and restricts access to certain inside details.

Encapsulation helps with software changes. The accessible interface of a class can remain the same, while the implementation of the attributes and methods can change. Outsiders using the class, do not need to care how the implementation actually works behind the interface. 

In programming, this sort of thinking is commonly referred to as, Black Box Thinking. Think of a class like a black box that you cannot see inside for details about, how attributes are represented, or how methods compute the result, but you provide inputs and obtain outputs by calling methods. It doesn't matter what happens in the box to achieve the expected behaviors. This distinction between what the outside world sees of a class, and how it works internally is important. Encapsulation achieves what is called, the Abstraction Barrier. Since the internal workings are not relevant to the outside world, this achieves an abstraction that effectively reduces complexity for the users of a class. This increases re-usability, because another class only needs to know the right method to call to get the desired behavior, what arguments to supply as inputs, and what appear as outputs or effects.

## Decomposition

Decomposition is taking a whole thing and dividing it up into different parts. Or, on the flip side taking a bunch of separate parts with different functionalities, and combining them together to form a whole. Decomposition allows you to further break down problems into pieces that are easier to understand and solve.

Since decomposition allows you to create clearly defined parts, it is quite natural that these parts are separate. A whole might have a fixed or dynamic number of a certain type of part. If there is a fixed number, then over the lifetime of the whole object it will have exactly that much of the part object. For example, a refrigerator has a fixed number of freezers, just one. This does not change over time, but there are sometimes parts with a dynamic number. Meaning, the whole object may gain new instances of those part objects over its lifetime. For example, a refrigerator can have a dynamic number of shelves or food items over time.

A part itself can also serve as a whole containing further constituent parts. When you look at our refrigerator example, a drawer can contain fruit.  

One issue in decomposition involves the lifetimes of the whole object, and the part objects, and how they could relate. Lifetimes might be closely related. For example, the refrigerator and its freezer have the same lifetime. One cannot exist by itself without the other. If you dispose off the refrigerator, you would dispose off the freezer as well. But lifetime can also not be so related. The refrigerator and food items have different lifetimes. Either can exist independently.

You can have whole things contain parts that are shared among them at the same time. 

Overall, decomposition helps you to break down a problem into smaller pieces. A complicated whole thing can be composed out of constituent, separate, simpler parts. Important issues to understand are how the parts relate to the whole, such as fixed or dynamic number, their lifetimes, and whether there is sharing.

## Generalization
  
One design principle called generalization, helps us to reduce the amount of redundancy when solving problems. Many behaviors and systems in the real world operate through repetitious actions. We can model behaviors using methods. It lets us generalize behaviors and it eliminates the need to have identical code written throughout a program. Methods are a way of applying the same behavior to a different set of data. 

Generalization is frequently used when designing algorithms, which are meant to be used to perform the same action on different sets of data. We can generalize the actions into its own method, and simply pass it through a different set of data through arguments. 

Generalization happens to be one of the main design principles of object-oriented modeling and programming. But it's achieved differently than what we've just seen with methods. 

Generalization can be achieved by classes through inheritance. In generalization we take repeated, common, or shared characteristics between two or more classes and factor them out into another class. Specifically, you can have two classes, a parent class and a child class. When a child class inherits from a parent class, the child class will have the attributes and behaviors of the parent class. You place common attribute and behaviors in your parent class. There can be multiple child classes that inherit from a parent class, and they all will receive these common attributes and behaviors. The child classes can also have additional attributes and behaviors, which allow them to be more specialized in what they can do. In standard terminology, a parent class is known as a superclass and a child class is called the subclass. 

Inheritance and methods exemplify the generalization design principle. There are techniques that left us apply a rule called D.R.Y., which stands for Don't Repeat Yourself. We can write programs that are capable of performing the same tasks but with less code.