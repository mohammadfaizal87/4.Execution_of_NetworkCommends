# 4.Execution_of_NetworkCommands
## NAME : MOHAMMAD FAIZAL SK
## REGISTER NUMBER : 212223240092
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>
## PROGRAM 
## PING COMMAND

## CLIENT:
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
```
## SERVER:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```    
## TRACEROUTE COMMAND:
```
from scapy.all import*     
target = ["www.google.com"]     
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
```
## Output
## CLIENT

![image](https://github.com/c-sanjay/4.Execution_of_NetworkCommends/assets/147139405/85db283e-a086-44c5-a2e3-1ca8997f26ad)

## SERVER

![image](https://github.com/c-sanjay/4.Execution_of_NetworkCommends/assets/147139405/3ef29a7a-1d98-457f-b052-2fdf83a6dbbd)

## TRACEROUTE COMMAND
![Screenshot 2024-04-22 135157](https://github.com/c-sanjay/4.Execution_of_NetworkCommends/assets/147139405/88cef99e-d29b-4174-8baf-5910e1e8dd4e)


## Result
Thus Execution of Network commands Performed 
