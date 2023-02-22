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
- Various Command-Line Tools
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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
It is important to take care of the patient, to be followed by the doctor, but it is a time of great pain and suffering. For to come to the smallest detail, no one should practice any kind of work unless he derives some benefit from it. Do not be angry with the pain in the reprimand in the pleasure he wants to be a hair from the pain in the hope that there is no breeding.
</p>
<br />
