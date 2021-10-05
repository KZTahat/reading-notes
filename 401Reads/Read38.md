# Read 38

## Redux - Asynchronous Actions

1. How granular should your reducers be?
   A Redux app really only has one reducer function: the "root reducer" function that you will pass to createStore later on. That one root reducer function is responsible for handling all of the actions that are dispatched, and calculating what the entire new state result should be every time.

2. Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched
   I think this is a pro, thus we can handel and mainpulate different parts of the state. This is because the suggested Redux reducer structure is "reducer composition", where many mostly-independent reducer functions can be combined into one structure, and many reducer functions could potentially respond to a single action and update their own slice of state.

3. Name a strategy for preventing the above
   there is definitely no one-to-one mapping by default, and you should break out of such a paradigm any time you feel you want to handle an action in many reducers.

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)
