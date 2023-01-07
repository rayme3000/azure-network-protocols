![VMs NSG](https://user-images.githubusercontent.com/59034949/210693949-4308af3f-306f-467f-9444-6cb044de2357.jpg)


<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


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

- Create our Resources
- Observe ICMP Traffic
- Observe SSH Traffic
- Observe DHCP Traffic
- Observe DNS Traffic
- Observe RDP Traffic

<h2>Actions and Observations</h2>

![nsg vms](https://user-images.githubusercontent.com/59034949/211152518-58571969-a6fd-4514-81bc-e5e855694202.png)
![nsg net](https://user-images.githubusercontent.com/59034949/211152875-c9b96267-382d-410a-b18e-519c7b8ced3d.png)


<p>
1. Create a Resource Group
<br>
2. Create a Windows 10 Virtual Machine (VM).
<br>
3. Create a Linux (Ubuntu) VM.
<br>
**Note: If a troubleshooting error appears, make sure the "NetworkWactherRG" is inside of the same resource group as the VMs.<br>
4. Observe Your Virtual Network within Network Watcher.

![nsg rdp](https://user-images.githubusercontent.com/59034949/211152903-ffd8de06-c587-4581-bff4-3c016f224fea.png)

  
<p>
5. Use Remote Desktop to connect to your Windows 10 Virtual Machine.
<br>
6. Within your Windows 10 Virtual Machine, Install Wireshark.
<br>
7. Open Wireshark and filter for ICMP traffic only.
<br>
8. Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM.
<br>
9. From The Windows 10 VM, open command line or PowerShell and attempt to ping a public website (such as www.google.com) and observe the traffic in WireShark.
<br>
10. Initiate a perpetual/non-stop ping from your Windows 10 VM to your Ubuntu VM.

![nsg wire](https://user-images.githubusercontent.com/59034949/211153027-2e80b34e-d0e4-4512-bb77-784ab045b600.png)
![nsg ping](https://user-images.githubusercontent.com/59034949/211153053-dcf76720-aa39-4a37-92b6-51289b589d58.png)

  
11. In Wireshark, filter for SSH traffic only. From your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address). Type commands (ls, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark. Exit the SSH connection by typing ‘exit’ and pressing [Enter].
<br>
12. Back in Wireshark, filter for DHCP, DNS, and RDP traffic only (indivually). Observe each protocol’s traffic appearing in WireShark.

</p>
<br />
