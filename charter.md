# Charter for SEcure access To Tls Local rEsources (SETTLE) Working Group

# Background

Servers on local networks have historically settled for unencrypted
communications -- printers, routers, and SMB file sharing.
However, with the advent of HTTPS everywhere, browsers disadvantage
unencrypted communications by requiring a [secure context](https://www.w3.org/TR/secure-contexts)
for features such as Service Workers, Web Bluetooth, WebCrypto,
WebTransport, and more. This increases the importance of a secure
context to local domains. Non-HTTP protocols such as SMB3 encrypted
file sharing would benefit from stronger server authentication and
printing (IPP over HTTPS) would benefit from encrypted communications.

Today, a secure communication channel is established using TLS with a PKIX
certificate signed by a public Certification Authority (CA) that is trusted
by the client.

However, servers on a local network cannot easily get PKIX
certificates signed by a public CA because:

  * they are not directly reachable from the outside (due to firewall or Network Address
Port Translation (NAPT))
  * lack of domain name delegation, and
  * ongoing certificate renewal.

Due to those challenges, if a local server does have have a
certificate it won't have a public DNS name or have a certificate
signed by a public CA.  When connecting, the user will receive a
certificate warning -- sometimes each time the user connects to the
server.  Over time, the user disregards such warnings even when an
attacker has compromised the path or the server, as the client cannot
confidently distinguish an attack.  This is undesirable.


An alternative to a public CA is a locally-installed certificate
authority (also called "private CA" or "enterprise CA").  However, a
locally-installed CA remains complicated for end users because users
are unfamiliar with Certificate Signing Requests, some devices do not
generate Certificate Signing Requests, and users are unfamiliar with
how a CSR can be moved from a device to the local CA, get signed, and
moved back to the device. Repeating this effort across several devices
with different user interfaces and CSR capabilities and repeating it
again every quarter or year (to rotate keys) is not tenable for most
users. The user experience to add a locally-installed Certificate
Authority on a client device also differs by web browser and operating
system.  Further, adding a Certificate Authority enables interception
of TLS-encrypted data which makes such a solution untenable when
visiting a less-trusted network (e.g., hotel, library) even if there
are useful local hosts (e.g., printer).

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
