## UML Sequence Diagram

Sequence Diagrams are used to show your team how objects in your program interact with each other to complete tasks. 

Simply put, think of a sequence diagram like a map of conversations between different people, where this map follows all the messages sent from person to person. 


Let's say that a person wants to order a burger at a local fast food restaurant, here is a simple sequence diagram of the scenario. 

![[Pasted image 20230310190858.png]]

That person will go to a restaurant and talk to the cashier and order a burger. 

The cashier will then talk to the chef of the back to tell him my order. 

The shuffle cook the burger, give it to the cashier. 

And the cashier will give it to the person. 

Now, let's go into more detail, because a sequence diagram is another type of UML diagram, to fully understand it, you should have a good grasp of objects and basic UML class diagrams. Knowing how to break down a system into classes is essential in creating meaningful sequence diagrams. 

A sequence diagram describes how objects in your system interact to complete a specific task. 

![[Pasted image 20230310192610.png]]

When creating sequence diagrams, first you use a ***box*** to represent role play by an object. The role is typically labeled by the name of the class for the object. 

![[Pasted image 20230310193223.png]]

Second, you use ***vertical dotted lines***, known as ***lifelines***, to represent an object as time passes by. 

![[Pasted image 20230310193249.png]]

Finally, you use ***arrows*** to show messages that are sent from one object to another. 

***

Now that you know the different elements, let's put everything together by creating a sequence diagram. Let's use changing the channel of your television using a remote control. 

First, I'm going start by drawing a box, that will surround the entire process. This is to show that this is one sequence of activities. 

![[Pasted image 20230310194703.png]]

A sequence diagram can contain other sequence diagrams within it. For example, if you are creating a sequence diagram for an ATM, there might be a different sequence for Withdrawal and Deposits. And during a single process someone might want to do both. In your sequence diagram, you would have one big sequence of activities with two smaller sequences inside them. 

![[Pasted image 20230310194926.png]]

Moving on, in the top corner I'm going to draw a label with a meaningful title. Remember, your team will be looking at this diagram as a reference for development, so make the titles meaningful. We will name it Change TV Channel. Next, I'm going to draw out the objects that are important in this task. 

![[Pasted image 20230310195041.png]]

To keep things clean, you should draw objects from left to right in the sequence that they interact with each other. In this example, the TV viewer starts the entire process. The use of the remote which will then interact with the TV. So when are diagram, I'm going to drive the TV viewer then the remote and then the TV. 

![[Pasted image 20230310195233.png]]

If there are people in your example, who will be using or interacting with objects, this are typically draw on a ***stick figures***. We call these people actors, in our example, the TV viewer's an actor. So I'm going to draw them as a stick figure, I'm going to the other objects as ***labeled boxes***. 

![[Pasted image 20230310195427.png]]

Each of these objects has a lifeline. The lifelines you can draw as a dashed line projecting downwards from the object. 

![[Pasted image 20230310195813.png]]

Now, I'm going to start drawing the messages that are sent from object to object. In a sequence diagram, if one object sends a message to another object or objects, we denote this by drawing a ***solid line arrow*** from the sender to the receiver. 

![[Pasted image 20230310195521.png]]

To return data and to control back to initiating objects, we would use a ***dotted line arrow***. 


What's the first thing that happened in this example? Let's assume the TV is already on and the TV viewer wants to change her channel. The first thing that happens is the TV viewer presses the numbers on the remote to tell it which channel to go to. 

![[Pasted image 20230310200050.png]]

This activates both TV viewer and the remote in our sequence diagram. 

![[Pasted image 20230310200250.png]]

When an object is activated, we denote this on our sequence diagram using ***small rectangles*** on the objects ***lifeline***. 

You activate an object whenever an object sends, receives or it's waiting for a message. 

![[Pasted image 20230310200421.png]]

The first message that is sent is from the TV viewer to the remote. That message says that the TV viewer pressed numbers. So I'm going to add this to the diagram with a solid line arrow and label it Press Numbers (number) . 

![[Pasted image 20230310200637.png]]

The remote then sends a new message to the television to change the channel to number. We denote this on the diagram with another solid line arrow labeled Change channel (number) . 

![[Pasted image 20230310200717.png]]

This also activates the television object, so I will add a small rectangle to the television's lifeline. 

You'll notice that since a television wasn't activated at the beginning of the example, we don't want the rectangle on its lifeline to start at the same place as the TV viewer or the remote. I drew it a little bit lower on the lifeline to indicate it was activated later in the process. 

![[Pasted image 20230310200831.png]]

Next, the television changes the channel, which the TV viewer can see on the TV screen. This is a returning of control. that means I'm going to denote this response using a dotted line arrow. I'm going to draw this arrow from the television object to the TV viewer. This action only affects the television and the TV viewer. The remote is not part of this interaction, so we do not extend the box on the remote's lifeline to include this action. 

As you design software, your sequence diagrams can get much more complicated. You can also show loops and alternative processes in a sequence diagram. 

Let's see what these would look like in a sequence diagram. 

![[Pasted image 20230310201542.png]]

Say the TV viewer is unsure what channel to go to and would like to surf the channels until they find a channel they like. I can wrap the previous sequence I just drew as part of an alternative process. So that it is a sequence of actions that will occur if a condition is true. So I put the sequence in a box and label it ***alt***, for alternative, in the top right corner. 

![[Pasted image 20230310201855.png]]

Now, I need to specify when this alternative will occur. In this case, the sequence occurs if the TV viewer knew what channel they would like. We will label this alternative TV Viewer knows what channel they want. 

![[Pasted image 20230310202416.png]]

If the TV viewer does not know what channel they want, other sequences can occur. One sequence is that the TV viewer will browse to the channels until they find something to watch. So I'm going to drag this sequence underneath the previous sequence with the condition ***else***, meaning this sequence occurs if all other alternatives are false. However, this sequence contains a loop. I will denote that by adding and labeling a box ***loop*** on the top left corner. 

Right under the label, I put a conditional statement for the loop. If that statement is true, it will go through the loop. Loop sequence should continually occur if the TV viewer does not like the channel they are watching, so I will add that condition to this loop box. 

![[Pasted image 20230310202754.png]]

The TV viewer is going to press the up or down arrow on the remote to browse through the channels. This sends a message to the remote. The remote will then send a message to the TV with this action. Just like in the initial sequence, the TV changes the channel and displays that to the TV viewer. The final sequence diagram looks like this. 

Sequence diagrams are a very powerful too you can use to model your software. Sequence diagrams are commonly used as a planning tool before the development team starts programming, or to show others how a system is designed. And they can help you to determine the functions you will need to right. It might even help you find problems in your system that you didn't see before. Sequence diagram are another technique you now know that will help you to create clean, well-designed programs. 

## UML State Diagram

A state diagram is a technique that you can use to describe how your system behaves and responds. State diagrams can describe a single object and illustrate how that object behaves in response to a series of events in your system.

A ***state*** is the way an object exists at a particular point in time. The state of an object is determined by the values of its attributes. 

Using UML state diagrams, you can express the different states of your objects and how the states will change when an event occurs. 

To better understand how to create UML state diagrams, let's actually create one together. Let's use a vending machine as an example for our UML state diagram. 

![[Pasted image 20230320163419.png]]

First, I'll indicate the start of this diagram with a filled circle. Every state diagram has a filled circle to indicate which is the starting state, the vending machine starts in a state named idle. This is when the vending machine is waiting for coins to be inserted. I draw states as rounded rectangles. 

Let me explain states in more detail, each state has three important sections, a ***state name***, ***state variables***, ***and activities***. 

![[Pasted image 20230320163820.png]]

Each state should at least have a state name. A state name is as it sounds, the name of the state, these names should be meaningful for the states of your object. For example, a car in reverse would have a state named reverse. Or a vending machine in a waiting, or idle state, would have a state named idle. State variables are data relevant to the state of the object. For example, using a course as an object, a relevant variable is the number of students enrolled. The course would be in state full, if this variable was at the course capacity. 

![[Pasted image 20230320164051.png]]

Activities are actions that are performed when in a certain state, and they're displayed at the bottom. There are three types of activities for each state, ***entry***, ***exit***, and ***do***. 

- Entry activities are actions that occur when the state is just entered from another state. 

- Exit activities are actions that occur when the state is exited and moves on to another state. 

- And do activities are actions that occur once, or multiple times while the object is in a certain state. 

![[Pasted image 20230320164314.png]]

Now back to our vending machine example. When the vending machine enters this idle state, it always displays the total of coins inserted so far. This means it is also tracking this total. I will draw these inside the rectangle. The state variable is total, and the entry activity will be display total. Inserting a coin is an event that could change the state of the vending machine. 

![[Pasted image 20230320164332.png]]

Events that could change a state label transitions between the states. You draw these transitions with arrows from one state to another. Each transition arrow will always have an event, and may have a guard condition and an action. The transition and action happens from a given state if the event occurs and the condition is true. 

***

![[Pasted image 20230320164709.png]]

Now back to our vending machine example. When the vending machine enters this idle state, it always displays the total of coins inserted so far. This means it is also tracking this total. I will draw these inside the rectangle. The state variable is total, and the entry activity will be display total. 

Inserting a coin is an event that could change the state of the vending machine. Events that could change a state label transitions between the states. You draw these transitions with arrows from one state to another. Each transition arrow will always have an event, and may have a guard condition and an action. 

Again, back to our vending machine. Suppose, when in the idle state, someone inserts a coin and the total so far is less than the product price. Let's express this situation with a transition arrow that loops back to the idle state. With the event insert coin, condition total less than price, and action display insert more coins. 

But suppose when in the idle state, someone inserts a coin and the total equals the product price. Let's express this situation with a transition arrow to a new state, named enough coins. And label this transition with the event, insert coin, and condition, total equals price. Let's have an entry action for enough coins being, display enough coins. 

When in the enough coins state, we have enough payment. So if someone presses the dispense button, the vending machine should release one of the product. We'll express this situation with a transition arrow from the enough coin state back to idle. And label this transition with the event, press dispense, and action, total equals zero, dispense product. 

In either state, if someone press the cancel button, the vending machining should return all the coins inserted. So we'll express this with two transitions from the two states. Both back to the idle state, and label both transitions with an event, press cancel, and action, total equals zero, eject coins. 

![[Pasted image 20230320165417.png]]

One element of state diagrams that's not shown in the one we just created is termination. Termination represents an object being destroyed, or the process being completed, and is drawn as a circle with a filled circle inside. 

For example, when using a bank machine, you can represent it returning your card at the end of the process and thus ending in termination. Not all diagrams have a termination like the vending machine, they may run continuously. 

***

State diagrams are useful for describing the behavior of a system or of a single object. For example, it can help you determine the different events that might occur during an object's lifetime. Like different user inputs, and how that object should behave when these events occur, like checking conditions and performing actions.