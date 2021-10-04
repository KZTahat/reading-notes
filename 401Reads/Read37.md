# Read 37

## Redux - Combined Reducers

1. Why choose Redux instead of the Context API for global state?
   Redux allows you to manage your app's state in a single place and keep changes in your app more predictable and traceable. It makes it easier to reason about changes occurring in your app.

2. What is the purpose of a reducer?
   A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. We have tools, like Redux, that help manage an application's state changes in a single store so that they behave consistently.

3. What does an action contain?
   The action describes what happened and it is the reducer's job to return the new state based on that action. and it has two main keys - type - of the change will happen to the state, and - payload - which is a piece of information that used to make the change to the state.

4. Why do we need to copy the state in a reducer?
   If the new state is different, the reducer must create new object, and making a copy is a way to describe the unchanged part.

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)
