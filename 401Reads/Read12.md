# Read 12

## Socket.io

1. What is the benefit of transforming data into packets?<br />
    Data is divided into packets because it makes the network more efficient. It allows the network to balance the load across various pieces of equipment on a millisecond-by-millisecond basis.<br />

2. UDP is often refereed to as a connectionless protocol. Why is this?<br />
    Because there is no virtual connection between sender and receiver<br />

3. Can a socket server application have multiple socket connections?<br />
    Multiple connections on the same server can share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs, and the server would be able to handle as many clients as available as system resources allow it to.<br />

4. Can a socket connection application be connected to multiple socket servers?<br />
    yes, like when a client is talking to multiple servers, it is using multiple ports on the client machine.

5. Can an application be both a socket server and a socket connection?<br />
    if multiple servers can interact between each other, then yes an application be both a socket server and a socket connection. yet I'm not sure.

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)