# Read 08

## Access Control (ACL)

1. When is Basic Authorization used vs. Bearer Authorization?<br />
    when we want to give the user limited access (scopes) to the data without giving away or using the username and the password once again we use Bearer Authorization, and if we want a secure application as well because Basic authentication transmits credentials as user ID/password pairs, encoded using base64 where it's reversible encoding.

2. What does the JSON Web Token package do?<br />
    defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed, so it can generate the json token, compare between two tokens and we can access and have some authority with this token.

3. What considerations should we make when creating and storing a SECRET?<br />
    - Never store unencrypted secrets in .git repositories.
    - Don’t share your secrets unencrypted in messaging systems like slack.
    - Use encryption to store secrets within .git repositories like environment variables.
    - Restrict API access and permissions. 

## Terminology:
- encryption : Encryption is the process of taking plain text, like a text message or email, and scrambling it into an unreadable format — called “cipher text.”<br />
- token : Crypto tokens are a type of cryptocurrency that represents an asset or specific use and resides on their blockchain. Tokens can be used for investment purposes, to store value, or to make purchases.<br />
- bearer : Bearer authentication (also called token authentication) is an HTTP authentication scheme that involves security tokens called bearer tokens.<br />
- secret : In cryptography, a secret is a piece of data, known only to the parties involved, in a secure communication. The secret can be a password, a passphrase, a big number, or an array of randomly chosen bytes.
JSON Web Token

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)