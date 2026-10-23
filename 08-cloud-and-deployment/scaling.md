# Scaling

Scaling changes a system's capacity to handle workload, either by increasing resources on a machine or adding machines.

## What you'll learn

- The difference between vertical and horizontal scaling
- Why load balancing and data storage affect scaling
- How to recognize trade-offs in a growing system

## Explore further

Start with [servers](server.md) and [cloud computing](cloud.md) for the infrastructure context.

## Curiosity Questions

92. What happens when one user uses your application?

   A client sends a request to the application, which runs its code, may read
   or write data, and returns a response. Even one user's request travels
   through several layers—device, network, server, and possibly database—so
   reliability, security, and latency already matter.

93. What changes when one million users use it?

   More simultaneous requests compete for compute, network, storage, and
   database capacity. Teams may add application instances, distribute traffic,
   cache repeated reads, partition or replicate data, and monitor bottlenecks.
   A million registered users is not the same as a million simultaneous
   active users; actual traffic patterns determine capacity needs.

94. Why can’t we simply buy one huge computer?

   A larger single machine has limits and can become expensive, difficult to
   upgrade, or a single point of failure. Distributing work across machines
   can increase capacity and resilience, but adds network delays,
   coordination, and operational complexity. Some workloads still fit best
   on one well-sized machine.

99. How does Netflix, YouTube, or Instagram handle millions of users?

   At a high level, large services distribute traffic across many servers,
   cache content near users, separate systems into services, and use
   replicated data stores and monitoring. Video services deliver much media
   through content-delivery networks and adapt quality to connection speed.
   Exact architectures differ and are proprietary; these techniques require
   careful capacity planning and failure handling.

100. If you had to build WhatsApp from scratch, what would you need?

   You would need client apps, identity and contact management, reliable
   message delivery, encrypted transport and end-to-end encryption, message
   storage or queues, push notifications, media storage, key management,
   abuse prevention, backups, and a scalable backend. You would also need
   privacy, security, accessibility, moderation, monitoring, and recovery
   plans. A safe messaging service is a substantial distributed system, not
   just a chat screen and database.

### Rabbit Hole

6. How can millions of people use the same application at the same time?

   The service runs multiple copies of its application across machines and
   routes requests among healthy copies, often using a load balancer.
   Caches reduce repeated work; queues smooth bursts; databases are tuned,
   replicated, or partitioned according to the workload. Teams monitor
   bottlenecks and failures and add capacity as needed. This does not mean
   every user shares one process: the system coordinates many independent
   processes and data stores.
