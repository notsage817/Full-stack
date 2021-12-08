### Model-View-Controller
+ *Models* manage data and business logic for us.
+ *Views* handles display and representation logic (HTML,CSS,JS)
+ *Controllers* routes commands to the models and views, containing control logic.

![image](https://user-images.githubusercontent.com/59595363/145305749-feadcb25-dbaf-48ac-a891-4ef871a92fbb.png)

#### Create the functionality
1. On the view: implement an HTML form
2. On the controller: retrieve the user's input and manipulate models
3. On the models: create a record in database and return the newly created to-do item to the controller
4. On the controller: take the newly created to-do item, and decide how to update the view with it.
##### Getting user data from a view to a controller
+ URL query parameters
  + 
+ Forms
  `request.form.get('<name>')` reads the value from a form input control by the <name> attribute on the input HTML element.
+ JSON
  `request.data` retrieves JSON as a string.
