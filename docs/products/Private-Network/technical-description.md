---
sidebar_position: 2
---

# Technical Description

Some more technical details to Contabo's S3 Private Networking feature available as add-on for Cloud VPS / VDS.

## Technology

Contabo's Private Networking feature is build up on additional network connections only interconnected within one single data center. Different physical servers hosting the VPS/VDS are interconnected by Switches. This way we increase the performance for private networking to a maximum. These connections are not shared with the normal (internet) uplink.

We are using scope links (Linux terminology) basically meaning that the traffic of private networks are not routed and thus no gateway is required.

Please be aware that the physical connections for Private Networking are shared resources.

## Limitations

In the following limitations which might not be apparent are described:

* There are no bandwidth guarantees in a private network as it is a shared resource.
* Expect the bandwidth to be multiple times faster than the uplink of your Cloud VPS/VDS.
* Round trip times (latency) will be significantly better. Here an example ping:
  ```sh
  ping 10.0.16.2
  PING 10.0.16.2 (10.0.16.2) 56(84) bytes of data.
  64 bytes from 10.0.16.2: icmp_seq=1 ttl=64 time=0.063 ms
  64 bytes from 10.0.16.2: icmp_seq=2 ttl=64 time=0.069 ms
  64 bytes from 10.0.16.2: icmp_seq=3 ttl=64 time=0.069 ms
  64 bytes from 10.0.16.2: icmp_seq=4 ttl=64 time=0.069 ms
  64 bytes from 10.0.16.2: icmp_seq=5 ttl=64 time=0.073 ms
  64 bytes from 10.0.16.2: icmp_seq=6 ttl=64 time=0.047 ms
  64 bytes from 10.0.16.2: icmp_seq=7 ttl=64 time=0.078 ms
  64 bytes from 10.0.16.2: icmp_seq=8 ttl=64 time=0.069 ms
  64 bytes from 10.0.16.2: icmp_seq=9 ttl=64 time=0.068 ms
  64 bytes from 10.0.16.2: icmp_seq=10 ttl=64 time=0.068 ms
  ```
* Private networks are not spanning across data centers or regions. This is how high performance can be realized.
* If your Cloud VPS/VDS is in the same region the Private Networking system is able to put the Cloud VPS/VDS of one private network at one data center.
* Private Networking is not a firewall solution. The normal uplink is not touched at all. Thus your Cloud VPS/VDS being part of a private network are still connected to the internet. You can use local firewall rules.
