# Read 03

## Express REST API

1. Name 3 real world use cases where you’d want to change the request with custom middleware.<br />

2. True or false: The route handler is middleware?<br />
   True, Route handler or Router level middlewares are similar to application-level middlewares except that they are bound to an instance of express.Router().
   <br />
3. In what ways can a middleware function end the process and send data to the browser?<br />

   - when there is some error and it calls next with some message.
   - by simply sending the data with (res.send()).

4. At what point in the request lifecycle can you “inject” middleware?<br />
   It can be injected befor or after every request.

5. What can cause express to error with “Request headers sent twice, cannot start a second response”<br />
   when you send headers twice.

<br />

## Terms

- Middleware: Middleware is a term for any software or service that enables the parts of a system to communicate and manage data. It is the software that handles communication between components and input/output, so developers can focus on the specific purpose of their application.<br />

It's mainly functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next.


- Request Object: The request object is the main entry point for an application to issue a request to the Library - all operations on a URL must use a Request object. <br />

- Response Object: It is the object which communicates between the server and the output which is sent to the client.<br />

- Application Middleware: it is a simple function that excutes regular javascript code.<br />

- Routing Middleware: Router-level middleware works in the same way as application-level middleware, except it is bound to an instance of express.Router().<br />

- Test Driven Development: is a software development process relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases.<br />

- is a branch of Test Driven Development (TDD). BDD uses human-readable descriptions of software user requirements as the basis for software tests. <br />

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)