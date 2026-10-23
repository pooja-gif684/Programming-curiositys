# Authentication

Authentication is the process of establishing who or what is making a request.

## What you'll learn

- The difference between identity and proof of identity
- Common factors such as knowledge, possession, and biometrics
- Why secure systems protect credentials and sessions

## Explore further

After identity is established, [authorization](authorization.md) determines permitted actions.

## Curiosity Questions

71. How does a website know who you are after login?

   The website verifies evidence of identity, such as a password plus a
   second factor, then associates a protected session or token with the
   account. Later requests present that session proof so the server can look
   up the account. Sessions expire or can be revoked; a cookie or token is
   evidence of a session, not the user's identity by itself.

72. Where is your password stored?

   A well-designed service does not store the original password. It stores a
   salted password hash produced by a slow, purpose-built algorithm such as
   Argon2id, scrypt, or bcrypt, along with the algorithm parameters needed for
   verification. Passwords should never be logged or stored as plain text.

73. Why shouldn’t passwords be stored as plain text?

   If a database is exposed, plain-text passwords immediately reveal users'
   credentials, which people may have reused elsewhere. A salted,
   deliberately slow password hash makes each guess costly and prevents
   identical passwords from having identical stored values. Hashing does not
   remove the need to secure the database and login system.

79. What is a token?

   A token is a piece of data a client presents to prove or describe some
   authorization, such as a session identifier or signed access token. A
   bearer token can grant access to whoever possesses it, so it must be
   protected in transit and storage, scoped, and expired or revocable as
   appropriate.

80. How can one careless line of code expose millions of users?

   A single mistake can affect a shared boundary: for example, returning
   sensitive fields in an API response, skipping an authorization check, or
   logging a secret. If that code handles every account, the impact can scale
   to every affected user. Layered access controls, code review, testing,
   monitoring, and limiting collected data reduce risk but cannot guarantee
   that mistakes never happen.

### Rabbit Hole

4. When I click Login, how does my password travel from my phone to the server
   and come back as “Login successful”?

   The app sends the credentials to the service over HTTPS, which protects
   them in transit from network observers. The server validates the request,
   compares the submitted password against the stored password hash using the
   same password-hashing scheme, and applies any additional checks such as
   multi-factor authentication or rate limits. On success it creates a
   session or token and returns it securely; the client stores and sends that
   proof on later requests. The password should not be sent back in the
   response, and login success alone does not grant every permission.
