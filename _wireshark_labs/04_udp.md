---
title: UDP
layout: collection_doc
---

1. There are four fields in the UDP header (source port, destination port, length, and checksum).
2. Each field in the UDP header is two bytes long.
3. The value in the Length field is the total length of the packet in bytes including the header, i.e. the length of the data payload + 8 (the length of the header).
4. The maximum number of bytes in a UDP payload is therefore 65527 (that is, the highest number that can be stored in two bytes minus 8 for the header = 0xFFFF - 0x0008 = 65535 - 8).
5. The largest possible source port number is 65535 as the source port field is only two bytes long.
6. The protocol number for UDP is 0x11 = 17.
7. For a pair of UDP messages wherein the second is sent in response to the first, the source and destination port numbers are reversed, e.g. the first packet's source port is 58104 and its destination port is 443, whereas the second packet's source is 443 and its destination is 58104.
