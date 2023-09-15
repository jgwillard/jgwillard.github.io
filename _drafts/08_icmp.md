1. The address of my host is 192.168.4.27. The address of the destination host is 143.89.12.134.
2. ICMP packets do not have port numbers because it is a network-layer protocol, not a transport-layer protocol. The packets do not contain any application-layer data, like TCP or UDP datagrams do, so there is no need for port numbers to determine what application or service to send data to.
3. Type: 8 (Echo (ping) request), Code: 0. Other fields are: Checksum, Identifier, Sequence Number, Timestamp, and Data. Checksum, Identifier, and Sequence Number are two bytes each.
4. Type: 0 (Echo (ping) reply), Code: 0. Other fields are: Checksum, Identifier, Sequence Number, Timestamp, and Data. Checksum, Identifier, and Sequence Number are two bytes each.
