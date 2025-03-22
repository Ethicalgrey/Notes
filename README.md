# Notes
An archive of my notes to hopefully help others.


## Active Directory
### LLMNR Poisioning with Responder

<ins>What is LLMNR?</ins>
  - LLMNR (Link-Local Multicast Name Resolution) is a protocol used by Windows systems to resolve hostnames to IP addresses on local networks, primarily in environments where a DNS server isn't available or DNS fails.

  - It allows devices to resolve names of other devices on the same local network without relying on a DNS server.

  - NBT-NS (NetBIOS Name Service) is an older protocol that was previously used for the same purpose. LLMNR was introduced as a replacement for NBT-NS.

  - Key flaw: LLMNR, like NBT-NS, is susceptible to poisoning attacks because it allows attackers to respond to LLMNR queries with fake responses, often capturing sensitive data such as usernames and NTLMv2 hashes. When a system makes a request for a name resolution and the attacker responds with a forged response, the system may inadvertently send authentication information (NTLMv2 hash) to the attacker.

### Responder

<ins>What is Responder?</ins> 
- It is most commonly used to exploit vulnerabilities in protocols like LLMNR (Link-Local Multicast Name Resolution), NBT-NS (NetBIOS Name Service), and MDNS (Multicast DNS), as well as other services that Windows systems rely on for name resolution and authentication.
