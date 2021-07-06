# Read: Class 09

## Functional Programming Concepts
<br />

1. What is functional programming?<br />
    Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.
    <br />

2. What is a pure function and how do we know if something is a pure function?<br />
    It returns the same result if given the same arguments (it is also referred as deterministic)
    <br />

3. What are the benefits of a pure function?<br />
    It does not cause any observable side effects. Examples of observable side effects include modifying a global object or a parameter passed by reference.
    <br />
4. What is immutability?<br />
    mutability is discouraged in functional programming.
    <br />
5. What is Referential transparency?<br />
    Basically, if a function consistently yields the same result for the same input, it is referentially transparent.
    <br />

## Node JS Tutorial for Beginners #6 - Modules and require()

1. What is a module?<br />
    a module is just another JS file that works like a component, it have some functionality and we call it whenever we need it.
    <br />
2. What does the word ‘require’ do?<br />
    it like imports the module file to another file so we can use it.
    <br />
3. How do we bring another module into the file that we are working in?<br />
    we use `require('x')` ,the `'x'` string will be the path to module we reqire in the working file.
    <br />
4. What do we have to do to make a module available?<br />
    we need to export the functionaliteis that we may use in other files using `module.export = 'functions'`

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)