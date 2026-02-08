Networking Concepts: DNS, IP, Subnets & Ports
------------------------------------------------
Task 1: DNS – How Names Become IPs

The browser asks DNS for the IP address of google.com.

DNS finds and returns the IP address of Google’s server.

The browser connects to that IP address over the internet.

Google’s server sends back the website data.

The browser displays the Google homepage.

What are these record types
---------------------------------------------------
A record :- Maps a domain name to an IPv4 address.

AAAA record :- Maps a domain name to an IPv6 address.

CNAME record :- Points one domain name to another domain name.

MX Record :- MX record decides where your domain’s emails are delivered.

NS Record :- which name servers are authoritative and handle DNS queries for a domain.

---------------------------------------------------------
Run: dig google.com

dig is a command-line tool used to query DNS servers and get information about a domain name, such as its IP address and other DNS records.

-----------------------------------------------------
Task 2: IP Addressing

IPv4:- An IPv4 address is a 32-bit number written in four octets separated by dots.

-----------------------------------------------------

Public vs Private IP Address

Public IP Address:-A public IP address is used to communicate over the internet.It is globally unique, meaning no two devices on the internet can have the same public IP at the same time.

Private IP Address:-A private IP address is used inside a local network (home, office, cloud private network).It cannot be accessed directly from the internet.

-----------------------------------------------------
Private IP Address Ranges

These ranges are reserved for private networks:

10.0.0.0 – 10.255.255.255

172.16.0.0 – 172.31.255.255

192.168.0.0 – 192.168.255.255

-------------------------------------------------------

ip addr show:- The ip addr show command displays all network interfaces and their assigned IP addresses on a Linux system. It helps identify private, public, and loopback addresses.

------------------------------------------------------
Task 3: CIDR & Subnetting

What does /24 mean in 192.168.1.0/24?

ANS :- It means 24 bits are used for the network portion of the IP address.

How many usable hosts in a /24? A /16? A /28?

Usable Hosts = 2^(32 − CIDR) − 2

1) 2^(32-24) -2 = 254

2) 65,534

3) 14

Total IPs = 2^(32 − CIDR)
Usable Hosts = 2^(32 − CIDR) − 2


   CIDR	               Subnet Mask	                        Total IPs   	                Usable Hosts
/24	                  255.255.255.0           	               256    	                      254
/16	                  255.255.0.0                            65,536                          65534
/28	                  255.255.255.240                           16                             14

-------------------------------------------------------------

Task 4: Ports – The Doors to Services

A port is a communication endpoint that allows different services to run on the same IP address. Tools like ss -tulpn help identify which services are listening on which ports.

port         service

22---ssh

80----http

443---https

53----DNS

3306---mysql

6379---redis

27017---MongoDB

-----------------------------------------

curl http://myapp.com:8080 :-
DNS converts myapp.com into an IP address.Your system connects to that IP using port 8080 and the HTTP protocol.

Your app can't reach database at 10.0.1.50:3306

Check if the server can reach the IP address on the network.Then check if port 3306 is open and the database service is running.
