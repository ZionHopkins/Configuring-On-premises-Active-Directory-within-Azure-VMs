# Configuring-On-premises-Active-Directory-within-Azure-VMs

Setup Resources in Azure

Create the Domain Controller VM (Windows Server 2022) named “DC-1”

Take note of the Resource Group and Virtual Network (Vnet) that get created at this time

Set Domain Controller’s NIC Private IP address to be static
<p>
<img src="https://i.imgur.com/rMZIb2e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/YZeGtv1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/Rg1NY6j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create the Client VM (Windows 10) named “Client-1”. Use the same Resource Group and Vnet that was created in
  
Ensure that both VMs are in the same Vnet (you can check the topology with Network Watcher

Ensure Connectivity between the client and Domain Controller
  
Login to Client-1 with Remote Desktop and ping DC-1’s private IP address with ping -t <ip address> (perpetual ping)
  
Login to the Domain Controller and enable ICMPv4 in on the local windows Firewall

<p>
<img src="https://i.imgur.com/aX8tYw4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Check back at Client-1 to see the ping succeed

Install Active Directory
  
Login to DC-1 and install Active Directory Domain Services
<p>
<img src="https://i.imgur.com/NaVLgh4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/Xkg1ggr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
