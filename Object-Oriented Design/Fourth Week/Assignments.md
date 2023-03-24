Now that you have become more familiar with this application, it’s time to add some new functionality.

In this assignment you will update the application to implement this new functionality using the updated UML class diagram as a guide. 

**Setup instructions**

**Use this tutorial as your guide:**

[[SDA Object-Oriented Design - Capstone 1.4 Tutorial.pdf]]

Use the following updated UML class diagram to assist you with your understanding and implementation:

![[Pasted image 20230324150102.png]]

**About the application**

This version of the app should accommodate the new contacts feature. In particular:

-   ContactsActivity should be accessible from the MainActivity. 

![[Pasted image 20230324155446.png]]

![[Pasted image 20230324155501.png]]

-   ContactsActivity should be implemented as a ListView.
-   An owner should now be able to add a potential borrower (a contact) to their contacts. Each contact must have a unique username and an email.

![[Pasted image 20230324155616.png]]

![[Pasted image 20230324155622.png]]

-   An owner can edit or delete a contact, but not if the contact is currently borrowing an item, i.e. the contact is a borrower.

![[Pasted image 20230324155635.png]]

-   Owners are now required to select a contact to be the borrower of an item when changing the status of an item from “Available” to “Borrowed”. That is, it is no longer sufficient to enter the borrower’s username as a string -- now the borrower must be picked from the owner’s list of contacts. 

![[Pasted image 20230324155648.png]]

![[Pasted image 20230324155653.png]]

![[Pasted image 20230324155702.png]]

**Part 1 Submission** will test your ability to translate the UML class diagram into Java code. When you are ready to submit your code, include the following two files in a folder:

-   **Contact.java**
-   **ContactList.java**

Then compress the folder into a ZIP archive. Windows users can use 7zip or WinRAR. Upload it where prompted.

**Part 2 Submission** will test the correctness of your code

In order to grade your assignment, you will need to submit a 5 minutes or less demo video of your app that shows the following steps as a continuous interaction without crashing (if possible):

1.  Start the video of your app from the MainActivity.
2.  From the MainActivity, navigate to the ContactsActivity.
3.  From the ContactsActivity, add a new contact to your contact list. Show that you can enter a username and email, save this contact to your contact list.
4.  Show that by selecting (long clicking) a contact in the contact list, you can edit this contact. Update the email address of a contact.
5.  Show that you can delete one of your contacts.
6.  Go back to the MainActivity and look at your available Items.
7.  Add an item to your inventory (if you don't already have an available item).
8.  Edit an item in your inventory by long clicking on the item. Click the "Available" toggle. The toggle should now say "Borrowed" and a box should appear below to indicate the name of the borrower. By default the box will show the username of the first contact in your contacts. If you have more than one contact in your contacts you can click this box and then select the desired contact.
9.  Finally, press "Save" to return to your inventory.

Upload your demo video to [Internet Archive](https://archive.org/index.php) or [YouTube](https://www.youtube.com/) and then provide a link to it where prompted. 