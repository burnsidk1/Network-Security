1) sudo ufw logging on
![<1>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Logging/1.png)

2) sudo ufw logging high
![<2>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Logging/2.png)

3) Question: Why is the log information useful to us?
* The log information is useful because it shows MAC addresses, source and destination ports/IPs and protocols. It also shows if the UFW is blocking the packet or not. This can help monitor suspicous activity and troubleshoot network issues.

4) sudo tail -f /var/log/ufw.log
![<4>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Logging/4.png)

4) sudo grep 'DENY' /var/log/ufw.log AND sudo grep 'ALLOW' /var/log/ufw.log
![<5>](https://github.com/burnsidk1/Network-Security/blob/main/Screenshots/Enable%20UFW%20Logging/5.png)
Question: Is there any output for 'DENY'? Why or why not?
* There is no output for deny because there is nothing currently being blocked through the UFW.