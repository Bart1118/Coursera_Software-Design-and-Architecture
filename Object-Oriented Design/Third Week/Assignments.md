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

