<p align="center">
<img src="https://i.imgur.com/jKfy3JS.png" alt="Azure Logo"/>
</p>

# 🏗️ Setting Up Virtual Machines
<p>To analyse traffic I setup two virtual machines in Azure. The first was a Windows 10 machine and the second an Ubuntu Server machine. I set these up on the same virtual network so that they could communicate to each other. I then tested this communication using the <code>ping</code> command to send a ICMP packet from the Windows 10 machine to the Ubuntu Server.</p>

## Video Demonstration

- ### [YouTube: How To Setup Virtual Machines in Azure](https://www.youtube.com)

## Environments and Technologies Used

- Microsoft Azure (Virtual Machines/Compute)
- Microsoft Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
- Ubuntu Server 20

<h2>List of Prerequisites</h2>

- Microsoft Azure Subscription
- Reliable Internet Connection

<h2>Setup Steps</h2>


<p>
Navigate to portal.azure.com. Either make an account or login. At the home page use the search bar to find "Resource groups". This will be the container to hold the virtual machines that will be used in this project.
</p>
<p>
<img src="https://i.imgur.com/A0upyMN.png" height="80%" width="80%" alt=""/>
</p>
<br />


<p>
Once in "Resource groups", select "+Create".
</p>
<p>
<img src="https://i.imgur.com/snGmYke.png" height="80%" width="80%" alt=""/>
</p>
<br />


<p>
Then assign a name in the "Resource group" dialogue box and select the appropriate region for your resources to be hosted. Then click "Review + create".
</p>
<p>
<img src="https://i.imgur.com/s491ej9.png" height="80%" width="80%" alt=""/>
</p>
<br />


<p>
Make sure you've named it appropriately so you know what the resource group is for and then click "Create"
</p>
<p>
<img src="https://i.imgur.com/VhAlbA2.png" height="80%" width="80%" alt=""/>
</p>
<br />


<p>
Your screen should look like this. Now to create the Virtual Machines.
</p>
<p>
<img src="https://i.imgur.com/RPgDApj.png" height="80%" width="80%" alt=""/>
</p>
<br />

<p>
Next, search for "Virtual Machines" in the search bar and select it.
</p>
<p>
<img src="https://i.imgur.com/CvwnEMd.png" height="80%" width="80%" alt=""/>
</p>
<br />

<p>
Click "Create", then "Azure virtual machine".
</p>
<p>
<img src="https://i.imgur.com/lYaZCc3.png" height="80%" width="80%" alt=""/>
</p>
<br />

<p>
Then select the resource group you created. Give your VM a name and make sure the VM is in the same region as the resource group. Then, under "Image", select "Windows 10 Pro, version 21H2 - x64 Gen2". This will be the VM that most of our work will be done from.
</p>
<p>
<img src="https://i.imgur.com/GIztw1f.png" height="80%" width="80%" alt=""/>
</p>
<br />

<p>
Next, select the drop down menu next to "Size" to change to a more capable machine. Assigning 2-4 vcpus and 16GB memory to the VM.
</p>
<p>
<img src="https://i.imgur.com/SpCLWMX.png" height="80%" width="80%" alt=""/>
</p>
<br />

<p>
Scroll down the page and create an administrator account. Make sure to record your username and password. Usually it's not good practice to write down a password but in this case we will be deleting this machine as soon as we're done. You'll also want to make sure the you tick the "Licensing" box, otherwise you wont be able to create the VM.
</p>
<p>
<img src="https://i.imgur.com/BvZjhxo.png" height="80%" width="80%" alt=""/>
</p>
<br />

<p>
Next, at the top of the screen, click on "Networking". Here we will make sure that network settings are configured correctly. We want Azure to create a Virtual Network. Take note of the name as we will use it when we make the next VM. Also, allow it to assign a subnet. Here it is set to 10.0.0.0/24. 
</p>
<p>
<img src="https://i.imgur.com/yJPVWHZ.png" height="80%" width="80%" alt=""/>
</p>
<br />

<p>
Finally, go to the top again and select "Review + create" and then "Create" at the bottom of the page.
</p>
<p>
<img src="https://i.imgur.com/u8AtTiZ.png" height="80%" width="80%" alt=""/>
</p>
<br />

<p>
Azure will then begin deploying the VM. It will take a couple of minutes as it assigns the appropriate resources.
</p>
<p>
<img src="https://i.imgur.com/u8AtTiZ.png" height="80%" width="80%" alt=""/>
</p>
<br />

<p>
Now repeat the process for your second VM. Make sure to select "Ubuntu Server 20.04" as the Image. Then scroll down and select "Password" under Authentication Type. This will allow you to access the VM using SSH without needing to go through the process of using a public and private key.
</p>
<p>
<img src="https://i.imgur.com/ScoGNHd.png" height="80%" width="80%" alt=""/>
<p>
<img src="https://i.imgur.com/ui06W6c.png" height="80%" width="80%" alt=""/>
</p>
</p>
<br />

<p>
Ensure that the Network settings are the same. Then, "Review + create" and create the VM.
</p>
<br />

<p>
Navigate back to the Virtual Machines page and you will be able to see both VMs there.
</p>
<p>
<img src="https://i.imgur.com/REjdJNb.png" height="80%" width="80%" alt=""/>
</p>
<br />

You have successfully setup and deployed 2 virtual machines in Azure. In the section on network analysis we will be going through how to connect to our Windows machine to work from.
