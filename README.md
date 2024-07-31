

<p align="center">
<img src="https://i.imgur.com/VoDHJKz.png" alt="Azure and ProtonVPN"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [Creating A VPN Using Azure and ProtonVPN: Windows - Video ](https://youtu.be/A-DTNcSS3-M?si=T90ga6GNGlIcQh9s)
In this comprehensive video tutorial (featuring instrumental music and no audio commentary), I will guide you through the entire process of creating two virtual machines in Microsoft Azure. We will set up one virtual machine with a Windows operating system and another with a Linux operating system. This tutorial will cover all the necessary steps and configurations to ensure both virtual machines are up and running smoothly.
<br/>
<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04
<h2>High-Level Steps</h2>

- Creating Our Resources
- Conducting Network Activities: Filtering Traffic with Various Protocols in Wireshark Using PowerShell
- Observe ICMP, SSH, DHCP, DNS, RDP Traffic

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/eeFtFsy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, you'll need to obtain the public IP address for VM1. 
</p>
<br />

<p>
<img src="https://i.imgur.com/pxHBwVx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Microsoft Remote Desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/NnNED4P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to PC name and add VM1's IP address then log-in with the credentials you created for VM1. 
</p>
<br />

<p>
<img src="https://i.imgur.com/Xz9lhwr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<p>
<img src="https://i.imgur.com/iU6K7Ou.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/9pTt9Fm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here you see me trying to ping VM2, but since VM1 and VM2 have the same private IP address, some Linux commands didn't work properly. I did a workaround and used the public IP address instead.
</p>
<br />

<p>
<img src="https://i.imgur.com/0SvpyJt.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now I was able to create a firewall rule that denied ICMP traffic.
</p>
<br />

<p>
<img src="https://i.imgur.com/9pTt9Fm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Next, I filtered the traffic by ICMP and viewed the results in Wireshark.
<br />

<p>
<img src="https://i.imgur.com/CWj1q6C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Then I filtered by DNS and viewed the results in Wireshark.
</p>
<br />

<p>
<img src="https://i.imgur.com/epWorgI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Here is filtered by SSH viewing results in Wireshark.
</p>
<br />

<p>
<img src="https://i.imgur.com/epWorgI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lastly, I connected to VM2 from VM1  secure shell (SSH) command >ssh labuser @10.0.0.0. Note: During this lab I used VM2's public IP address instead of the private one, being that VM1 and VM2 both shared the same private IP address on the Network which caused no response for some commands.  
</p>
<br />
