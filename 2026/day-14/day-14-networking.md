OSI Model (7 Layers)
-----------------------------

 Physical 
 Data Link 
 Network
 Transport 
 Session 
 Presentation
 Application 

 TCP/IP Model (4 Layers)
 -----------------------------
 Link Layer – Physical + Data Link
 Internet Layer – IP addressing and routing
 Transport Layer – TCP/UDP communication
 Application Layer – User protocols (HTTP, DNS)

 Hands-on Checklist
 ------------------------------
 Identity
 Command: hostname -I
 Observation: It shows which IP address has been assigned to your system and confirms that the machine is properly connected to the network.
 -------------------------------
 Reachability
 Command: ping <target>
 Observation:This command checks if the other system is reachable. It also shows how fast the reply comes and if any data is lost.
 --------------------------------
 Path
 Command: traceroute <target>
 Observation: This command shows the path to the destination and helps find where the network is slow or not responding.
 ---------------------------------
 Ports
Command: ss -tulpn 
Observation: This command shows which services are running on the system and the port numbers they are using to accept connections.
----------------------------------
Name Resolution
Command: dig <domain> 
Observation: This command is used to find the IP address of a domain name.
-----------------------------------
HTTP Check
Command: curl -I 
Observation: This command checks if the website or web server is responding and shows the HTTP status code.
------------------------------------
Connections Snapshot
Command: netstat -an | head
Observation: It shows all active network connections and the ports that are listening for incoming connections.
  
 
