# Read: Class 13

## Status Codes Based On REST Methods

1. In your own words, describe what each group of status code represents:<br />
    - 100’s = These are informational status codes; they usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client. Like using a different protocol or telling the client that its request will fail before they start sending the body.<br />
    - 200’s = These are the success codes. They tell the client that its request was accepted. <br />
    - 300’s = These are redirection codes. They tell the client that the resource they are requesting isn’t available at the expected location anymore. This can have multiple reasons, be temporary or permanent, but the client has to issue a request to the new location. <br />
    - 400’s = These are the client error codes. They are all about invalid requests a client sent to a server. There are several causes to this, timeouts, wrong URI, missing authentication, etc. A client is sending incorrect input and should confirm the input parameters are correct before retrying the request. <br />
    - 500’s = These are the server error codes. Often they indicate problems with overwhelmed servers or unreachable servers behind proxies, but sometimes they can be directly related to client requests that trigger error exceptions on the server. These errors can be temporary or permanent. Usually it’s best for the client to retry the same request.
     <br />
2. What is a status code 202?<br />
    that the request met all validation requirements at the time of sending.
    <br />

3. What is a status code 308?<br />
     This code tells the client that the request was valid, but its processing will finish sometime in the future.
     <br />
     
4. What code would you use if an update didn’t return data to a client?<br />
    204 No Content 
    <br />

5. What code would you use if a resource used to exist but no longer does?<br />
    410 Gone
    <br />

6. What is the ‘Forbidden’ status code?<br />
    403 Forbidden
    <br />

## Build A REST API With Node.js, Express, & MongoDB - Quick 

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?<br />
    Because when we want to deploy our application, we will need to use some other other server than localhost, so we need to remove it to enviroment variable. 
    <br />

2. What is middleware?<br />
    Middleware is essentialy code that runs when the server gets a request but befor it gets passed to my routes 
    <br />
3. What does app.use(express.json()) do?<br />
    This lets our server accepts JSON as a body instead of post element or get element.
    <br />

4. What does the /:id mean in a route?<br />
    This is an ID for the each route we have, and with the colon infront of it this means that it's a parameter that we can access by typing in request `requset.params.id` and this would give us access to whatever they pass after the first slash.
    <br />

5. What is the difference beween PUT and PATCH?<br />
    They are both for updating routes, BUT we used `PATCH` for updating only what the user passes and we use `PUT` if we want to update all the information.
    <br />

6. How do you make a defalut value in a schema?<br />
    We can simply use `default` and set it to the default value.
    <br />

7. What does a 500 error status code mean?<br />
    It means that the actual server (DataBases in crud apps) had some kind of error which caused the actual transaction not to work and it had nothing to do with the actual user using the API.
    <br />

8. What is the difference between a status 200 and a status 201?<br />
    `201` status means an object is successfully created and it's more specific then the default status code `200` which only means everything was successful.

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)