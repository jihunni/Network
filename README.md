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

	
