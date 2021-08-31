# Read 13

## Message Queues

1. What does it mean that web sockets are bidirectional? Why is this useful?<br />
    WebSockets allow for full-duplex bidirectional communication. This enables the server to send real-time updates asynchronously, without requiring the client to submit a request each time.<br />

2. Does socket.io use HTTP? Why?<br />
    Even when websockets can be used, the initial connection setup it done over HTTP. Also, a socket.io server will attach to an HTTP server so it can serve its own client code through. <br />

3. What happens when a client emits an event?<br />
    client side emits will trigger the events which are listening to a specific keyword in the server side, causing some functions (handle functions) to run and handle that event with whatever code.

4. What happens when a server emits an event?<br />
    server side emits will send a message to all the connected clients who are listening to this event, causing some functions to be executed. <br />

4. What happens if a client “misses” an event?<br />
    if a client misses an event the message will be stored in the message queue in memory or on database or maybe on icloud, then once that client reconnect the queue will resend the messages he missed.<br />

5. How can we mitigate this?<br />
    after the resend of missed messages occurs, the queue will delete all the messages.<br />

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)