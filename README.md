<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Connect to Remote Desktop 
- Utilize Powershell and Wireshark
- Implement SSH,RDH,DNS,ICMP with Powershell 
- Analyze various traffic with Wireshark

<h2>Actions and Observations</h2>

<p>
</p>
<p>

  ![Screenshot 2024-02-28 180634](https://github.com/TiffanyChristman/azure-network-protocols/assets/161388738/0ff3d740-1080-4319-9504-7e1c34743411)

</p>
<br />
Create a Windows 10 Virtual Machine (VM) and a Linux (Ubuntu) VM Windows 10 Virtual Machine (VM), while creating the VM, select the previously created Resource Group, allow it to create a new Virtual Network (Vnet) and Subnet


<p> 

</p>
<p>

 ![Screenshot 2024-02-28 185422](https://github.com/TiffanyChristman/azure-network-protocols/assets/161388738/71d7a9d1-911e-440c-94d1-0f8cebc6c8c6)


<b>Use Remote Desktop to connect to your Windows 10 Virtual Machine, use the machine to connect to Ubunto VM. The Windows 10 Virtual Machine is the "host".</b>

</p>

![wireshark](https://github.com/TiffanyChristman/azure-network-protocols/assets/161388738/5c2aaf90-e1eb-4125-b491-15b6b97fb40e)


<p>
Open Wireshark and filter for ICMP traffic only
Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM

</p>

<br />

<p>
  
![Screenshot 2024-02-29 163758](https://github.com/TiffanyChristman/azure-network-protocols/assets/161388738/ba024ba0-ffb2-4b23-a7c5-6a98ad497ee5)


</p>
<p>
Observe ping requests and replies within WireShark
From The Windows 10 VM, open command line or PowerShell and attempt to ping the Ubuntu private IP address and observe the traffic in WireShark

</p>
<br />

<p>
  
![Screenshot 2024-02-29 164001](https://github.com/TiffanyChristman/azure-network-protocols/assets/161388738/756f04ad-0db4-446f-93aa-6ed1a3bd63b1)



</p>
<p>
Filter for SSH traffic only,from your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address)
Type commands (username, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark

</p>
<br />

<p>
  
  ![Screenshot 2024-02-29 164237](https://github.com/TiffanyChristman/azure-network-protocols/assets/161388738/ea026dd6-47b7-482b-847d-1fed18409e88)

</p>
<p>  

Filter for DNS traffic only, from your Windows 10 VM within a command line, use nslookup to see what google.com and disney.com’s IP addresses are


</p>
<br />
