# HTML Tables; JS Constructor Functions
<!-- Chapter 6: “Tables” (pp.126-145) -->
## Tables
There are several types of information that need to be displayed in a grid or table. For example: sports results, stock reports, train timetables.A table represents information in a grid format. Examples of tables include financial reports, TV schedules, and sports results.<br />
- ****Basic Table Structure**:
    The ```<table>``` element is used to create a table. The contents of the table are written out row by row.
    ```<tr>``` : You indicate the start of each row using the opening ```<tr>``` tag. (The tr stands for table row.) It is followed by one or more ```<td>``` elements (one for each cell in that row). At the end of the row you use a closing ```</tr>``` tag. Each cell of a table is represented using a ```<td>``` element. (The td stands for table data.)<br />

- **Table Headings**:
    The ```<th>``` element is used just like the ```<td>``` element but its purpose is to represent the heading for either a column or a row. (The th stands for table heading.) Even if a cell has no content, you should still use a ```<td>``` or ```<th>``` element to represent the presence of an empty cell otherwise the table will not render correctly. (The first cell in the first row of this example shows an empty cell.)Using ```<th>``` elements for headings helps people who use screen readers, improves the ability for search engines to index your pages, and also enables you to control the appearance of tables better when you start to use CSS.You can use the scope attribute on the ```<th>``` element to indicate whether it is a heading for a column or a row. It can take the values: row to indicate a heading for a row or col to indicate a heading for a column.<br />
    <br />
<!-- Chapter 3: “Functions, Methods, and Objects” (pp.106-144) -->
## Creating an Object: constructor notation
The new keyword and the object constructor creat a blank object, we can then add properities and methods to the object.<br />
First, you create a new object using a combination of the new keyword and the Object () constructorfunction. (This function is part of the JavaScript language and is used to create objects.), Next, having created the blank object, you can add properties and methods to it using dot notation. Each statement that adds a property or method should end with a semicolon.<br />
- **Updating an object**:
    To update the value of properties, use dot notation or square brackets. They work on objects created using literal or constructor notation. To update a property, use the same technique that was shown on the left-hand block to add properties to the object, but give it a new value. If the object does not have the property you are trying to update, it will be added to the object. <br />
    <br />
    ```
    hotel.name = 'park';
    ```
    <br />
    You can also update the properties of an object (but not its methods) using square bracket syntax. The object name is followed by square brackets, and the property name is inside them. A new value for the property is added after the assignment operator. Again, if the property you areattempting to update does not exist, it will be added to the object.<br />
    <br />

    ```
    hotel['name'] = 'park';
    ```
    <br />
- **CREATING MANY OBJECTS: CONSTRUCTOR NOTATION**:
    Sometimes you will want several objects to represent similar things. Object constructors can use a function as a template for creating objects. First, create the template with the object's properties and methods. ometimes you will want several objects to represent similar things. Object constructors can use a function as a template for creating objects. First, create the template with the object's properties and methods. The function has three parameters. Each one sets the value of a property in the object. The methods will be the same for each object created using this function.<br />
    <br />

    ```
    function Hotel (name, rooms, booked) {
        this.name = name; 
        this.rooms = rooms;
        this.booked = booked;
        this. checkAvailability = function() { 
            return this.rooms - this. booked; 
        };
    }
    ```
    <br />
    The this keyword is used instead of the object name to indicate that the property or method belongs to the object that this function creates. Each statement that creates a new property or method for this object ends in a semicolon (not a comma, which is used in the literal syntax). The name of a constructor function usually begins with a capital letter (unlike other functions, which tend to begin with a lowercase character). The uppercase letter is supposed to help remind developers to use the new keyword when they create an object using that function (see next page).<br />

    we create instances of the object using the constructor function. The new keyword followed by a call to the function creates a new object. The properties of each object are given as arguments to the function.<br />
    Here, two objects are used to represent two hotels, so each object needs a different name. When the new keyword calls the constructor function (defined on the left-hand page), it creates a new object. Each time it is called, the arguments are different because they are the values for the properties of each hotel. Both objects automatically get the same method defined in the constructor function.<br />
    <br />

    ```
    var quayHotel = new Hotel('Quay', 40, 25);
    var parkHotel = new Hotel('Park', 120, 77);
    ```
    <br />
    Even when many objects are created using the same constructor function, the methods stay the same because they access, update, or perform a calculation on the data stored in the properties. You might use this technique if your script contains a very complex object that needs to be available but might not be used. The object is defined in the function, but it is only created if it is needed.<br />


<br />

[Home]( https://kztahat.github.io/reading-notes/)