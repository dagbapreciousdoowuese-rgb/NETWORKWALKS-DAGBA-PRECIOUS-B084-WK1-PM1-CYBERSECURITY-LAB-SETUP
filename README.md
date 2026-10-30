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


**Step 1: Installing Oracle VirtualBox**

The first stage of the project was preparing the virtualisation software needed to run the cybersecurity laboratory.
I downloaded and installed Oracle VirtualBox 7.2.20 on my Windows laptop. VirtualBox provides a platform for creating and running virtual machines, which allows me to operate another operating system without replacing my existing Windows installation.
After installation, I opened VirtualBox to confirm that the application was working and ready for the Kali Linux setup.


<img width="3072" height="4096" alt="image" src="https://github.com/user-attachments/assets/8138f76d-a770-4b8e-a8bd-ddb874634811" />

A view of the VirtualBox Environment.


**Step 2: Downloading and Setting Up Kali Linux**

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
