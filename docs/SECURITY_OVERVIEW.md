# Security Posture (Summary)

WebPatrolz has undergone an internal security review covering authentication,
authorization, outbound network requests made by the monitoring engine,
file/upload handling, and rate limiting.

At a high level, the platform follows standard practices for a service that
fetches user-supplied URLs on a schedule, including:

- Authenticated, token-based access with short-lived credentials
- Role-based access control between regular users, organization members,
  and admins
- Input validation on all user-supplied data, including monitor targets and
  integration URLs
- Rate limiting on public and authenticated endpoints
- Standard security headers and TLS enforcement

A full, detailed security audit report — including specific findings,
remediations, and known/accepted residual risk — is maintained internally
and is available to qualified partners and investors under NDA.

## Responsible disclosure

If you believe you've found a security issue with a deployed instance of
WebPatrolz, please report it privately rather than opening a public issue.
_[Add a security contact email here once available.]_
