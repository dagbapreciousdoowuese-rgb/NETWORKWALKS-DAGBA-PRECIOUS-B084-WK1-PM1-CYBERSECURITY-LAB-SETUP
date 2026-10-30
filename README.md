**Week 1: Building My Cybersecurity Practical Lab Environment**

**Networkwalks Cybersecurity Programme | Practical Project 1**

**Project Overview**

This project is focused on setting up my first practical cybersecurity laboratory using Oracle VirtualBox and Kali Linux. Its main aim was to create a virtual environment where I can better learn cybersecurity concepts, practise technical skills and carry out security-related exercises in a controlled setting.

Using my Windows laptop as the host computer, I installed and prepared a Kali Linux virtual machine and worked on its network configuration, connectivity and integration with the host system.

This laboratory will serve as my starting point for hands-on cybersecurity practice and future technical exercises.



**Project Objectives**

The main goal of this exercise was to build a functional virtual laboratory that I can use for practical cybersecurity learning.

The specific tasks included:

- Installing and configuring Kali Linux in Oracle VirtualBox.
- Creating a dedicated NAT Network for the laboratory.
- Connecting the Kali Linux virtual machine to the configured network.
- Setting up a static IPv4 address.
- Providing internet access within the virtual machine.
- Enabling bidirectional clipboard sharing and drag-and-drop.
- Connecting the Windows Downloads folder to Kali Linux through a shared folder.
- Creating a snapshot to preserve the virtual machine's initial configuration.
- Testing the network connection and documenting the results.


**Installing Oracle VirtualBox**

The first stage of the project was preparing the virtualisation software needed to run the cybersecurity laboratory.
I downloaded and installed Oracle VirtualBox 7.2.20 on my Windows laptop. VirtualBox provides a platform for creating and running virtual machines, which allows me to operate another operating system without replacing my existing Windows installation.
After installation, I opened VirtualBox to confirm that the application was working and ready for the Kali Linux setup.


<img width="3072" height="4096" alt="image" src="https://github.com/user-attachments/assets/8138f76d-a770-4b8e-a8bd-ddb874634811" />

A view of the VirtualBox Environment.



**Downloading and Setting Up Kali Linux**

After installing Oracle VirtualBox, the next task was to obtain Kali Linux and prepare it to run as a virtual machine.
I downloaded the pre-built Kali Linux virtual machine image from the official Kali Linux website. This version was already packaged for virtualisation, making it possible to import it directly into VirtualBox without going through a separate operating system installation process.

**Downloading Kali Linux**

I visited the official Kali Linux website and downloaded the pre-built VirtualBox image.
After the download was completed, I used 7-Zip to extract the compressed file. This gave me access to the virtual machine configuration files required by VirtualBox.

<img width="3072" height="4096" alt="image" src="https://github.com/user-attachments/assets/409e5529-5b77-4d1d-a43d-59e5fa677551" />


I opened the extracted folder and located the .vbox configuration file.
I opened this file with VirtualBox, which registered the Kali Linux virtual machine in the application.
After registering Kali Linux, I selected the virtual machine in VirtualBox and started it.
Once it booted successfully, I could access the Kali Linux desktop and its built-in tools.

<img width="3072" height="1743" alt="image" src="https://github.com/user-attachments/assets/148845a3-bd34-456f-a509-89f51d0c4b0f" />



<img width="3955" height="2417" alt="Kali Linux after start up" src="https://github.com/user-attachments/assets/d4f17c33-1ba9-4cd2-aeb4-9cb4355deecf" />




**Creating a NAT Network in VirtualBox**

After setting up Kali Linux, the next stage was creating a dedicated virtual network for the cybersecurity laboratory.
I used VirtualBox's Network Manager to create a NAT Network named Cybersecurity-Lab. This network provides a common networking environment for virtual machines and allows them to access external networks through Network Address Translation (NAT).
I opened the VirtualBox Network Manager and created a new NAT Network.
I assigned it the name Cybersecurity-Lab to make it easy to identify within the virtualisation environment.
I configured the network to use the required IPv4 address range and subnet prefix:
10.0.0.0/24. This defines the private network address range that will be used for communication within the laboratory.
I enabled the NAT Network and left IPv6 disabled, as required for the project.
The network was then saved for use by the Kali Linux virtual machine.



<img width="3072" height="2354" alt="image" src="https://github.com/user-attachments/assets/76889dd5-91f1-4d6a-8970-8464f6d9da5b" />


<img width="3072" height="4096" alt="image" src="https://github.com/user-attachments/assets/c660e16c-2673-4099-bca9-f0281ddb0676" />


The Cybersecurity-Lab NAT Network was successfully created in VirtualBox and made available for the Kali Linux network adapter configuration.





**Connecting Kali Linux to the NAT Network**

With the NAT Network created, the next task was to connect the Kali Linux virtual machine to it. This connection allows Kali Linux to communicate through the virtual network configured for the laboratory.

I selected the Kali Linux virtual machine in VirtualBox and opened its Settings.
Under the Network section, I accessed the configuration options for Adapter 1.
I enabled the network adapter and changed its attachment type to NAT Network.
I then selected the previously created Cybersecurity-Lab network from the available network options.
The adapter settings were configured as shown in the screenshot.

After selecting the appropriate network, I saved the changes. This connected the Kali Linux virtual machine to the dedicated NAT Network created earlier.







<img width="4096" height="3072" alt="Network Adapter" src="https://github.com/user-attachments/assets/f97aa379-25f8-4651-aa6c-d506a2851fbb" />










**Configuring the Network and VirtualBox Integration**

After connecting Kali Linux to the Cybersecurity-Lab NAT Network, I proceeded to configure its network settings, establish internet connectivity and enable communication between the virtual machine and my Windows host.

I opened the Kali Linux terminal and used the following command to examine the available network interfaces:

ip a

The project required Kali Linux to use a static IPv4 address rather than depend on automatic address assignment.

The required network parameters were:

Parameter| Configuration
IPv4 Address| 10.0.0.2
Subnet Prefix| /24
Default Gateway| Virtual network gateway
DNS Server| Configured DNS server

I used Kali Linux's network configuration tools to apply the required settings.

After configuring the network address, I proceeded to check whether Kali Linux could communicate with external networks.

I used the following commands during the connectivity checks:

Testing external IP connectivity:

ping -c 4 8.8.8.8

Testing DNS resolution:

ping -c 4 google.com

The first command checks whether the machine can reach an external IP address, while the second checks whether it can resolve a domain name and communicate with the destination.

These tests help distinguish between general network connectivity problems and DNS-related issues.

I also configured VirtualBox to support file and text exchange between my Windows host and Kali Linux.

Under the virtual machine's settings, I configured the following options:

Setting| Configuration
Shared Clipboard| Bidirectional
Drag and Drop| Bidirectional





<img width="3072" height="4096" alt="drag and drop" src="https://github.com/user-attachments/assets/dd92b173-57ec-44d7-a4ce-0b67b22ac7c0" />






This stage covered the network addressing requirements, connectivity checks and VirtualBox integration settings needed for the laboratory.

