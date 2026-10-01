A background [[daemons|daemon]] that [[GnuPG]] uses for all network-related operations, like:

- 🔑 Fetching keys
- 🔏 Resolving and verifying certificates
- 🌐 Looking up keys via Web Key Directory (WKD)
- etc.

Think of it as GnuPG’s *network butler* - GPG itself doesn’t open sockets or handle TLS directly; it asks `dirmngr` to do it.