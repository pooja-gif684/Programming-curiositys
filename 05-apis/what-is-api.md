# What Is an API?

An application programming interface (API) is a defined way for software components to interact.

## What you'll learn

- How an API describes available operations
- Why interfaces let systems evolve independently
- Examples of APIs in libraries and network services

## Explore further

The [request and response](request-response.md) chapter introduces a common API interaction pattern.

## Curiosity Questions

51. What exactly is an API?

   An API is a defined interface through which one software component can use
   another. It specifies available operations and the data they accept or
   return; an API may be a local library interface or a remote service accessed
   over a network.

52. Why can’t two applications simply access each other’s variables?

   Separate applications usually run in separate process address spaces, so
   one cannot safely read another's memory directly. Even when programs share
   a machine, they may use different languages and internal data layouts.
   APIs provide an explicit, validated contract for exchanging information.

53. What happens when a React application calls a Node.js or Python API?

   The browser code typically serializes request data (often as JSON) and
   sends it over HTTP to the API endpoint. A Node.js or Python server receives
   and validates the request, performs application logic and perhaps queries a
   database, then returns a response. The browser parses that response and
   updates the interface; network failures, authorization, and CORS policies
   can affect the exchange.
