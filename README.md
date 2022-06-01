# Network
- client, server
- network protocol
  - IPv4
  - IPv6
  - dynamic IP address
  - static IP address
  - Dynamic Host Configuration Protocol (DHCP): a network management protocol used on Internet Protocol (IP) networks for **automatically** assigning IP addresses and other communication parameters to devices connected to the network using a client–server architecture.
  	- DHCP server, DHCP client, mac address (physical address)
	- Dynamic DNS
- network  
  - local area network (LAN) : private IP address
	- wide area network (WAN) : public IP address
		- Internet Service Provider (ISP)
	- port : 0~65535
		- 0~1023 : well-known port, listening
			- 22 : SSH
			- 80 : http
			- 8080 : web server (custom)
		- port forwarding : WAN -> LAN port
		 	e.g. public_ip:port -> private_ip:port
	- url format :  `scheme://<user>:<password>@<host>:<port>/<url-path>`
- router: Gateway address, router address
	- Network Address Translation (NAT): a method of mapping an IP address space into another by modifying network address information in the IP header of packets while they are in transit across a traffic routing device. 
		![image](https://user-images.githubusercontent.com/48517782/171415044-a9f70b76-b2ed-46f6-82f8-2d9a155ca9ca.png)
	- IP address check
		- window
		- Linux
			```
			$ ifconfig # IP address of a clinent
			$ route # Gateway address, route IP address
			```
		- MacOS 	

## Domain Name System (DNS)
DNS Server
- host : a device that participate in a network
- cliens
- hosts file
- security
- DNS server
- Public DNS
	- `1.1.1.1`, `1.0.0.1`
- DNS Internal, hierarchical
	- blog.example.com.
	- sub, second-level, top-level, root	
	- client -> root DNS name server -> top-level DNS name server -> second-level DNS name server -> sub DNS name server
	- DNS register : Registrant -> registrar (authoritative name server, example.com A 123.456.123.456) -> registry (top-level domain, example.com NS a.iana-servers.net) -> ICANN (root name server, com NS a.gtld-servers.net)
	- client -> DNS Server -> Root name server -> top-level domain -> authoritative name server -> IP address
	- nslookup, dig
		```
		$ nslookup example.com
		$ nslookup -type=a example.com # non-authoriative answer (IP address from cache in DNS server)
		$ nslookup -type=ns example.com
		$ nslookup example.com a.iana-servers.net
		```
	- freenom.com	

