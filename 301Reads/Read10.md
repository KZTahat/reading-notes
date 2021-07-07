# Read: Class 10

## Understanding the JavaScript Call Stack

1. What is a ‘call’?<br />
    The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.
    <br />

2. How many ‘calls’ can happen at once?<br />
    one call at a time
    <br />

3. What does LIFO mean?<br />
    At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).
    <br />

4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.<br />
    ```
    function firstFunction(){
    console.log("Hello from firstFunction");
    }

    function secondFunction(){
    firstFunction();
    console.log("The end from secondFunction");
    }

    secondFunction();

We only need to invoke seconed function in order to generate the call stack

5. What causes a Stack Overflow?<br />
    A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.
    <br />
    ```
    function callMyself(){
    callMyself();
    }

    callMyself();

The `callMyself()` will run until the browser throws a “Maximum call size exceeded”. And that is a stack overflow.
<br />

## JavaScript error messages

1. What is a ‘refrence error’?<br /
    This is as simple as when you try to use a variable that is not yet declared you get this type os errors.<br />
    `console.log(foo) // Uncaught ReferenceError: foo is not defined`
    <br />

2. What is a ‘syntax error’?<br />
    this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.<br />
    `JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1`
    <br />

3. What is a ‘range error’?<br />
    Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.<br />
    `var foo= [] 
    foo.length = foo.length -1 // Uncaught RangeError: Invalid array length`<br />

4. What is a ‘tyep error’?<br />
    Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.<br />
    `var foo = {}
    foo.bar // undefined
    foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined` <br />

5. What is a breakpoint?<br />
    The point were we will have the error, the red part of our first example represents the call stack, which is the path that your program has taken to reach the point were you set a `breaking` point or were you have an error.

6. What does the word ‘debugger’ do in your code?<br />
    The breakpoint can also be achieved by putting a `debugger` statement in your code in the line you want to break.


<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)