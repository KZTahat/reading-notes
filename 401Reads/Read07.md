# Read 07
##  Bearer Authorization

1. Write the following steps in the correct order:<br />
    - Register your application to get a client_id and client_secret
    - Ask the client if they want to sign in via a third party
    - Redirect to a third party authentication endpoint
    - Make a request to a third-party API endpoint
    - Make a request to the access token endpoint
    - Receive access token
    - Receive authorization code

2. What can you do with an authorization code?<br />
    Authorization codes are used for any transaction or entry that has restrictions on which users are entitled to access. For example, a credit card authorization code is a five- or six-number code from the issuing bank to the vendor, that authorizes the sale. If the credit card used is counterfeit or if the card is over its predetermined limit, the credit card company will automatically decline the sale. If approved, the authorization code is attached to the credit card transaction. This signals to the merchant that the transaction is legitimate, while also helping to identify the transaction in follow-up examinations, such as the return of merchandise or purchasing disputes.<br />

3. What can you do with an access token?<br />
    Access tokens are the thing that applications use to make API requests on behalf of a user. The access token represents the authorization of a specific application to access specific parts of a user's data.<br />

4. What’s a benefit of using OAuth instead of your own basic authentication?<br />
    - It enables apps to obtain limited access (scopes) to a user's data without giving away a user's password.<br>
    - It decouples authentication from authorization and supports multiple use cases addressing different device capabilities.<br />
    - It supports server-to-server apps, browser-based apps, mobile/native apps, and consoles/TVs.<br />

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)