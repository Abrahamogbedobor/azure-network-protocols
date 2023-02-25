<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools such as PING and IPCONFIG
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used</h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Creating Resource Group
- Creating Virtual Network
- Creating Subnet
- Creating two Virtual Machine on Windows(W-10) and Linus(Ubuntu) Operating System with Network Security Group attached i.e firewall
- Examination of Traffic between both Virtual Machines Using Protocol Analyser (Wireshark)

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/yTmMG7q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
A resource group named RG-LAB was created using UK South as its location as shown above. The next step involves creating VM1, this is because in azure when a virtual machine is created then, virtual network and subnet wiould be created automatically.
</p>
<br />

<p>
<img src="https://i.imgur.com/BVCgvaq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/0kXjAOg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The above figure shows the steps used in creating VM1 notably, when creating VM1, it is advisable to have all the virtual network on one region. Meaning, if UK South is to be selected in VM1 UK South should also be selected when creating VM2. Also, the second figure shows how virtual network and subnet were created automatically when a virtual machine was created as well as public IP addresses. The subnet address(private IP) shown on image2 would be used in commmunicating between both VM1 nad VM2. While the public IP address is for communication between VM1 and general public.
</p>
<br />

<p>
<img src="https://i.imgur.com/RGvp0Dl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Several resources were created after complete deployment of VM1 as shown above. Resources such as virtual network, public IP, Network Security Group(FIREWALL), and NIC i.e Network Interface Card which is used as an adaptor that is stationed in the cloud were all created on VM1 automatically.
</p>
<br />

<p>
<img src="https://i.imgur.com/DcAXddx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
VM2 above follows same pattern as VM1 except that VM2 uses linus computer Ubuntu to be precise, the virtual network of both VM1 and VM2 were same as well as subnet.
</p>
<br />

<p>
<img src="https://i.imgur.com/RSBCuO6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Both VM1 and VM2 has been successfully created and deployed. A network watcher resource was then used to display network topology for both virtual machines as shown above. However, in some cases an error may occur displaying no network watcher found. In such case, the network watcher resource must then be moved into the virtual machine resource group that was created.
</p>
<br />

<p>
<img src="https://i.imgur.com/8vrEquX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/6ySZBv3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The above figure shows what has been created. This includes two VMs with network security and public IP on both VM which was then attached to two seperate cloud adaptor (NIC). Both adaptors where jointly attached to a subnet and the subnet was then attached to a virtual network.
</p>
<br />

<p>
<img src="https://i.imgur.com/Vz6qAQh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/gGn2QYK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The final stage of this lab is observing traffic between both VMs using a protocol analyser such as 'wireshark'. Also, several commands line tools such as ping and ipconfig were used to send traffic between VM1 and VM2. First, wireshark was downloaded on VM1 then the ethernet adapter was clicked along with the blue start icon at the far left end tab. This then start capturing packets and receiving live traffic on VM1 as shown above. In other to filter the above traffic on VM1 network from spanning an internet protocol called ICMP (Internet Control Messaging Protocol) was then used.
</p>
<br />

<p>
<img src="https://i.imgur.com/sz2Xsfs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the above figure, ICMP was used to help filttered the traffic. As soon as ICMP was used, the spanning stopped as shown above. Notably, ICMP is a protocol used in pinging users. PING is a command line control that is used to test connectivity of any host on a network using its private IP address meaning, to test the connectivity of VM2 on VM1 virtual network such as PING (vm2 + private ip address)
</p>
<br />

<p>
<img src="https://i.imgur.com/rPvtCVv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Using powershell on VM1 as shown above
</p>
<br />
