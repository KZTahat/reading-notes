#  Class 05

## Putting it all together

### React Docs - thinking in React

1. How would you break a mock into a component heirarchy?<br />
    The first thing you’ll want to do is to draw boxes around every component (and subcomponent) in the mock and give them all names.
    <br />
2. What is the **single responsibility principle** and how does it apply to components?<br />
     Single responsibility principle, that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.
     <br />
3. What does it mean to build a ‘static’ version of your application?<br />
    A version that takes your data model and renders the UI but has no interactivity, to build a static version of your app that renders your data model, you’ll want to build components that reuse other components and pass data using props. Don’t use state at all to build this static version, state is reserved only for interactivity, that is, data that changes over time. Since this is a static version of the app, you don’t need it.
    <br />
4. Once you have a static application, what do you need to add?<br />
    Identify The Minimal (but complete) Representation Of UI State, to make your UI interactive, you need to be able to trigger changes to your underlying data model. React achieves this with state.
    <br />
5. What are the three questions you can ask to determine if something is state?<br />
    1. Is it passed in from a parent via props? If so, it probably isn’t state.<br />
    2. Does it remain unchanged over time? If so, it probably isn’t state.<br />
    3. Can you compute it based on any other state or props in your component? If so, it isn’t state.
    <br />

6. How can you identify where state needs to live?<br />
    For each piece of state in your application:

    * Identify every component that renders something based on that state.<br />
    * Find a common owner component (a single component above all the components that need the state in the hierarchy).<br />
    * Either the common owner or another component higher up in the hierarchy should own the state.<br />
    * If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.<br />


<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)