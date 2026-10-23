# Request and Response

In a request-response interaction, one component asks for an operation and another returns a result.

## What you'll learn

- The roles of client and server
- How request data and response data are structured
- How errors and status information are communicated

## Explore further

See [REST APIs](rest-api.md) for one common style of web API design.

## Curiosity Questions

54. What is a request?

   A request is a message asking a service to perform an operation or provide
   information. In HTTP it typically contains a method, a URL path, headers,
   and sometimes a body; it may also carry credentials, which must be protected
   appropriately.

55. What is a response?

   A response is the service's reply to a request. An HTTP response includes a
   status code describing the outcome, headers with metadata, and often a body
   containing data or an error description.

56. Why do APIs commonly use JSON?

   JSON is text-based, supported by many programming languages, and represents
   common data such as objects, arrays, strings, numbers, booleans, and null.
   Its ubiquity makes it convenient for web APIs, though it has limitations
   (for example, no built-in date or binary type) and is not the only format.

59. What happens if an API takes 10 seconds to respond?

   The client waits until it receives a response or its timeout expires; the
   user may see a loading state or delay. A client timeout does not necessarily
   stop server-side work, so retries can accidentally duplicate operations.
   Good APIs and clients use appropriate timeouts, clear progress or error
   states, and safe retry rules.

60. What happens if the API server is completely down?

   Requests may fail to connect or time out, and clients should report that
   the service is temporarily unavailable rather than pretending the action
   succeeded. Systems can use multiple instances, health checks, and
   failover to improve availability, but clients still need to handle failure
   and avoid unsafe repeated writes.
