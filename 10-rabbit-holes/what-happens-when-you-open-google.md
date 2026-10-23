# What Happens When You Open Google?

Opening a website brings together networking, name resolution, secure connections, and browser rendering.

## Follow the trail

1. **Interpret the address:** The browser parses `google.com`, applies any
   relevant cached information, and determines which service to contact.
2. **Resolve the name:** A DNS resolver returns records such as IP addresses
   for the domain. The result may vary by location and time.
3. **Route packets:** The device sends packets toward the selected address.
   Local networks, internet providers, and routers forward them hop by hop.
4. **Secure connection:** The browser connects to the service, commonly using
   HTTPS. TLS encrypts traffic and verifies the server's certificate for the
   requested name.
5. **Request and response:** The browser sends an HTTP request. The service
   may route it through proxies and application servers, retrieve data, and
   return an HTTP response.
6. **Render the page:** The browser processes the response and may request
   additional scripts, styles, images, or data before displaying the page.
   Modern sites often make many requests rather than downloading one file.

The exact servers and routes are not fixed: DNS, load balancing, and content
delivery can send different users to different infrastructure.

## Explore further

See [IP addresses](../04-internet/ip.md) and [HTTP](../04-internet/http.md) for more of the network path.
