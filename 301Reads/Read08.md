# Read: Class08

## Readings: APIs
### API Design Best Practices

1. What does REST stand for?<br />
    Representational State Transfer (REST).
    <br />

2. REST APIs are designed around resources, which are any kind of object, data, or service that can be accessed by the client.
<br />

3. What is an identifer of a resource? Give an example.<br />
    A resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:`https://adventure-works.com/orders/1`
    <br />

4. What are the most common HTTP verbs?<br />
     The most common operations are GET, POST, PUT, PATCH, and DELETE.
     <br />

5. What should the URIs be based on?<br />
    URIs should be based on nouns (the resource) and not verbs (the operations on the resource).
    <br />

6. Give an example of a good URI.<br />
    `https://adventure-works.com/orders`
    <br />

7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?<br />
    Another factor is that all web requests impose a load on the web server. The more requests, the bigger the load. Therefore, try to avoid "chatty" web APIs that expose a large number of small resources.
    <br />

8. What status code does a successful GET request return?<br />
    HTTP status code 200 (OK).
    <br />

9. What status code does an unsuccessful GET request return?<br />
    HTTP status code 404 (Not Found).
    <br />

10. What status code does a successful POST request return?<br />
    HTTP status code 201 (Created).
    <br />

11. What status code does a successful DELETE request return?<br />
    HTTP status code 204


<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)