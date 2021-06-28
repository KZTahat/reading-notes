# Passing Functions as Props

## React Docs - lists and keys

1. What does .map() return?<br />
    .map returns whatever varialble we are storing the .map callback functiona output as an array for sure, because ,map is only used with arrays. so we are iterating through an array, make whatever changes to the array elements inside the callback function, store the new element in the assigned variable using **return** key word and then return the variable.
    <br />
2. If I want to loop through an array and display each value in JSX, how do I do that in React?<br />
    We can build collections of elements and include them in JSX using curly braces {}. we loop through the elements of an array using the JavaScript map() function. We return a ```<li>``` element for each item. Finally, we assign the resulting array of elements to listItems. On the parent componenet we include the entire listItems array inside a ```<ul>``` element, and render it to the DOM.
    <br />
3. Each list item needs a unique ____.<br />
    Each list item needs a unique key, When not using the key, we’ll be given a warning that a key should be provided for list items. A “key” is a special string attribute you need to include when creating lists of elements.
4. What is the purpose of a key?<br />
    Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity, the best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys, When we don’t have stable IDs for rendered items, you may use the item index as a key as a last resort:<br />
    ```
    const todoItems = todos.map((todo, index) =>
        // Only do this if items have no stable IDs
        <li key={index}>
            {todo.text}
        </li>
    );
    ```
<br />


## The Spread Operator

1. What is the spread operator?<br />
    In JavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments. The spread operator was added to JavaScript in ES6, just like the rest parameters, which have the same syntax: three magic dots ```…```.
2. List 4 things that the spread operator can do.<br />
    - Adding to state in React<br />
    - Concatenating or combining arrays<br />
    - Combining objects <br />
    - Using Math functions <br />
    <br />
3. Give an example of using the spread operator to combine two arrays.<br />

    ```
        const myArray = [`🤪`,`🐻`,`🎌`]
        const yourArray = [`🙂`,`🤗`,`🤩`]
        const ourArray = [...myArray,...yourArray]
        console.log(...ourArray) // 🤪 🐻 🎌 🙂 🤗 🤩
    ```
<br />

4. Give an example of using the spread operator to add a new item to an array.<br />
    ```
    const fewFruit = ['🍏','🍊','🍌'] // 3
    const fewMoreFruit = ['🍉', '🍍', ...fewFruit] // Adding two more
    console.log(fewMoreFruit) // (5) ["🍉", "🍍", "🍏", "🍊", "🍌"]
    ```
5. Give an example of using the spread operator to combine two objects into one.<br />
    ```
    const hello = {hello: "😋😛😜🤪😝"}
    const world = {world: "🙂🙃😉😊😇🥰😍🤩!"}
    const helloWorld = {...hello,...world}
    console.log(helloWorld) // {hello: "😋😛😜🤪😝", world: "🙂🙃😉😊😇🥰😍🤩!"}
    ```
<br />

## How to Pass Functions Between Components

1. In the video, what is the first step that the developer does to pass functions between components?<br />
    He created a new thing (variable or attribute) to send as a prop to send to the child component
    <br />
2. In your own words, what does the increment function do?<br />
    The increment function adds one to the this.count each time the user presses on **Add** button.
    <br />
3. How can you pass a method from a parent component into a child component?<br />
    We can easily pass it as we pass the other props inside the component tag, **methodName = {this.method}**
    <br />
4. How does the child component invoke a method that was passed to it from a parent component?<br />
    On the child side we easily invoke the passed method like we use the other props:
    ```
    this.props.methodName(parameters);
    ```


<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)