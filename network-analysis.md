<p align="center">
<img src="https://i.imgur.com/o7mCGi4.png" alt="Wireshark Logo"/>
</p>

# 🦈 Network Analysis using Wireshark
After setting up 2 VMs, I begin filtering traffic using WireShark to then look at and analyse.

<h2>Video Demonstration</h2>

- ### [YouTube: How To Analyse Network Traffic Using Wireshark](https://youtu.be/FVvaHPj0ikc)

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

<p>
<img src="https://i.imgur.com/MFk1JTO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
2. Open the browser and go to https://www.wireshark.org/#download. Download the Windows 10 version for 64bit.

<p>
<img src="https://i.imgur.com/ruvhhXd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

3. Once downloaded, install Wireshark.

<p>
<img src="https://i.imgur.com/yM85P2p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

4. Open Wireshark and click the blue fin to start capturing network traffic.

<p>
<img src="https://i.imgur.com/BfgRSak.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

5. At the top of the screen you will see a search bar. Type **icmp** to filter to ICMP traffic only. Then hit **ENTER**.

<p>
<img src="https://i.imgur.com/wHlZ8B8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

6. Go to **Start** and type **Powershell**. Open up Powershell and then type <code>ping [ip of Ubuntu machine]</code>. Observe the traffic in Wireshark taking note of the source and destination addresses for both request and reply packets.

<p>
<img src="https://i.imgur.com/sIDEuFU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/uzWjS75.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

7. Next, in Wireshark filter to **SSH**.

<p>
<img src="https://i.imgur.com/YGVxve1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


8. In Powershell type in <code>ssh [username]@[ubuntu ip]</code>. Login in to the user you created. Observe the generated traffic in Wireshark. Run a few commands such as <code>whoami, pwd, ls, etc.</code>. Continue to observe the traffic in Wireshark.

<p>
<img src="https://i.imgur.com/sf3pD1e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

9. Next in Wireshark click on the green fin. This will reset the traffic capture. Select **Continue without saving**.

<p>
<img src="https://i.imgur.com/43ktDTF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

10. Filter out DHCP. IN Powershell type <code>ipconfig /renew</code>. Observe the traffic in Wireshark.

<p>
<img src="https://i.imgur.com/NyL86dX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

11. Reset the traffic capture. Filter out DNS. In Powershell type <code>nslookup google.com</code>. This will cause the VM to conduct a Name Server lookup to determine the ip address of google.com. Observe the network traffic in Wireshark.

<p>
<img src="https://i.imgur.com/8ssWFWj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

12. Finally, reset the traffic capture once again. This time type in the filter <code>tcp.port == 3389</code>. This will filter for Remote Desktop Protocol (RDP). This is the protocol in use while  you are connected using Remote Desktop Connection.

<p>
<img src="https://i.imgur.com/AqwdERr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
