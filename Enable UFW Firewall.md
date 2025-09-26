1) sudo ufw status
![<1>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Firewall/1.png)

2) sudo ufw allow 22/tcp
![<2>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Firewall/2.png)

Question: If you are remotely accessing your server, why is it important to allow traffic through port 22 before enabling UFW?
* It's important to allow traffic through Port 22 because that is the SSH port. If this port is not allowed, then the firewall will block your connection and you won't be able to access the server.

3) sudo ss -tuln 
![<3>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Firewall/3.png)

4) sudo ufw enable 
![<4>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Firewall/4.png)

5) sudo ufw status
![<5>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Firewall/5.png)

6) Question: Let us say your server is a web server. Which ports should be allowed through in UFW?
* If the server is a web server, ports 80 (HTTP), 443 (HTTPS), and 22(SSH) should be allowed through the UFW at a minimum.

7) sudo ufw status verbose
![<7>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Firewall/7.png)

Question: Any information that looks important or useful?
* It looks like the different allowed ports and version information is useful here.

8) sudo ufw deny from <ip_address>
Screenshot just shows the command you would use.
![<8>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Firewall/8.png)

9) sudo ufw allow from <IP_ADDRESS> to any port <PORT_NUMBER>
![<9>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Firewall/9.png)
Question: What is port 587 typically used for? 
* Port 587 uses the STARTTLS protocol for encrypted email submissions, which is more secure than Port 25.

10) sudo ufw status 
![<10>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Firewall/10.png)