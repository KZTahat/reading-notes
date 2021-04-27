# HTML Links, CSS Layout, JS Functions
<!-- Chapter 3 (first part): “Functions, Methods, and Objects” (pp.86-99 ONLY) -->
## Functions and Methods 
Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of statements).Furthermore, the statements in function are not always executed when a page loads, so functions also offer a way to store the steps needed to achieve a task. The script can then ask the function to perform all of those steps as and when they are required. If you are going to ask the function to perform its task later, you need to give your function a name. That name should describe the task it is performing. When you ask it to perform its task, it is known as **calling** the function. Remember that programming Some functions need to be provided with information in order to achieve a given task. For example, a function to calculate the area of a box would need to know its width and height.Pieces of information passed to a function are known as **parameters**. And when you write a function and you expect it to provide you with an answer the response is known as a **return value**.
- **Declaring Function**<br />
    to creat a function, you give it a name and then write the statments needed to achieve its task inside the curly braces. functions store the code required to perform specific task and that the script can ask the function to perform this task whenever needed. If different parts of a script need to to perform the same task, you do not need to repeat the same statmentsmultiple times, you use a function to do it and reuse the same code.<br />

    sometimes a function needs specific information to perform its task, in such cases when we declare a function we give it parameters where inside the function they act like variables. if a function needs information to work we indicates what it needs to know in parentheses after the function name known as the parameters of the function and inside the function they act like variables, this demonestrates how the code can perform a task without knoeing the exact details in advance.
- **Calling a function**<br />
    Having declared the function, we can then execute all its statments between its curly braces with just one line of code. This is known as calling the function, to run the code in the function we use the function name followed by parentheses, we can call the same function as many times as we want within a JavaScript file, sometimes we may see a function is called befor it has been declared. Will this still works becuase the interpreter runs through a script befor executing each statment, so it will know that a function declaration appears later in the script, but for the moment we will declare the function befor calling it.<br />

    when we call a function that needs parameters, we specify the values it should use in the parentheses thet follow its name, those values are called arguments and can be provided as variables or as values.<br />
    - *returning a single value*:
      some functions return information to the code that called them, for example when they perform a calculation thehy return the result, this also demonestrates how the same function can be used to performe thte same steps with different values.

<!-- Chapter 4: Ch.4 “Links” (pp.74-93) -->
## Links
Links are the defining feature of the web because they allow you to move from one web page to another — enabling the very idea of browsing or surfing.
- Writing Links:<br />
    Links are created using the ```<a>``` element. Users can click on anything between the opening ```<a>``` tag and the closing ```</a>``` tag. You specify which page you want to link to using the href attribute.
    
    ```
        <a href="http://www.imdb.com">IMDB</a>
    ```
    The text between the opening ```<a>``` tag and closing ```</a>``` tag is known as link text. Where possible, your link text should explain where visitors will be taken if they click on it (rather than just saying "click here"). To write good link text, you can think of words people might use when searching for the page that you are linking to. (For example, rather than write "places to stay" you could use something more specific such as "hotels in New York.")<br />
    When you are linking to other pages within the same site, you do not need to specify the domain name in the URL. You can use a shorthand known as a relative URL. If all the pages of the site are in the same folder, then the value of the href attribute is just the name of the file.<br />

- Email Links:<br />
    To create a link that starts up the user's email program and addresses an email to a specified email address, you use the ```<a>``` element. However, this time the value of the href attribute starts with **mailto:** and is followed by the email address you want the email to be sent to. An email link will look just like any other link but, when it is clicked on, the user's email program will open a new email message and address it to the person specified in the link.<br />


[Home]( https://kztahat.github.io/reading-notes/)