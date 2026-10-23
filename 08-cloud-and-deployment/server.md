# Servers

A server is software or a computer that provides services or resources to other programs, often called clients.

## What you'll learn

- How clients and servers communicate
- The difference between server hardware and server software
- What it means to deploy an application

## Explore further

Learn how cloud platforms provide computing resources in [cloud computing](cloud.md).

## Curiosity Questions

91. Where does your application actually run after deployment?

   It runs on infrastructure selected for the deployment: for example, a
   physical or virtual server, a container platform, a managed application
   service, or a user's device. A cloud provider manages some underlying
   resources, but the application's processes still execute on physical
   computers somewhere.

95. What is a server?

   A server is a program that provides a service to clients; the word is also
   used for the computer running that program. A web server, for example,
   accepts network requests and returns responses. One machine can run many
   server programs, and one service can span many machines.

98. What happens when a server crashes?

   Requests to that instance may fail or time out, and any unsaved in-memory
   state may be lost. A supervisor or orchestrator can detect the failure and
   restart it; a load balancer can route new requests to healthy instances.
   Replication and backups help protect data, but recovery depends on the
   system's design.

### Rabbit Hole

5. When I upload a photo to Instagram, where does that photo actually go?

   The app sends the image, usually in an HTTPS request, to an upload service.
   The service authenticates and validates it, may resize or scan it, then
   stores image data in object storage and saves metadata and ownership in a
   database. A content-delivery network may cache renditions near viewers.
   The exact architecture is private to the service and can change; a
   successful upload response means the service accepted the upload, not
   necessarily that every replica or cache already has it.
