# Charter for Working Group

# Background

Servers on local networks have historically settled for unencrypted
communications -- printers, routers, network attached storage (NAS).
However, with the advent of HTTPS everywhere {{everywhere}}, browsers
disadvantage unencrypted communications by requiring a secure context
(generally HTTPS) for features such as Service Workers, Web Bluetooth,
WebCrypto, WebTransport, and more.  This increases the importance of a
secure context to local domains.

Today, a secure context is obtained with a PKIX certificate ({{?RFC5280}})
signed by a Certification Authority (CA) that is trusted by the client.

However, servers on a local network cannot easily get PKIX
certificates signed by a Certification Authority because: they are not
directly reachable from the outside (due to firewall or NAPT), lack of
domain name delegation, and ongoing certificate renewal.

# Goals

Primary goal is to provide implementation guidance to browsers to obtain a secure context
with servers operating within a local network.

If the primary goal can only be acheived through protocol extensions
or modifications, this working group will coordinate with other IETF
working groups for those protocol changes.


# Program of Work

The working group is expected to:

* develop a document describing the problem, prior attempts to solve the problem, and deployment
issues

* develop a requirements document that balances existing browser behavior with the working group's primary goal.

* develop operational guidance for deployment of a system that meets the working group's primary goal.


# Coordination

The working group will coordinate with W3C and GSMA as necessary.
