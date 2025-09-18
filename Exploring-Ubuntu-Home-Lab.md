1) ifconfig 
Used to show all network interfaces and their IP addressed. These command helps to identify which interfaces are currently active and their statuses. 

2) sudo netstat -tuln 
Can be used to identify all of the open ports and their services. This helps to identify which ports don't need to be open and are therefore potential vulnerabilities. Shows network connections, routing tables and interface information.

3) sudo lsof -i -P -n
Lists all open connections to the system. This can help someone identify unathorized connections. "lsof" stands for "list open files".

4) sudo nmap -sS -O localhost
This command scans the server to find any open ports, as well as operating system information. "-sS" makes the TCP scan stealthy and "-O" means the operating system information is desired. "localhost" can also be replaced with other domains, but only when given explicit permission because it is otherwise illegal to IP scan a website.

5) sudo nmap -sP 192.168.1.0/24
Uses the "-sP" command which is a ping scan to identify all of the live hosts on a network. This does not require a port scan.

6) sudo nmap -sV localhost
Scans open ports to determine what is running on the ports and what version is the service on. "-sV" specifically calls out the service type and version in the scan.

7) sudo nmap --script vuln localhost
Uses a built in nmap script that can scan for vulnerabilites on the localhost. "localhost" can also be changed to another domain. "-script vuln" specifically checks for vulnerabilities.

8) sudo tcpdump -i eth0
Can monitor the network traffic passing through a specified network device. "tcpdump" in specific anaylzes the packets.

9) sudo watch -n 1 netstat -tulnp
"-n 1" defines that the continously monitored network connection should be updated every 1 second.

10) sudo ufw status verbose
"ufw" is used to configure firewalls by showing iptables. The command shows the firewalls configured, and what ports are allowed or blocked.