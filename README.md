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

-Virtual Machines

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
<img src="/images/step4a.png" >
</details>

Choose a username that's easy to remember for the lab or just make sure to open a notepad and save your credentials so you don't forget

<details><summary>See screenshots</summary>
<img src="/images/step7.png" >
</details>

Next we're going to go to the network tab and make a new vnet called lab1vnet

<details><summary>See screenshots</summary>
<img src="/images/step8.png" >
</details>

Now we're through with the configuration and we can continue to review & create

<details><summary>See screenshots</summary>
<img src="/images/step9.png" >
</details>

<h3>Step3.Create a linuxvm for deployment</h3>
Go to the virtual machine tab and click create new vm. We're going to use the same configuration as the windows10 vm with same resource group and virtual network.

<details><summary>See screenshots</summary>
<img src="/images/step10.png" >
</details>

For the authentication, I'm going to choose password instead of ssh key

<details><summary>See screenshots</summary>
<img src="/images/step11.png" >
</details>

Next make sure to choose the same vnet as the windowsvm and afterwards, we can review and create the linuxvm

<details><summary>See screenshots</summary>
<img src="/images/step12.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step13.png" >
</details>

<h3>Step4. Windows deployment</h3>
In order to rdp into the windowsvm i have to get the public ip address. Click on the windowsvm and the public ip address will be on the overview page.

<details><summary>See screenshots</summary>
<img src="/images/step14.png" >
</details>

After getting the public ip address, press win+r and type in mstsc to open the rdp connection tab. Enter your public ip address for the windows vm and the password and you'll be connected to the windows vm

<details><summary>See screenshots</summary>
<img src="/images/step15.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step16.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step17.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step18.png" >
</details>

<h3>Step5. Installing Wireshark</h3>
After connecting with your vm, you'll see some prompts from windows. You can say no to all of those prompts until you reach the GUI. After landing on the desktop, go to microsoft edge and type in wireshark. Once you land on the wireshark home page, choose the download button and depending on which architecture you're running, download the correct version.

<details><summary>See screenshots</summary>
<img src="/images/step19.png" >
</details>



<details><summary>See screenshots</summary>
<img src="/images/step20.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step21.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step22.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step23.png" >
</details>


<details><summary>See screenshots</summary>
<img src="/images/step24.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step25.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step26.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step27.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step28.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step29.png"
</details>

<details><summary>See screenshots</summary>
<img src="/images/step31.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step32.png" >
</details>

<h3>Step6.Open Wireshark</h3>
After installation, go to the start button and type in wireshark to open. After it's open, choose the ethernet button and it'll take you to the network analyzer.

<details><summary>See screenshots</summary>
<img src="/images/step33.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step34.png" >
</details>

<h3>Step7. Analyzing network traffic using various protocols</h3>
After the network analyzer opens up, we can see a bunch of data currently shifting through the network. Even though the only thing I've done is just open wireshark, I can see my network is very active. So the first protocol to use is icmp which is short for ping. Head to the search bar above the network information and type icmp to filter the traffic to just icmp data.

<details><summary>See screenshots</summary>
<img src="/images/step35.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step37.png" >
</details>

After changing protocols, press the start button and open up powershell. From here I'm going to ping google.com and the linux vm that was created. type the following command ping www.google.com to see my vm attempt to establish a connection with google.com.

<details><summary>See screenshots</summary>
<img src="/images/step38.png" >
</details>

we can see the reply from google.com sending back to the client. That's a good sign because that shows a proper network connectivity between our client and google. Next is to ping the linux vm and check if we have a proper connection to the linux client. Go back to azure and get the private ip address and that's what will be used to attempt a connection with linux

<details><summary>See screenshots</summary>
<img src="/images/step39.png" >
</details

<details><summary>See screenshots</summary>
<img src="/images/step40.png" >
</details>

I'm going to start up a continuous ping so I can see what happens when a firewall restriction is put in place while a perpetual ping is established. In order to start a perpetual ping, go back to powershell and type ping -t 10.0.0.5 and that'll initiate the continuous ping.

<details><summary>See screenshots</summary>
<img src="/images/step41.png" >
</details>

I'm going to set some firewall permissions to further see what happens in wireshark when a firewall is in place for a particular client. Go back into azure and click the linux vm. After it's selected, go to the network settings tab and scroll down to the network security group.

<details><summary>See screenshots</summary>
<img src="/images/step42.png" >
</details>

<details><summary>See screenshots</summary>
<img src="/images/step43.png" >
</details>

In order to set up the firewall, I'm going to click on create port rule and select inbound port rule.

<details><summary>See screenshots</summary>
<img src="/images/step45.png" >
</details>

On the add inbound security rule, go to the destination port ranges and type *. This is a stand in for any. Next is to select the protocol ICMPv4. Ping command uses the protocol to establish a connection with different servers and clients. Next, choose deny to block all incoming traffic from making a connection with the linux server. For the priority, I'm going to type in 290. So the reason for the number is the lower the number, the higher the priority and it'll take precedence over the SSH protocol in place.

<details><summary>See screenshots</summary>
<img src="/images/step47.png" >
</details>

After configuring this firewall, we can start to see the changes take effect immediately. Looking in the terminal, we can start to see the ping time out as the linux client can no longer reached. We can start to see a lot of request timed out messages and it'll continue in perpetuity until this rule is either deleted or the priority has been lowered.

Now we're going to delete the firewall rule and once that happens, we can see that communication to the client starts up rather quickly.

<details><summary>See screenshots</summary>
<img src="/images/step48.png" >
</details>

After analyzing firewall rules, I'm going to analyze ssh traffic. Clear the filter and type ssh in the search bar and restart the packet capture. Next go back into azure and get the private ip address to the linux vm. Copy down the ip address and go back into the windows vm and go back to powershell. To ssh into the linux vm
type ssh username@private-ipaddress. In my case, I'm going to enter ssh basheddaemon@10.0.0.6. You'll be prompted to enter your password and after that you'll be connected to the linux vm via a terminal. Enter a few commands to see how the traffic works in regards to ssh commands compared to when a ping is initiated.

<details><summary>See screenshots</summary>
<img src="SSH/ssh_step1.png" >
</details>

<details><summary>See screenshots</summary>
<img src="SSH/ssh_Step2.png" >
</details>











