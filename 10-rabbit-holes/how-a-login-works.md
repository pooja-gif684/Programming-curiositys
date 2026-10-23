# How a Login Works

A login flow checks a claimed identity, establishes a session, and relies on authorization to protect later actions.

## Follow the trail

1. **Enter credentials:** The user enters a password in the app. The client
   sends it to the service through HTTPS, which protects the connection in
   transit; the app should not log or expose the password.
2. **Verify identity:** The server validates the request, finds the account,
   and verifies the password against a stored salted password hash using the
   appropriate password-hashing algorithm. Rate limits and optional
   multi-factor checks can help resist account attacks.
3. **Create a session:** If verification succeeds, the server creates a
   session or issues a token. The client receives that session proof over the
   protected connection; it should be stored and transmitted using
   appropriate safeguards.
4. **Use the session:** Later requests include the session cookie or token.
   The server validates it, identifies the caller, and separately checks
   whether that caller is authorized to perform the requested action.
5. **End or expire access:** The session expires, is revoked, or is cleared
   when the user logs out. Sensitive actions may require renewed
   authentication.

“Login successful” means the service accepted the authentication step. It
does not mean every subsequent action is allowed, and it should never return
the password to the client.

## Explore further

Learn about [authentication](../07-security/authentication.md), [authorization](../07-security/authorization.md), and [password hashing](../07-security/hashing.md).
