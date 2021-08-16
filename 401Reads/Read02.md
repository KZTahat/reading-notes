# Read 02
## Express

1. What’s the difference between PUT and PATCH?<br />
    the difference between `PUT` and `PATCH` is that PUT is used for updating the whole object or element while PATCH is used to update only some specific propertys of that object.

2. Provide links to 3 services or tools that allow you to “mock” an API for development like json-server. <br />
    1. `Nock`
        Nock is an HTTPS library designed to replicate and mock servers and expectations in Node.js. Functionally, Nock does this by overriding both the http.request and http.ClientRequest functions, intercepting requests and responding with a specific mocked response through the use of Interceptors.<br />
        Interceptors are addressed in the order they appear on a list, meaning that you can create multiple interceptors that result in different responses to two or more calls. This is especially useful if you’re testing mocked failures or routing, as you can mimic complex server functionality relatively seamlessly.
        <br />
    2. MockServer
        MockServer (and its counterpart service MockServer Proxy) is a multifaceted tool that comes in a variety of builds. It’s available as a Netty web server, a Docker container, a Maven plugin, an npm plugin, and a Grunt plugin. There’s a ton of great options that can be leveraged for a variety of environments. This already makes it a pretty compelling tool given that you can plug it into just about anything you’re running, but its wide range of functionality is the core compelling argument.
        <br />
    3. Beeceptor
        Beeceptor is a great tool largely because it requires absolutely no code in order to utilize it. Beeceptor is a free online tool for mocking a REST API interaction using any HTTP request. You can customize your responses to simulate pretty much any response or failure situation. Beeceptor also offers some great functionality to simulate latency on downstream APIs – you can both simulate transmit latency and timeouts, which is a great use case for many APIs and often missed during testing.
        <br />

3. Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?<br />
    - APIDoc.js :<br />
        `400` : bad request <br />
        `404` : not Found <br />
        `403` : forbidden <br />
        `500` : server error <br />
    - swagger :<br />
        `400` : bad request <br />
        `404` : not Found <br />
        `401` : Unauthorized <br />
        `500` : server error <br />
<br />

4. Compare and contrast SOAP and REST. <br />
    - SOAP stands for Simple Object Access Protocol whereas REST stands for Representational State Transfer.<br />
    - SOAP is a protocol whereas REST is an architectural pattern.<br />
    - SOAP uses service interfaces to expose its functionality to client applications while REST uses Uniform Service locators to access to the components on the hardware device.<br />
    - SOAP needs more bandwidth for its usage whereas REST doesn’t need much bandwidth.<br />
    - Comparing SOAP vs REST API, SOAP only works with XML formats whereas REST work with plain text, XML, HTML and JSON.<br />
    - SOAP cannot make use of REST whereas REST can make use of SOAP.<br />

## Documenting Terms

- `Web Server` : <br />
The term web server can refer to hardware or software, or both of them working together.

1. On the hardware side, a web server is a computer that stores web server software and a website's component files. (for example, HTML documents, images, CSS stylesheets, and JavaScript files) A web server connects to the Internet and supports physical data interchange with other devices connected to the web.<br />

2. On the software side, a web server includes several parts that control how web users access hosted files. At a minimum, this is an HTTP server. An HTTP server is software that understands URLs (web addresses) and HTTP (the protocol your browser uses to view webpages). An HTTP server can be accessed through the domain names of the websites it stores, and it delivers the content of these hosted websites to the end user's device.<br />

- `Express` : Express.js, or simply Express, is a back end web application framework for Node.js, released as free and open-source software under the MIT License. It is designed for building web applications and APIs.<br />

- `Routing` : Routing or router in web development is a mechanism where HTTP requests are routed to the code that handles them. To put simply, in the Router you determine what should happen when a user visits a certain page.<br />

- `WRRC` : ??

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)