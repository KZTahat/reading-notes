# Read 23

## Advanced State with Reducers

1. How can we ensure that an effect hook runs only once?
   If we pass an empty array [] , it just renders the component only once like componentDidMount .

2. Can useState() update more than one state variable at the same time?
   no it can't, we could combine the loading state and data state into one state object and then you could do one setState call and there will only be one render.` Note: Unlike the setState in class components, the setState returned from useState doesn't merge objects with existing state, it replaces the object entirely`.

3. Is useState() synchronous?
   useState and setState both are asynchronous. They do not update the state immediately but have queues that are used to update the state object.

## Terms

- State Hook : A Hook is a special function that lets you “hook into” React features.
- Component Lifecycle : We are born, grow, and then die. Almost everything follows this cycle in its life, and React components do as well. Components are created (mounted on the DOM), grow by updating, and then die (unmount on DOM).

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)
