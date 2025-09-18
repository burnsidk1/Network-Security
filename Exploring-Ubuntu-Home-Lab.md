1) ifconfig 
Used to show all network interfaces and their IP addressed. These command helps to identify which interfaces are currently active and their statuses. 
https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/1%20-%20Identify%20Network%20Interfaces%20and%20IP%20Addresses.png

2) sudo netstat -tuln 
Can be used to identify all of the open ports and their services. This helps to identify which ports don't need to be open and are therefore potential vulnerabilities. Shows network connections, routing tables and interface information.
![<Network Security>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/2%20-%20Check%20Open%20Ports.png)

3) sudo lsof -i -P -n
Lists all open connections to the system. This can help someone identify unathorized connections. "lsof" stands for "list open files".
https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/3%20-%20Analyze%20Network%20Connections.png

4) sudo nmap -sS -O localhost
This command scans the server to find any open ports, as well as operating system information. "-sS" makes the TCP scan stealthy and "-O" means the operating system information is desired. "localhost" can also be replaced with other domains, but only when given explicit permission because it is otherwise illegal to IP scan a website.
https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/4%20-%20Perform%20Network%20Scanning%20with%20Nmap.png

5) sudo nmap -sP 192.168.1.0/24
Uses the "-sP" command which is a ping scan to identify all of the live hosts on a network. This does not require a port scan.
https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/5%20-%20Check%20for%20Open%20Ports%20on%20the%20Server's%20Network.png

6) sudo nmap -sV localhost
Scans open ports to determine what is running on the ports and what version is the service on. "-sV" specifically calls out the service type and version in the scan.
https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/6%20-%20Check%20for%20Services%20and%20Versions.png

7) sudo nmap --script vuln localhost
Uses a built in nmap script that can scan for vulnerabilites on the localhost. "localhost" can also be changed to another domain. "-script vuln" specifically checks for vulnerabilities.
https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/7%20-%20Identify%20Potential%20Vulnerabilities.png

8) sudo tcpdump -i eth0
Can monitor the network traffic passing through a specified network device. "tcpdump" in specific anaylzes the packets.
https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/8%20-%20Inspect%20Network%20Traffic.png

9) sudo watch -n 1 netstat -tulnp
"-n 1" defines that the continously monitored network connection should be updated every 1 second.
https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/9%20-%20Monitor%20Network%20Connections%20in%20Real-Time.png

10) sudo ufw status verbose
"ufw" is used to configure firewalls by showing iptables. The command shows the firewalls configured, and what ports are allowed or blocked.
https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/10%20-%20Check%20Firewall%20Rules.png