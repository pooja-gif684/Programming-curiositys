# IP Addresses

Internet Protocol (IP) addresses identify endpoints used to route packets across networks.

## What you'll learn

- The purpose of IPv4 and IPv6 addresses
- How routers use destination addresses
- Why an IP address is not the same as a domain name

## Explore further

Learn how applications exchange web data in [HTTP](http.md).

## Curiosity Questions

44. What is an IP address?

   An Internet Protocol address identifies a network interface or endpoint for
   packet delivery. IPv4 uses 32-bit addresses and IPv6 uses 128-bit addresses.
   An address can be private or public, and it may change; it identifies a
   network location, not necessarily a person or a permanent device.

45. Why do we need ports?

   An IP address helps deliver packets to a host, while a transport-layer port
   helps direct data to a particular service or socket on that host. For
   example, HTTPS commonly uses port 443. Ports are part of transport
   protocols such as TCP and UDP, not separate physical connectors.

49. How does your request travel thousands of kilometres?

   The networking stack splits data into packets and sends them over physical
   links such as fibre, copper, or radio. Routers forward packets hop by hop
   according to routing information; packets may take different paths and are
   reassembled by the receiving protocols. Latency and reliability depend on
   the route and network conditions.
