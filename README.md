# 4.Execution_of_NetworkCommands
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

## PROGRAM:
```
Developed by : SUDHIR KUMAR .R
Register number : 212223230221
```
## PING COMMAND:
## CLIENT.PY:
```
import socket
from pythonping import ping
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 hostname=c.recv(1024).decode()
 try:
  c.send(str(ping(hostname, verbose=False)).encode())
 except KeyError:
  c.send("Not Found".encode())

```
## SERVER.PY:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 ip=input("Enter the website you want to ping ")
 s.send(ip.encode())
 print(s.recv(1024).decode())
```

## OUPUT:
## PING COMMAND:
## CLIENT.PY:

![321236192-41eb4864-16eb-4aea-bba2-04e4d6a56c89](https://github.com/Sudhirr5/4.Execution_of_NetworkCommends/assets/139332214/bce0207b-21bc-4bc1-ab0e-836f573e1fbd)


## SERVER.PY:

![321236049-7a11ad22-7731-4413-a825-20c902cbe523](https://github.com/Sudhirr5/4.Execution_of_NetworkCommends/assets/139332214/a5e912f5-512a-4a0d-8343-4a2b0b4a3d41)

## TRACEROUTE COMMMAND:

![321235452-927d7050-6bc8-4304-89aa-c2c7b208e3cb](https://github.com/Sudhirr5/4.Execution_of_NetworkCommends/assets/139332214/aceaae72-cc17-4b31-b06e-21a3cae5300e)

## Result
Thus Execution of Network commands Performed 
