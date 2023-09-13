1. DHCP messages are sent over UDP.
2. The port number for the first four DHCP messages are 68 for the client and 67 for the server.
3. The ethernet address of the host is 00:08:74:4f:36:23.
4. Values present in the DHCP discover message that are not present in the request message are: DHCP Message Type (discover) and DHCP Auto-Configuration. Values present in in the DHCP request message that are not found in the discover message are: DHCP Message Type (request) and DHCP Server Identifier (192.168.1.1). Values present in both are: Client Identifier, Requested IP Address, Host Name, Vendor class identifier.
5. The Transaction ID of the first four messages is 0x3e5e0ce3. The Transaction ID of the following two messages is 0x257e55a3. The Transaction ID serves to ensure that multiple interactions (all of which are broadcast to all hosts on the subnet) do not get mixed together.
6. The client sends messages to the broadcast IP address 255.255.255.255 with a source address of 0.0.0.0. The DHCP server also broadcasts its response to 255.255.255.255 but provides its actual IP address, so the four messages together look like: 0.0.0.0 -> 255.255.255.255, 192.168.1.1 -> 255.255.255.255, 0.0.0.0 -> 255.255.255.255, 192.168.1.1 -> 255.255.255.255.
7. The DHCP server's IP address is 192.168.1.1.
8. The DHCP server offers the IP address 192.168.1.101 in the DHCP Offer Message.
