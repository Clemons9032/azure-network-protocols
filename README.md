<p align="center">
<img src=images/Remote-Desktop-Protocol-RDP-vs-Secure-Shell-SSH-Protocol.jpg




<p align="center">
 <img src=images/DHCP.webp alt="Description">
</p>


<h1>networkprotocols - Prerequisites and Installation</h1>
This is a quick tutorial demonstrating the uses of wireshark and how to analyze network traffic using different protocols within an VM

<h2>Video Demonstration</h2>

- ### [Youtube: Analyzing network traffic] (https://www.youtube.com)

<h2>Environments and Technologies used

[![My Skills](https://skillicons.dev/icons?i=azure)](https://skillicons.dev)

- Microsoft Azure
- Remote Desktop Protocol
- DHCP
- SSH
- Wireshark
  
<h2>Operating Systems Used </h2>

[![My Skills](https://skillicons.dev/icons?i=windows,ubuntu)](https://skillicons.dev)

<h2>List of Prerequisites</h2>

Virtual Machines
-wireshark.exe
-Azure Account
  
<h2>High-Level Deployment and Installation</h2>

> [!Important]
> Each step will include written instructions and corresponding screenshots
Expand the See screenshots section to view the images

<h3>Step 1. Create Windows 10 VM</h3>
Log into the azure portal and click on virtual machines and select create new. I'm going to name the VM Windows10.

<details><summary>See screenshots</summary>
<img src="/images/create-newvm.png" >
</details>

<h3>Step 2. Configure windows 10 vm for deployment</h3>
The resource group that i created is called RG-NetworkActivities. Both VM's will need to be in this resource group for the lab. 

<details><summary>See screenshots</summary>
<img src="/images/step2a.png" >
</details>

Name the vm windowsvm and put it in East US 2 and I'm going to choose the windows 10 enterprise image 

<details><summary>See screenshots</summary>
<img src="/images/step2a.png" >
</details>

