# HTTP

HTTP is an application-layer protocol used for exchanging requests and responses, especially on the web.

## What you'll learn

- The structure of HTTP requests and responses
- How methods, headers, and status codes are used
- Why HTTP alone does not encrypt communication

## Explore further

See [HTTPS](https.md) for how HTTP can be protected with encryption and authentication.

## Curiosity Questions

46. What is HTTP?

   HTTP is an application-layer protocol for exchanging messages between
   clients and servers. A request includes a method, target, headers, and
   sometimes a body; a response includes a status code, headers, and
   optionally a body. HTTPS protects HTTP traffic with TLS.

48. What happens when you click a button on a website?

   The page's code handles the click, which might update the page locally,
   validate input, or send a request to a server. The server processes the
   request and returns a response; the page then updates based on that result.
   The exact behavior depends on what the button was programmed to do.

50. How does the server know where to send the response?

   The server sends its response over the connection associated with the
   request, so the network stack can deliver it to the requesting client.
   Connection identifiers, transport ports, and protocol state distinguish
   simultaneous communications; application data may also identify a
   particular user or operation.

### Rabbit Hole

10. If the Internet disappeared tomorrow, which parts of your application
    would still work?

   Anything available locally—such as an installed app's interface, cached
   files, and offline features—could still work, depending on its design.
   Features that need remote APIs, cloud databases, online authentication, or
   external assets would fail or become stale. Applications intended for
   offline use can queue changes locally and synchronize them when connectivity
   returns, but must handle conflicts and data protection.
