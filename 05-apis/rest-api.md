# REST APIs

REST is an architectural style for networked systems; web APIs described as REST commonly expose resources over HTTP.

## What you'll learn

- How resources and representations are used
- How HTTP methods can express operations
- Why real-world APIs may follow REST principles to varying degrees

## Explore further

Review [request and response](request-response.md) for the underlying interaction pattern.

## Curiosity Questions

57. What are HTTP methods?

   HTTP methods describe the intended action for a request. Common methods
   include `GET` to retrieve a representation, `POST` to submit data or create
   an operation, `PUT` to replace a resource, `PATCH` to partially update it,
   and `DELETE` to remove it. Servers define the actual behavior and must
   validate requests.

58. Why do we have `GET`, `POST`, `PUT`, `PATCH`, and `DELETE`?

   Distinct methods make an API's intended operations easier to understand
   and allow HTTP clients, caches, and intermediaries to follow consistent
   rules. `GET` is intended to be safe, and `PUT` and `DELETE` are defined as
   idempotent; `POST` is not inherently idempotent. These semantics help
   clients decide when requests may be cached or retried.

77. What is CORS?

   Cross-Origin Resource Sharing is a browser-enforced mechanism that lets a
   server state which web origins may read its responses. For some
   cross-origin requests, the browser first sends a preflight request. CORS is
   not authentication and does not stop non-browser clients from contacting
   an API; servers still need proper access control.
