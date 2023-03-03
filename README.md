<h1>Configuring a Standard ACL </h1>


<h2>Description</h2>
In this lab, I learned to configure a standard access control list (ACL). ACLs are ordered sets of rules that control the traffic that is permitted or denied the use of a path through a router. These rules can operate at Layer 3, making these decisions on the basis of IP addresses or at Layer 4, when only certain types of traffic are allowed based on a Transmission Control Protocol (TCP) or User Datagram Protocol (UDP) port number. When this is done, the ACL will typically reference a port number of the service or application that is allowed or denied.
<br />



<h2>Environments Used </h2>

- <b>Ubuntu 20.04.2 LTS</b> 

<h2>Utilities and Language </h2>

- <b>PuTTY SSH Client</b>

<h2>Program walk-through:</h2>

<p align="center">
From the left sidebar navigate to PuTTY and enter in your Host Name, port, and connection tyoe and click open<br/>
Now ping the IP address to see if it is reachable <br>
<img src="https://i.postimg.cc/m2bTjKH1/Screen-Shot-2023-03-02-at-11-01-57-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
  
<br />
Open a new PuTTY window and enter in Host Name, port and connection type  <br>
<img src="https://i.postimg.cc/j233zWfX/Screen-Shot-2023-03-02-at-11-03-52-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />



<br />
Enter the following commands<br>
conf t (to configure terminal) <br>
access-list 10 deny host 192.168.2.101 <br>
access-list 10 permit any <br>
interface e0/1 <br>
IP access-group 10 out <br>
end <br>
<img src="https://i.postimg.cc/7hjcFGLL/Screen-Shot-2023-03-02-at-11-08-46-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />



<br />
Execute the following command in enable mode to save router settings:<br>
copy running-config startup-config <br>
When asked Destination filename [startup-config]?, press Enter. <br>
Then type in the "show access-lists" command <br>
<img src="https://i.postimg.cc/XqZNKChN/Screen-Shot-2023-03-02-at-11-12-44-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />

  
  
  
<br />
Now ping the IP address from earlier to see if it is reachable in the first PuTTY window<br>
if it isn't than you've done it correctly <br>
<img src="https://i.postimg.cc/zGMfBpPt/Screen-Shot-2023-03-02-at-11-15-50-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
  
  
  
  
