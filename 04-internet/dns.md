# DNS

The Domain Name System (DNS) helps translate human-readable domain names into information computers use to find services.

## What you'll learn

- How a DNS lookup finds an answer
- Why DNS uses a distributed hierarchy
- What caching means for name lookups

## Explore further

After a name resolves, [IP](ip.md) explains the addressing used to reach a host.

## Curiosity Questions

41. What happens when you type `google.com` into a browser?

   The browser first interprets the address and may check cached information.
   It resolves the domain to an IP address using DNS, establishes a network
   connection (typically using HTTPS), sends an HTTP request, and renders the
   returned page. A site may involve many additional requests and services.

42. How does your computer find Google’s server?

   DNS provides one or more IP addresses associated with a domain, and IP
   routers forward packets toward those addresses. Large services may use
   several addresses, nearby content-delivery networks, and load balancers, so
   a browser is not necessarily contacting one fixed physical machine.

43. What is DNS?

   The Domain Name System is a distributed, hierarchical naming system that
   lets software look up records such as the addresses associated with a
   domain. Resolvers cache answers for their time-to-live period, reducing
   repeated lookups; DNS does not itself carry the website page.

### Rabbit Hole

3. When I enter `google.com`, how does my computer find another computer
   somewhere in the world?

   The browser asks a DNS resolver for records associated with the domain. The
   resolver may answer from cache or query DNS servers through the hierarchy.
   With an IP address, the device sends packets through its local network and
   internet service provider; routers forward them toward the destination.
   The browser then connects to a service at that address, usually over
   HTTPS. Routing, DNS answers, and service locations can change, and the
   destination may be a proxy or content-delivery network rather than one
   identifiable computer.
