#  JS Debugging
<!-- JavaScript book, Ch. 10, “Error Handling & Debugging” -->
## Error handling and debugging
JavaScript can be hard to learn and everyone makes mistakes when writing it. This chapter will help you learn how to find the errors in your code. It will also teach you how to write scripts that deal with potential errors gracefully.<br />
- **ORDER OF EXECUTION**:<br />
    To find the source of an error, it helps to know how scripts are processed. The order in which statements are executed can be complex; some tasks cannot complete until another statement or function has been run. The JavaScript interpreter uses the concept of execution contexts. There is one global execution context; plus, each function creates a new new execution context. They correspond to variable scope.<br />
- **STACKS**:<br />
    The JavaScript interpreter processes one line of code at a time. When a statement needs data from another function, it stacks (or piles) the new function on top of the current task.<br />
    When a statement has to call some other code in order to do its job, the new task goes to the top of the pile of things to do. Once the new task has been performed, the interpreter can go back to the task in hand. Each time a new item is added to the stack, it creates a new execution context. Variables defined in a function (or execution context) are only available in that function. If a function gets called a second time, the variables can have different values. You can see how the code that you have been looking at so far in this chapter will end up with tasks being stacked up on each other in the diagram to the right.<br />
    In the interpreter, each execution context has its own va ri ables object. It holds the variables, functions, and parameters available within it. Each execution context can also access its parent's v a ri ables object. Functions in JavaScript are said to have lexical scope. They are linked to the object they were defined within. So, for each execution context, the scope is the current execution context's variables object, plus the variables object for each parent execution context. Imagine that each function is a nesting doll. The children can ask the parents for information in their variables. But the parents cannot get variables from their children. Each child will get the same answer from the same parent. <br />

    ```
    var greeting = (function() {
        var d =new Date(); 
        var time= d.getHours(); 
        var greeting= greetUser(); 

        function greetUser() { 
            if (time < 12) { 
            var msg = 'Good morning '; 
        } else { 
            var msg = 'Welcome ' ; 
        }
            return= msg + getName(); 

        function getName() { 
        var name = 'Molly'; 
        return name; 
        }
       }
    });
    alert(greeting);
    ```
    <br />
    If a variable is not found in the variables object for the current execution context, it can look in the variables object of the parent execution context. But it is worth knowing that looking further up the stack can affect performance, so ideally you create variables inside the functions that use them. If you look at the example on the left, the inner functions can access the outer functions and their variables. For example, the greetUser() function can access the time variable that was declared in the outer greeting() function. Each time a function is called, it gets its own execution context and va r i ables object. Each time an outer function calls an inner function, the inner function can have a new variables object. But variables in the outer function remain the same. Note: you cannot access this variables object from your code; it is something the interpreter is creating and using behind the scenes. But understanding what goes on helps you understand scope.<br />

- **UNDERSTANDING ERRORS**:<br />
    If a JavaScript statement generates an error, then it throws an exception. At that point, the interpreter stops and looks for exception-handl ing code.<br />
    If you are anticipating that something in your code may cause an error, you can use a set of statements to handle the error. This is important because if the error is not handled, the script will just stop processing and the user will not know why. So exception-handling code should inform users when there is a problem. 


- *Syntax Error*:<br />
    - **SYNTAX IS NOT CORRECT**
    This is caused by incorrect use of the rules of the 
    language. It is often the result of a simple typo. 
    - **MISMATCHING OR UNCLOSED QUOTES**
    *document .write ("Howdyl');*
    SyntaxError: Unexpect ed EOF 
    - **MISSING CLOSING BRACKET**
    *document .getElementByid('page'*
    SyntaxErr or : Expected token ' ) ' 
    - **MISSING COMMA IN ARRAY**
    Would be same for missing] at the end 
    *var list = ['Item 1', 'Item 2 '  'rtem 3'];*
    SyntaxError: Expected token ']' 
    - **MALFORMED PROPERTY NAME**
    It has a space but is not surrounded by quote marks 
    *user = {first  name: "Ben", lastName: "Lee"};*
    Synt axError: Expected an identifier but 
    found 'name ' instead 

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)