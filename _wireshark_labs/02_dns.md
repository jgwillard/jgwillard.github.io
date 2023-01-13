---
title: DNS
layout: collection_doc
---

1. 58.229.6.225
2. ns1.u-strasbg.fr., shiva.jussieu.fr., ns2.u-strasbg.fr.
3. Above servers refused to provide IP addresses for yahoo.com, google.com, et al
4. DNS messages are sent via UDP
5. Destination port of request and source port of response are both 53
6. Destination IP address is 71.252.0.12, same as the server used by `nslookup` by default
7. One query of type "A" and one of type "HTTPS" are made; no answers present
8. Response message contains two answers: one type CNAME, one type HTTPS
9. Subsequent TCP SYN packet dest address corresponds to second IP address given by DNS response
10. GET http://www.ietf.org request elicits 301 Moved Permanently response with "Locaction: https://www.ietf.org" after which two more DNS requests are made, one of type A and one of type HTTPS, which appear identical to the requests made previously
11. Destination port of request and source port of response are both 53
12. Destination IP address is 71.252.0.12, the default local DNS server
13. DNS query message is of type "A" and contains no answers
14. DNS response message contains 3 answers: www.mit.edu has a CNAME record pointing to www.mit.edu.edgekey.net, which has a CNAME record pointing to e9566.dscb.akamaiedge.net, which has a type A record pointing to the IP address 104.106.237.16
15. ![DNS response 1](/assets/dns_response_1.png)
16. Destination IP address is 71.252.0.12, the default local DNS server
17. DNS query message is of type "NS" and contains no answers
18. DNS response message provides nameserver dcsb.akamaiedge.net; no IP address is provided
19. ![DNS response 2](/assets/dns_response_2.png)
20. Destination IP address is 2.16.40.64, corresponding to that of an authoritative nameserver for mit.edu, use5.akam.net (command run was `nslookup www.aiit.or.kr use5.akam.net`)
21. DNS query is of type "A" and contains no answers
22. No answers are provided; response was "Refused" (it appears that standard practice is for an authoritative nameserver to respond "Refused" to queries for any domain names for which it is not authoritative; perhaps at the time this lab was created MIT and AIIT shared authoritative DNS servers ([see this ServerFault post](https://serverfault.com/questions/892622/what-rfc-encourages-dns-servers-to-reply-refused-to-queries-for-unknown-domains)). Some geographically close schools did appear to share authoritative nameservers, for example MIT and Harvard, and W&M and ODU)
23. ![DNS response 2](/assets/dns_response_3.png)
