---
title: NAT
layout: collection_doc
---

1. The IP address of the client is 192.168.1.100
2. --
3. The source address:port of the request is 192.168.1.100:4335 and the destination is 64.233.169.104:80
4. The response is received at 7.158797 with a source of 64.233.169.104:80 and a destination of 192.168.1.100:4335
5. The TCP SYN segment setting up this connection is sent at 7.075657 and has the same source and destination as above. The TCP SYN-ACK segment is received by the client at 7.109053
6. On the ISP side, the first HTTP GET request is made at 6.069168, with a source of 71.192.34.104:4335 and a destination of 64.233.169.104:80, so all are identical to the home side trace except for the source IP address
7. The only fields in the IP datagram to have changed are source address and header checksum. The header checksum must have changed since it is a function of the contents of the rest of the header.
8. The HTTP 200 OK response is received at 6.117570, with a source of 64.233.169.104:80 and a destination of 71.192.34.104:4334, so all are identical to the home side trace except for the destination IP addres.
9. The TCP SYN segment setting up this connection is made at 6.035475 and has the same source and destination as above. The TCP SYN-ACK segment is received by the client at 6.067775

10. NAT translation table

    | WAN side            | LAN side            |
    | ------------------- | ------------------- |
    | 71.192.34.104, 4335 | 192.168.1.100, 4335 |
