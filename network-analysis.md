<p align="center">
<img src="https://i.imgur.com/o7mCGi4.png" alt="Wireshark Logo"/>
</p>

# 🦈 Network Analysis using Wireshark
After setting up 2 VMs, I begin filtering traffic using WireShark to then look at and analyse.

<h2>Video Demonstration</h2>

- ### [YouTube: How To Analyse Network Traffic Using Wireshark](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Microsoft Remote Desktop
- Wireshark

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
- Ubuntu Server 20

<h2>List of Prerequisites</h2>

- Microsoft Azure Subscription
- Reliable Internet Connection
- Wireshark

<h2>Installation Steps</h2>

1. Connect to your VM using Remote Desktop.
2. Open the browser and go to https://www.wireshark.org/#download. Download the Windows 10 version for 64bit.
3. Once downloaded, install Wireshark.
4. Open Wireshark and click the blue fin to start capturing network traffic.
5. At the top of the screen you will see a search bar. Type **icmp** to filter to ICMP traffic only. Then hit **ENTER**.
6. Go to **Start** and type **Powershell**. Open up Powershell and then type <code>ping [ip of Ubuntu machine]</code>. Observe the traffic in Wireshark taking note of the source and destination addresses for both request and reply packets.
7. Next, in Wireshark filter to **SSH**.
8. In Powershell type in <code>ssh [username]@[ubuntu ip]</code>. Login in to the user you created. Observe the generated traffic in Wireshark. Run a few commands such as <code>whoami, pwd, ls, etc.</code>. Continue to observe the traffic in Wireshark.
9. Next in Wireshark click on the green fin. This will reset the traffic capture. Select **Continue without saving**.
10. Filter out DHCP. IN Powershell type <code>ipconfig /renew</code>. Observe the traffic in Wireshark.
11. Reset the traffic capture. Filter out DNS. In Powershell type <code>nslookup google.com</code>. This will cause the VM to conduct a Name Server lookup to determine the ip address of google.com. Observe the network traffic in Wireshark.
12. Finally, reset the traffic capture once again. This time type in the filter <code>tcp.port == 3389</code>. This will filter for Remote Desktop Protocol (RDP). This is the protocol in use while  you are connected using Remote Desktop Connection.



<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
