Data speed measured in kbps (kilobits per second)
KBps = Kilobytes per second(1024 bits/second)
Bi = Bytes
b = bits
<h2>Networking components</h2>
<h4>Hardware</h4>
<h6>Network Interface Card</h6>
add on card plugged in motherboard extension; provides connection between computer & network
<h6>Network Medium</h6>
Cable that plugs into NIC; literally connects computer to network
- can also be wireless
<h6>Interconnecting device</h6>
Allows 2 or more computers to communicate on network without a direct connection
<h4>Software</h4>
<h6>Network client software</h6>
requests information stored on another network device/computer (Web browsers)
<h6>Network server software</h6>
Allows computer to share resources (Servers; i.e Apache webserver)
<h4>Client and Server</h4>
Client: workstation running client OS  or network software on a server that requests network resources from server
- Client Operating system: ClientOS
- Client computer: run user applications and access network resources
- Client software: requests network resources from server software on another computer
Server: computer becomes server when software installed on it provides network service to clients
- Server Operating system: ServerOS designed to provide resources
<h3>Network Protocols</h3>
<i>disclaimer: a lot of these are self written notes; cengage notes suck ass and are outdated</i>

Application accesses network by sending a packet
Client software formats packet; passes it to network protocol
Network protocol parses packet into suitable format; sends to NIC driver
NIC driver sends data to the NIC card; NIC parses packet into appropriate signals
<h3>TCP/IP</h3>
TCP stands for Transmission Control Protocol

| TCP/IP            | Description                                                                                  |
| ----------------- | -------------------------------------------------------------------------------------------- |
| Application       | Application tries to access network resource                                                 |
| Transport         | Client software detects attempt and passes to network protocol                               |
| Internet          | Protocol packages message in a format suitable to network and sends to network driver        |
| Network Interface | Driver sends data to card, converts it into relevant signals to transfer over network medium |
<h4>IP</h4>
Each IP has range of 8 bits, 0-255
Broadcast IP: if communicated to, will send the packet to the entire network
<h6>Private Ip addresses</h6>
These IP addresses are reserved for private networks
- 192.168.0.0 - 192.168.255.255 (65,536 addresses)
- 172.16.0.0 - 172.31.255.255 (1,048,576 addresses)
- 10.0.0.0 - 10.255.255.255 (16,777,216 addresses)

<h6>Subnet: (objects with * may contain wrong info)</h6>
The subnet mask is calculated by the octets that is cut, for example 192.168.1.0/24 the IP is cut at 24 bits because 8 + 8 + 8 = 24<i>*[citation needed]</i>
Max subnet: 30; only 1 usable host and 1 broadcast IP
Netmask IP shows the amount of usable IP addresses

| Type            | Purpose                                                                                     | Explanation                                                                                                   | Example       |
| --------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------- |
| Network Address | Identifies start of actual network, used to identify networks existance                     | For example, a device with the IP address of 192.168.1.100 will be on the network identified by 192.168.1.0   | 192.168.1.0   |
| Host Address    | IP address used to identify a device on subnet                                              | Device may have address of 192.168.1.1                                                                        | 192.168.1.100 |
| Default Gateway | Special address assigned to a device that is capable of sending data to a different network | Data that isn't on same network is sent here. Can use any host address, but usually the first or last address | 192.168.1.254 |

Each step required is referred as a layer; each layer has its own task and works together
TCP/IP uses 2 IP addresses:
- Physical address/ MAC address
- Logical address/ IP address
IP is an identifier for your computer

TCP is connection based protocol, must perform 3 way handshake before any data is sent
When three way handshape completed; stable connection stream established; Any data that is lost or corrupted on transmission is re-sent, thus leading to a connection which appears to be lossless
<h5>3 way handshake</h5>
1) Send a SYN packet request to server
2) Receive ACK
3) Send ACK
4) Receive ACK; start sending deeta![[Pasted image 20240508090013.png]]
![[Pasted image 20240508084915.png]]
<font color="#a0a000"><h4>UDP</h4>
Used for video, constant bit stream; does not need TCP handshake</font>
<h2>LANs WANs and MANs</h2>
<h3>LAN</h3>
Local Area Network, a small network limited to a single collection of machines and connected by one or more interconnecting devices in small geographic area
<h5>Internetwork</h5>
Networked collections of LANs tied together by devices such as routers
Reasons for creation:
- Two or more groups of users & computers are logically seperrated but still need to communicate
- Number of computers on 1 LAN has grown and is no longer efficient
<h3>WAN</h3>
Wide Area Network uses services of third party communication providers to carry network traffic from one location to another(worldwide)
<h3>MAN</h3>
Uses WAN technology to interconnect LANs in a geographic region, suck as country or city(campus)
<h3>Internet, Intranet, Extranet</h3>
- <strong>Internet</strong>- Worldwide public internetwork; uses TCP/IP& HTTP/HTTPS to transfer info
- <strong>Intranet</strong>: private internetwork where devices and servers are only available to users connected to internal network (Internal corporate servers)
- <strong>Extranet</strong>: allows limited and controlled access to internal resources by outside users
<h2>Packets and Frames</h2>
Computers transmit information in short bursts(packets) of around 1.5KiB of data (bursty, not UDP)
<h5>Reasons why data is transferred like this</h5>
- Pauses between bursts allow computer to transmit data between pulses
- Allows receiving computer to process received data
- Allows receiving computer to receive data from other computers at the same time and perform processing tasks
<h3>Packets</h3>
Packet: chunk of data with destination and source IP attached to it
<h4>Frame</h4>
Frame: packet with source & destination IP attached to it
process of adding IP & MAC known as encapsulation
Information added to the front of the data is called a header and information added to the end is called a trailer
<h3>Summary</h3>
- The layers of the network communication process can be summarized as user application, network software, network protocol, and network interface 
- The four terms used to describe networks of different scope are LAN, Internetwork, WAN, and MAN 
- Packets and frames are the units of data handled by different network components 
- Packets have the source and destination IP address added and are processed by the network protocol
- Frames have the MAC addresses and an error code added and are processed by the network interface 
- A client is the computer or network software that requests network data and a server is the computer or network software that makes the network data available to requesting clients
<font color="#00ff00">
<h2>Extra info</h2>
<h4>Encapsulation</h4>
As data is passed down each layer of the model, more information containing details specific to the layer in question is added on to start of transmission. Example: header added by Network Layer would include things like the source and destination IP addresses, and the header added by  Transport Layer would include (amongst other things) information specific to the protocol being used. The data link layer also adds a piece on at the <i>end</i> of the transmission, which is used to verify that the data has not been corrupted on transmission; this also has the added bonus of increased security, as the data can't be intercepted and tampered with without breaking the trailer. This whole process is referred to as <i>encapsulation;</i> the process by which data can be sent from one computer to another.
</font>
<h6>Further Reading:</h6>
https://ptgmedia.pearsoncmg.com/images/9781587204258/samplepages/1587204258.pdf