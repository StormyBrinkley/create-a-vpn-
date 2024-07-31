

<p align="center">
<img src="https://i.imgur.com/VoDHJKz.png" alt="Azure and ProtonVPN"/>
</p>

<h1>Creating A VPN Using Azure and ProtonVPN: Windows</h1>
In this tutorial, I'll link a virtual machine (VM) to the Internet via a VPN, enabling someone to connect to resources outside of their geographic area or send encapsulated and encrypted data. <br />


<h2>Video Demonstration</h2>

- ### [Creating A VPN Using Azure and ProtonVPN: Windows - Video ](https://youtu.be/A-DTNcSS3-M?si=T90ga6GNGlIcQh9s)
In this comprehensive video tutorial, I will guide you through creating a VPN using Microsoft Azure and ProtonVPN. I will set up one virtual machine with a Windows operating system, connect it to a network in Tokyo, Japan, and then connect it to a VPN in Dallas, Texas. 
<br/>
<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- ProtonVPN


<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 22.04

<h2>High-Level Steps</h2>

- Creating Our Resources
- Create a Virtual Machine in Azure 
- Create A VPN in ProtonVPN


Lastly, I connected to VM2 from VM1  secure shell (SSH) command >ssh labuser @10.0.0.0. Note: During this lab I used VM2's public IP address instead of the private one, being that VM1 and VM2 both shared the same private IP address on the Network which caused no response for some commands.  
</p>
<br />
