# Class 04

## React Docs - Forms

1. What is a ‘Controlled Component’?<br />
    A controlled component is a component element whose value is controlled by React using state, so with a controlled component, the element value is always driven by the React state. 
    <br />
    
2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.<br />
    We can not wait till the user submit the form we need to update the state with their responses as soon as they enter them in input fields, so the updates will runs on every keystroke to update the React state, the displayed value will keep updaing as the user types. And if we waited till the user submits the form the values of the targets will be **undifined**
    <br />

3. How do we target what the user is entering if we have an event handler on an input field?<br />
    The event handler exists on each input field using **onChange** attribute where the handler itself is using **event** to target the crossponding input.
<br />

## The Conditional (Ternary) Operator Explained

1. Why would we use a ternary operator?<br />
    To make the code shorter and to have less numbers of code.
<br />
2. Rewrite the following statement using a ternary statement:<br />

        if(x===y){
        console.log(true);
        } else {
        console.log(false);
        }

    <br />
    this code block with ternary operator will look like this:
    <br />
    <br />
    
    ```
    x===y ? console.log(true) : console.log(false);
    ```

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)