# Charter for SEcure access To Tls Local rEsources (SETTLE) Working Group

# Background

To this day, unencrypted transport to local servers remains common
practice.  Encrypted transport protocols with local servers would
provide strong identity, avoid browser warnings about insecure
connections, and is necessary for some protocols and features (e.g.,
QUIC).

Today, a secure communication channel is established using TLS with a PKIX
certificate signed by a Certification Authority (CA) that is trusted
by the client, either a public CA or a locally-installed CA.

A certificate signed by a public CA requires no changes on clients, but
obtaining such a certificate is difficult because the local server is
not publicly accessible and lacks a domain name.

A locally-installed CA requires user knowledge of Certificate Signing
Requests and requires CSR generation by local servers, and risks TLS
interception as the CA is not constrained to local servers.


# Goals

A primary goal of the SETTLE WG is to provide implementation and operational
guidance to obtain a secure context with HTTP servers operating within a local
network (e.g., router configuration, file transfers, printing).

Protocol changes or extensions remain the responsibility of their relevant
IETF WGs.  Likewise, the SETTLE WG will actively seek for review by
relevant WGs if specific protocol profiling is needed to meet the WG's
primary goal.

As existing client software handles identities using hostnames, the SETTLE WG
should concentrate on unique hostnames.


# Program of Work

The SETTLE WG is expected to:

* Develop a document describing the problem and deployment issues.

* Develop a requirements document that balances existing browsers behavior with the WG's primary goal.

* Develop operational guidance for deployment of a system that meets the WG's primary goal.

* Develop applicability of the operational guidance to key applications that might be selected by the WG.

# Coordination

The working group will coordinate as necessary with W3C, GSMA, CSA, CA/Browser Forum, among others.

# Milestones

TBD

