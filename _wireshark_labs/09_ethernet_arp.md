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
9. The contents of my ARP cache are:
   ```
   ? (192.168.4.1) at 5c:a5:bc:9d:8a:2d on en0 ifscope [ethernet]
   ? (192.168.7.187) at 7c:9e:bd:5c:5d:80 on en0 ifscope [ethernet]
   ? (192.168.7.255) at ff:ff:ff:ff:ff:ff on en0 ifscope [ethernet]
   mdns.mcast.net (224.0.0.251) at 1:0:5e:0:0:fb on en0 ifscope permanent [ethernet]
   ? (239.255.255.250) at 1:0:5e:7f:ff:fa on en0 ifscope permanent [ethernet]
   ```
10. The hexadecimal value for the source address of the Ethernet frame containing the ARP request message is `00:d0:59:a9:3d:68`. The hex value for the destination address of the frame is `ff:ff:ff:ff:ff:ff`.
11. The hex value for the two-bye frame field is `0x0806`, corresponding to ARP.
12. The ARP opcode field begins at byte 20 (`0x14`) of the Ethernet frame. The value of the opcode field is `0x0001`. The ARP message contains the address of the sender. The "question" in the ARP message appears in the last four bytes of the request (the Target IP address field).
13. The ARP opcode field begins at byte 20 (`0x14`) of the Ethernet frame. The value of the opcode field is `0x0002`. The "answer" in the ARP message appears in bytes 22-27 of the Ethernet frame (the Sender MAC address/HA field).
14. The hexadecimal values of the source and destination addresses of the ARP reply message are `00:06:25:da:af:73` and `00:d0:59:a9:3d:68` respectively.
15. There may be no reply to the second ARP request because the IP address requested has been disconnected from the network.
