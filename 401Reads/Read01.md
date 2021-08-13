## Read: Class 01

# Node Ecosystem, TDD, CI/CD

- **Array.map()**<br />
  The `map()` method creates a new array populated with the results of calling a provided function on every element in the calling array. and using map() method a return statment must be included in each iteration else it will automaticllay return null.

<br />

- **Array.reduce()** <br />
  The `reduce()` method executes a reducer function (that you provide) on each element of the array, resulting in a single output value.

<br />

- **superagent()** <br />

  - using the normal promise `.then()` :
    <br />
    <br />

  ```
  superagent
    .get(URL)
    .then((res) => {
        console.log(res);
      // res.body , res.headers , res.status
    })
    .catch((err) => {
      // console.log(err);
    });
  ```

      <br />

  - using `async/await` syntax :
    <br />
    <br />

  ```
  async function getResponse(){
      try{
      const response = await superagent.get(URL);
      console.log(response);
      // res.body , res.headers , res.status

      } catch (err){
          console.log(err);
      }

  }
  ```

  <br />

- `Promises `<br />
    A promise represents an operation that hasn't completed yet, instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future.<br />
    A Promise is in one of these states:

    - pending: initial state, neither fulfilled nor rejected.
    - fulfilled: meaning that the operation was completed successfully.
    - rejected: meaning that the operation failed.

<br />

- `Callback Functions` <br />
    Simply taking a callback doesn't make a function asynchronous. There are many examples of functions that take a function argument but are not asynchronous. For example there's forEach in Array. It iterates over each item and calls the function once per item.

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)