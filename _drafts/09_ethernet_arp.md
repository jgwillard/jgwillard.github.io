---
title: Ethernet and ARP
layout: collection_doc
---

1. The 48-bit Ethernet address of my computer is 9c:f3:87:a4:33:aa (Apple_a4:33:aa).
2. The 48-bit Ethernet destination address is 5c:a5:bc:9d:8a:2d (eero_9d:8a:2d). This address belongs to my router.
3. The hex value of the two-byte frame field is 0x8000. This corresponds to IPv4.
4. The ASCII "G" (0x47) in GET appears in the 55th byte (zero-indexed byte 54, 0x36) from the beginning of the frame.
5. The value of the source address is 5c:a5:bc:9d:8a:2d, which belongs to my router.
6. The value of the destination address is 9c:f3:87:a4:33:aa, which belongs to my computer.
7. The hex value of the two-byte frame field is 0x8000. This corresponds to IPv4.
8. The ASCII "O" (0x4f) in OK appears in the 68th byte (zero-indexed byte 67, 0x43) from the beginning of the frame.
