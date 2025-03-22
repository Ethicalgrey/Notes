# Notes
An archive of my notes to hopefully help others.


## Active Directory
#### LLMNR/NBTS Poisioning with Responder

**1. What is LLMNR?**
  - LLMNR: Link-Local Multicast Name Resolution.
  - Used to identify hosts when DNS fails to do so.
  - Previously NBT-NS (NetBIOS Name Service)
  - Key flaw is that the services utilize a user's username and NTLMv2 hash when appropriately responded to.
