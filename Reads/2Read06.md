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
The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window. As a browser loads a web page, it creates a model of that page. The model is called a DOM tree, and it is stored in the browsers' memory. It consists of four main types of nodes. <br />
- **THE DOCUMENT NODE**<br />
- **ELEMENT NODE**<br />
- **ATTRIBUTE NODE**<br />
- **TEXT NODE**<br />

```
<html> 
    <body> 
        <div id="page"> 
            <hl id="header">List</hl> 
            <h2>Buy groceries</h2> 
            <ul > 
                <li id="one" class="hot"><em>fresh</em> figs</li> 
                <li id="two" class="hot">pine nuts</l i> 
                <li id="three" class="hot">honey</l i > 
                <li id="four">balsamic vinegar</l i> 
            </ ul > 
        </ div> 
        <script src="js/l i st.js "></scri pt> 
    </ body> 
</ html > 
```

Every element, attribute, and piece of text in the HTML is represented by its own DOM node. At the top of the tree a document node is added; it represents the entire page (and also corresponds to the document object, which you first met on p36). When you access any element, attribute, or text node, you navigate to it via the document node. It is the starting point for all visits to the DOM tree.< br />
HTML elements describe the structure of an HTML page. (The ```<hl>``` - ```<h6>``` elements describe what parts are headings; the ```<p>``` tags indicate where paragraphs of text start and finish; and so on.)<br />
Each node is an object with methods and properties. Scripts access and update this DOM tree (not the source HTML file). Any changes made to the DOM tree are reflected in the browser. The opening tags of HTML elements can carry attributes and these are represented by attribute nodes in the DOM tree. Attribute nodes are not children of the element thar carries them; they are part of that element. Once you access an element, there are specific JavaScript methods and properties to read or change that element's attributes. For example, it is common to change the values of cl ass attributes to trigger new CSS rules that affect their presentation. <br />
Once you have accessed an element node, you can then reach the text within that element. This is stored in its own text node. Text nodes cannot have children. If an element contains text and another child element, the child element is not a child of the text node but rather a child of the containing element. (See the ```<em>``` element on the first ```<li>``` item.) This illustrates how the text node is always a new branch of the DOM tree, and no further branches come off of it. 


[Home]( https://kztahat.github.io/reading-notes/)