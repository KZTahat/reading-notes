# Read 16

## Cloud Servers

1. Describe the Web-Request-Response-Cycle<br />
   The request/response cycle traces how a user’s request flows through the app. Understanding the request/response cycle is helpful to figure out which files to edit when developing an app (and where to look when things aren’t working).

   <img src="https://content.codecademy.com/projects/3/request-response-cycle-static.svg"
       alt="code-challenge-2 whiteBoard"
       style="float: left; margin-right: 10px;" />

   1. A user opens his browser, types in a URL, and presses Enter.
   2. When a user presses Enter, the browser makes a request for that URL.
   3. The request hits the Rails router (config/routes.rb). The router maps the URL to the correct controller and action to handle the request.
   4. The action receives the request and passes it on to the view.
   5. The view renders the page as HTML.
   6. The controller sends the HTML back to the browser. The page loads and the user sees it.

   In this way, the request/response cycle is a useful way to see how a Rails app’s files and folders are for and how they fit together.

2. Explain what a “server” is, as it relates to the WRRC <br />
   A server is a computer or system that provides resources, data, services, or programs to other computers, known as clients, over a network. it also handle the requests coming from the client with the appropriate response. In theory, whenever computers share resources with client machines they are considered servers. ... This means that a device could be both a server and a client at the same time.

3. What does it mean to “deploy” an application?<br />
   Software deployment refers to the process of running an application on a server or device. A software update or application may be deployed to a test server, a testing machine, or into the live environment, and it may be deployed several times during the development process to verify its proper functioning and check for errors. Another example of software deployment could be when a user downloads a mobile application from the App Store and installs it onto their mobile device.<br />

## Terminologies

- `Server`: A server is a computer or system that provides resources, data, services, or programs to other computers, known as clients, over a network.
- `Pub/Sub` : Publish/subscribe messaging or pub/sub messaging, is a form of asynchronous service-to-service communication used in serverless and microservices architectures.
- `WRRC` : ??

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)
