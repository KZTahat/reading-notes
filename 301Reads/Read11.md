# Read: Class 11

## What is OAuth
1. What is OAuth?<br />
    OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.
    <br />

2. Give an example of what using OAuth would look like.<br />
    The simplest example of OAuth is when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon. You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permission gained from the second website.
    <br />

3. How does OAuth work? What are the steps that it takes to authenticate the user?
    What is OpenID?<br />
    Let’s assume a user has already signed into one website or service (OAuth only works using HTTPS). The user then initiates a feature/transaction that needs to access another unrelated site or service. The following happens (greatly simplified):
    <br />
    1. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.<br />

    2. The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.<br />

    3. The first site gives this token and secret to the initiating user’s client software.<br />
    4. The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).<br />
    5. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.<br />
    6. The user approves (or their software silently approves) a particular transaction type at the first website.<br />
    7. The user is given an approved access token (notice it’s no longer a request token).<br />
    8. The user gives the approved access token to the first website.<br />
    9. The first website gives the access token to the second website as proof of authentication on behalf of the user.<br />
    10. The second website lets the first website access their site on behalf of the user.<br />
    11. The user sees a successfully completed transaction occurring.<br />
    12. OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).
    <br />
    "OpenID is for humans logging into machines, OAuth is for machines logging into machines on behalf of humans."

<br />

## Authorization and Authentication flows
1. What is the difference between authorization and authentication?<br />
    In simple terms, authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to.
    <br />
2. What is Authorization Code Flow?<br />
    1. The user clicks Login within the regular web application.<br />

    2. Auth0's SDK redirects the user to the Auth0 Authorization Server (/authorize endpoint).<br />

    3. Your Auth0 Authorization Server redirects the user to the login and authorization prompt.<br />

    4. The user authenticates using one of the configured login options and may see a consent page listing the permissions Auth0 will give to the regular web application.<br />

    5. Your Auth0 Authorization Server redirects the user back to the application with an authorization code, which is good for one use.<br />

    6. Auth0's SDK sends this code to the Auth0 Authorization Server (/oauth/token endpoint) along with the application's Client ID and Client Secret.<br />

    7. Your Auth0 Authorization Server verifies the code, Client ID, and Client Secret.<br />

    8. Your Auth0 Authorization Server responds with an ID Token and Access Token (and optionally, a Refresh Token).<br />

    9. Your application can use the Access Token to call an API to access information about the user.<br />

    10. The API responds with requested data.
    <br />

3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?<br />
    The PKCE-enhanced Authorization Code Flow introduces a secret created by the calling application that can be verified by the authorization server; this secret is called the Code Verifier. Additionally, the calling app creates a transform value of the Code Verifier called the Code Challenge and sends this value over HTTPS to retrieve an Authorization Code. This way, a malicious attacker can only intercept the Authorization Code, and they cannot exchange it for a token without the Code Verifier.
    <br />

4. What is Implicit Flow with Form Post?<br />
    As an alternative to the Authorization Code Flow, OAuth 2.0 provides the Implicit Flow, which is intended for Public Clients, or applications which are unable to securely store Client Secrets. While this is no longer considered a best practice for requesting Access Tokens, when used with Form Post response mode, it does offer a streamlined workflow if the application needs only an ID token to perform user authentication.
    <br />

5. What is Client Credentials Flow?<br />
    1. Your app authenticates with the Auth0 Authorization Server using its Client ID and Client Secret (/oauth/token endpoint).<br />

    2. Your Auth0 Authorization Server validates the Client ID and Client Secret.<br />

    3. Your Auth0 Authorization Server responds with an Access Token.<br />

    4. Your application can use the Access Token to call an API on behalf of itself.<br />

    5. The API responds with requested data.
    <br />

6. What is Device Authorization Flow?<br />
    1.The user starts the app on the device.<br />

    2. The device app requests authorization from the Auth0 Authorization Server using its Client ID (/oauth/device/code endpoint).<br />

    3. The Auth0 Authorization Server responds with a device_code, user_code, verification_uri, verification_uri_complete expires_in (lifetime in seconds for device_code and user_code), and polling interval.<br />

    4. The device app asks the user to activate using their computer or smartphone. The app may accomplish this by:<br />

        - asking the user to visit the verification_uri and enter the user_code after displaying these values on-screen<br />

        - asking the user to interact with either a QR Code or shortened URL with embedded user code generated from the verification_uri_complete<br />

        - directly navigating to the verification page with embedded user code using verification_uri_complete, if running natively on a browser-based device<br />

    5. The device app begins polling your Auth0 Authorization Server for an Access Token (/oauth/token endpoint) using the time period specified by interval and counting from receipt of the last polling request's response. The device app continues polling until either the user completes the browser flow path or the user code expires.<br />

    6. When the user successfully completes the browser flow path, your Auth0 Authorization Server responds with an Access Token (and optionally, a Refresh Token). The device app should now forget its device_code because it will expire.<br />

    7. Your device app can use the Access Token to call an API to access information about the user.<br />

    8. The API responds with requested data.

<br />

7. What is Resource Owner Password Flow?<br />
    1. The user clicks Login within the application and enters their credentials.<br />

    2. Your application forwards the user's credentials to your Auth0 Authorization Server (/oauth/token endpoint).<br />

    3. Your Auth0 Authorization Server validates the credentials.<br />

    4. Your Auth0 Authorization Server responds with an Access Token (and optionally, a Refresh Token).<br />

    5. Your application can use the Access Token to call an API to access information about the user.<br />

    6. The API responds with requested data.<br />

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)