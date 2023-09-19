---
title: DHCP
layout: collection_doc
---

1. The address of my host is 192.168.4.27. The address of the destination host is 143.89.12.134.
2. ICMP packets do not have port numbers because it is a network-layer protocol, not a transport-layer protocol. The packets do not contain any application-layer data, like TCP or UDP datagrams do, so there is no need for port numbers to determine what application or service to send data to.
3. Type: 8 (Echo (ping) request), Code: 0. Other fields are: Checksum, Identifier, Sequence Number, Timestamp, and Data. Checksum, Identifier, and Sequence Number are two bytes each.
4. Type: 0 (Echo (ping) reply), Code: 0. Other fields are: Checksum, Identifier, Sequence Number, Timestamp, and Data. Checksum, Identifier, and Sequence Number are two bytes each.
5. The IP address of my host is 192.168.4.27. The address of the destination host is 128.93.162.83.
6. If `traceroute` sent UDP packets rather than ICMP, the IP protocol number would be 17 rather than 1.
7. The ICMP packets sent by `traceroute` and by `ping` seem the same. The IP headers differ in that `traceroute` sends datagrams with a TTL of 1, then 2, etc, whereas `ping` sets the TTL to 64. The `ping` packets also have normal responses rather than error messages.
8. The ICMP error packet contains fields indicating the type of error and the checksum, and then also wraps the original IP datagram and ICMP message that caused the error.
9. The last three packets received by the source host were normal echo replies, sent in response to three echo requests sent by the source host.
10. For the following output of `traceroute`, it seems clear that the hop from 5 to 6 added significant delay:

```
$ traceroute -I www.inria.fr
traceroute to inria.fr (128.93.162.83), 64 hops max, 72 byte packets
 1  192.168.4.1 (192.168.4.1)  3.648 ms  1.772 ms  2.361 ms
 2  lo0-100.washdc-vfttp-312.verizon-gni.net (100.36.55.1)  2.863 ms  9.335 ms  9.771 ms
 3  ae1312-20.washdcdn-mse01-aa-ie1.verizon-gni.net (100.41.21.150)  10.219 ms  7.896 ms  9.911 ms
 4  * * *
 5  verizon-com.customer.alter.net (204.148.11.238)  10.347 ms  34.033 ms  45.312 ms
 6  et-3-3-0.cr2-par7.ip4.gtt.net (213.200.119.214)  82.324 ms  87.042 ms  89.234 ms
 7  renater-gw-ix1.gtt.net (77.67.123.206)  89.150 ms  87.712 ms  108.891 ms
 8  te1-1-inria-rtr-021.noc.renater.fr (193.51.177.107)  88.586 ms  83.443 ms  89.441 ms
 9  inria-rocquencourt-gi3-2-inria-rtr-021.noc.renater.fr (193.51.184.177)  88.132 ms  88.069 ms  88.151 ms
10  unit240-reth1-vfw-ext-dc1.inria.fr (192.93.122.19)  88.383 ms  82.253 ms  89.722 ms
11  prod-inriafr-cms.inria.fr (128.93.162.83)  88.459 ms  84.610 ms  90.015 ms
```

Based on the hostnames given, we can infer that router 9 is located in Rocquencourt, which is in fact the location of INRIA.
