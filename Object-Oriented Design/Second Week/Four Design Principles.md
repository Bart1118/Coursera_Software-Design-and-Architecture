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



## Generalization
  
