## Practice Peer-graded Assignment: Ungraded Assignment – UML Sequence Diagram

**Assignment Topic:**

Here is an UML class diagram to represent a system for North American airports.

![[u0aE1YbuEem-xg4p7cmXwA_f52c77b6ccf3423fa9a389a7ea4ac135_ungraded_uml_class_00.jpg]]

Now you are being asked to communicate more details about the system.

Create a UML sequence diagram that will show your clients how the system’s classes will interact when customers are buying their flight tickets on the booking website.

The system should allow the customer to search available flights from the database by inputting their desired location and departure/arrival date. The website will search the database and return the available flights to display. Once the customer has chosen the flight, they will add the flight to their cart and checkout. They will also then input their payment information and once everything is complete, the website should confirm the flight, empty cart and lastly display a confirmation of the ticket for the flight.

**How to submit:**

You will be expected to upload a PDF file of your UML sequence diagram. A free online tool you may use to make your diagram is [Lucidchart](https://www.lucidchart.com/).

![[Blank diagram (1)_00.jpg]]

![[Pasted image 20230313175515.png]]

***

## Peer-graded Assignment: Capstone Assignment 1.2 – UML Sequence Diagram

**Guidelines for the assignment**

Review this lecture to aid you on your assignment:

1.3.6 – UML Sequence Diagram

**How to create your assignment**

Review the code responsible for adding a new item.

Make a sequence diagram that captures the interactions of objects in the app when a new item is added.

Your sequence diagram should contain the following classes:

-   AddItemActivity
-   ItemList
-   Dimensions
-   Item

And contain calls of the following methods:

-   onCreate() (provided for you, see Template)
-   loadItems()
-   saveItem() (provided for you, see Template)
-   Dimensions constructor
-   Item constructor
-   addItem()
-   saveItems()

Lastly, the activation of AddItemActivity should start with the call to “onCreate()”

![[My UML Sequence Diagram_00.jpg]]

![[1A6qSJLZS2iOqkiS2Qtocg_00e55cd0dc29494193fac28e8e5b9700_1.2_sequence_diagram_solution_00.jpg]]

***

## Practice Peer-graded Assignment: Ungraded Assignment – UML State Diagram

**Assignment Topic:**

During your two previous assignments you created a UML class diagram and sequence diagram to display your new system for North American airports. You are now required to create a UML state diagram to communicate the state of the planes in the airports.

The airplanes should go through multiple different states. When planes are not in use for a flight they are usually **waiting** to be assigned. Once a plane is chosen to be used for a flight, they are **assigned** to that flight until the airplane is ready for take-off. While the plane is in the air and flying the state is termed **‘en route’**. Once the plane has reached its destination, the plane has to change into a state of **landing** for the airport to prepare for its arrival. Finally, once the plane has successfully landed, the plane is checked to see if it is ready to be assigned to a new flight or if maintenance is required. If **maintenance** is required the plane is unusable and if a mechanic decides that the plane cannot be repaired it is removed from the airport and disposed. 

![[Blank diagram_00.jpg]]

![[Pasted image 20230320173724.png]]

***

## Peer-graded Assignment: Capstone Assignment 1.3 – UML State Diagram

**Guidelines for the assignment**

Review this lecture to aid you on your assignment:

Review Lecture: 1.3.7 – UML State Diagram

**How to create your assignment**

Review the code responsible for adding a new item and editing an existing item.

Remember that an item can either be “Available” or “Borrowed” and can either have an image attached or not.

In this assignment you are to make a state diagram that captures the four possible states of an item.

-   Available without photo
-   Available with photo
-   Borrowed without photo
-   Borrowed with photo

Include arrows to indicate transitions between the states and label these transitions accordingly. And, remember to include the terminal state and to indicate the starting state. 

![[Blank diagram_00 1.jpg]]

