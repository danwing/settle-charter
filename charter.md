# Charter for SEcure access To Tls Local rEsources (SETTLE) Working Group

# Background

Servers on local networks have historically settled for unencrypted
communications -- printers, routers, and SMB file sharing.
However, with the advent of HTTPS everywhere, browsers disadvantage
unencrypted communications by requiring a secure context (generally
HTTPS) for features such as Service Workers, Web Bluetooth, WebCrypto,
WebTransport, and more. This increases the importance of a secure
context to local domains. Other local services such as SMB file sharing and
printing would also benefit from encrypted communications for integrity and
privacy.

Today, a secure communication channel is established using TLS with a PKIX
certificate signed by a Certification Authority (CA) that is trusted
by the client.

However, servers on a local network cannot easily get PKIX
certificates signed by a CA because: they are not
directly reachable from the outside (due to firewall or Network Address
Port Translation (NAPT)), lack of domain name delegation, and ongoing
certificate renewal.

# Goals

A primary goal of SETTLE WG is to provide implementation and operational
guidance to obtain a secure context with servers operating within a local
network.

If the primary goal can only be achieved through protocol extensions or modifications,
the SETTLE WG will coordinate with relevant IETF WGs for those protocol changes. Likewise,
the SETTLE WG will actively seek for review by relevant WGs if specific protocol
profiling is needed to meet the WG's primary goal.

In order to increase deployability for key services within local networks, the SETTLE WG
might consider assessing the applicability of the guidance for a few services.

# Program of Work

The SETTLE WG is expected to:

* Develop a document describing the problem, prior attempts to solve the problem, and deployment
issues.

* Develop a requirements document that balances existing browsers behavior with the WG's primary goal.

* Develop operational guidance for deployment of a system that meets the WG's primary goal.

* Develop applicability of the operational guidance to key applications that might be selected by the WG.

# Coordination

The working group will coordinate as necessary with W3C, GSMA, CSA, among others.

# Milestones

07/25: Send Liaisons to a set of identified organizations about SETTLE

09/25: Submit "SETTLE Problem Space and Deployment Issues" to the IESG for publication

12/25: Submit "SETTLE Requirements" to the IESG for publication

04/25: Submit "SETTLE Operational Guidance" to the IESG for publication

06/26: Submit "SETTLE Applicability Document" to the IESG for publication

08/26: Close or recharter the WG
