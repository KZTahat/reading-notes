# JS Object Literals; The DOM
<!-- Chapter 3: “Object Literals” (pp.100-105) -->
## WHAT IS AN OBJECT? 
Objects group together a set of variables and functionsto create a model of a something you would recognize from the real world. In an object, variables and functions take on new names.<br />
- IN AN OBJECT: VARIABLES BECOME KNOWN AS PROPERTIES:<br />
    If a variable is part of an object, it is called a property. Properties tell us about the object, such as the name of a hotel or the number of rooms it has. Each individual hotel might have a different name and a different number of rooms.
- IN AN OBJECT: FUNCTIONS BECOME KNOWN AS METHODS:<br />
    If a function is part of an object, it is called a method. Methods represent tasks that are associated with the object. For example, you can check how many rooms are available by subtracting the number of booked rooms from the total number of rooms.
<br />
Like variables and named functions, properties and methods have a name and a value. In an object, that name is called a key. An object cannot have two keys with the same name. This is because keys are used to access their corresponding values. The value of a property can be a string, number, Boolean, array, or even another object. The value of a method is always a function.<br />
- creating an object (literal notation):<br />
    Literal notation is the easiest and the most popular war to creat objects.<br />
```
var hotel = {
    name: 'Quay',
    rooms: 40,
    booked: 25,
    gym: true,
    roomtype: ['twin','double','suite'],

    checkAvability: function(){
        return this.rooms - this.booked;
    }
}
```
- Accessing an object (Dot operation):<br />
    we access the properties or methods of an object using dot notation, we can also access them using square brackets.<br />
```
var hotelname = hotal.name;
var rommsfree = hotel.checkAvailability();
```
<!-- Chapter 5: “Document Object Model” (pp.183-242) -->
## Document Object Model:<br />
The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window. 