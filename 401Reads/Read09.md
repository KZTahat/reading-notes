# Read 09

## Authorization/Authentication

1. What header(s) are used in authentication and authorization<br />
    The WWW-Authenticate and Proxy-Authenticate response headers define the authentication method that should be used to gain access to a resource. They must specify which authentication scheme is used, so that the client that wishes to authorize knows how to provide the credentials.<br />

2. What is safe to put into a JWT<br />
    A JWT needs to be stored in a safe place inside the user's browser. ... To keep them secure, you should always store JWTs inside an httpOnly cookie. This is a special kind of cookie that's only sent in HTTP requests to the server. It's never accessible (both for reading or writing) from JavaScript running in the browser.<br />

3. How are JWTs validated<br />
    To parse and validate a JSON Web Token (JWT), we can:
    - Use any existing middleware for your web framework.<br />
        Many web frameworks, such as ASP.NET Core, include JWT middleware that handles JWT validation. Typically, this is the best route to take because the middleware integrates well with the framework's overall authentication mechanisms.<br />

    - Choose a third-party library from JWT.io<br />
        If you choose a third-party library, choose a library that supports the signing algorithm you selected when you registered your application or API with Auth0. Also, be aware that not all libraries validate all JWT claims. At JWT.io, you can see which validations each library supports (look for the green check marks).<br />

    - Manually implement checks <br />
        To validate a JWT, your application needs to:<br />
        - Check that the JWT is well formed.
        - Check the signature.
        - Check the standard claims.
        - If any of these steps fail, then the associated request must be rejected.

## Terminology

- RBAC: Role-based access control is a method of restricting network access based on the roles of individual users within an enterprise.<br />

- User Roles: it is what the user is supposed to do in an organization, what are his/her duties.<br />

- JWT Token: JSON Web Token (JWT) access tokens conform to the JWT standard and contain information about an entity in the form of claims. They are self-contained therefore it is not necessary for the recipient to call a server to validate the token.<br />

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)