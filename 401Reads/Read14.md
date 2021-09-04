# Read 14

## Event Driven Architecture

1. What’s the difference between a FIFO and a standard queue?<br />
    Standard queues guarantee that a message is delivered at least once and duplicates can be introduced into the queue. FIFO queues ensure a message is delivered exactly once and remains available until a consumer processes and deletes it; duplicates are not introduced into the queue. <br />

2. How can the server be assured a message was properly received?<br />
    a server can never know if a message was properly received by the receiver unless there was some kind of feedback coming from the reciever side telling that the message was properly received like the work way of the TCP model.<br />

3. What classic design pattern is best represented by event driven programming?<br />
    The event-driven architecture pattern is a popular distributed asynchronous architecture pattern used to produce highly scalable applications. ... The event-driven architecture is made up of highly decoupled, single-purpose event processing components that asynchronously receive and process events. <br />

4. How do you test an event driven system?<br />
    service tests for event-driven systems operate on events for inputs and events for outputs. Another by-product of a decoupled architecture is often an absence of mocks and stubs in the service test code, which stems from inherent ‘unawareness’ the service has of other services. <br />


<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)