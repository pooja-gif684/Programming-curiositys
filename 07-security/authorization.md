# Authorization

Authorization determines which actions an authenticated user or system is allowed to perform.

## What you'll learn

- How roles and permissions represent access rules
- The principle of least privilege
- Why authorization checks belong close to protected resources

## Explore further

Review [authentication](authentication.md) to distinguish identifying a user from granting access.

## Curiosity Questions

76. What happens if someone changes an API request?

   The server must treat every request as untrusted, validate its fields, and
   check that the authenticated caller is allowed to perform the requested
   action on the specific resource. If the request is invalid or unauthorized,
   it should reject it without exposing protected data or applying the
   change. Hiding controls in the interface is not an access-control check.

78. How does a server know whether you are authorized?

   It authenticates the request, identifies the principal (such as a user or
   service), and evaluates the relevant permissions and policies for that
   operation and resource. The check should use trusted server-side data and
   happen on every protected action; possession of a valid login session does
   not automatically authorize all actions.
