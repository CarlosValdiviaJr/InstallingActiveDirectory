# Setting Up Active Directory on Oracle VirtualBox

## Overview
This project provides a step-by-step guide for setting up Active Directory on Oracle VirtualBox. By following these instructions, users can create a local environment to simulate a Windows Server environment for testing or development purposes.

### Prerequisites
- [Oracle VirtualBox](https://www.virtualbox.org/) installed on your system.
- A Windows Server ISO file. (Ensure you have the appropriate license for usage)
- Basic familiarity with Oracle VirtualBox and Windows Server environments.

## Step-by-Step Guide

### Step 1: Download and Install Oracle VirtualBox
1. Navigate to the [Oracle VirtualBox website](https://www.virtualbox.org/) and download the appropriate version for your operating system.
![Virtual Box Download - Imgur](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/51ad1e8e-689b-4ff4-a646-e4f47b926d52)
3. Follow the installation instructions provided by the installer.
4. Launch VirtualBox once the installation is complete.

### Step 2: Download Windows 2019 ISO file
1. Navigate to the [Microsoft's Windows Server 2019 Download Page](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019/) and download the appropriate ISO file for your operating system.
![Screen Shot 2024-03-24 at 1 28 24 PM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/d7b90a86-4007-4a18-a753-96bfd161f384)
2. Follow the installation instructions provided by the installer.

### Step 3: Create a New Virtual Machine
1. Click on the "New" button in the VirtualBox interface to create a new virtual machine.
![Screen Shot 2024-03-24 at 1 31 42 PM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/3836df7c-5175-4914-9575-9cd6a339bf77)
3. Enter a name for your virtual machine (e.g., "Windows Server").
4. For "ISO Image" select the Windows Server 2019 ISO file you previosly downloaded.
5. For "Edition" select the "Standard Evalutaion (Desktop Experience)"
6. Select "Skip Unattended Installation"
![Screen Shot 2024-03-21 at 8 50 27 PM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/c53a68f6-051f-47a8-9772-6ae03669925d)
7. Allocate the desired amount of RAM for the virtual machine.
8. Create a new virtual hard disk and set the size according to your requirements.
9. Complete the virtual machine creation wizard.

### Step 4: Install Windows Server
1. Start the virtual machine by clicking the "Start" button in the VirtualBox interface.
2. Follow the on-screen instructions to install Windows Server within the virtual machine.
![Screen Shot 2024-03-24 at 1 55 10 PM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/965ee81a-4a0b-4969-8968-0f64999431d3)
4. Complete the installation process and log in to the Windows Server environment.

### Step 5: Install and Configure Active Directory
1. Open the "Server Manager" dashboard in Windows Server.
2. Click on "Add roles and features" to start the wizard.
![Screen Shot 2024-03-24 at 11 22 46 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/a189aa17-a7c9-47cf-ab72-19441b5f8c90)
![Screen Shot 2024-03-24 at 11 23 13 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/0a81eac3-b210-4c61-add6-a68b594a0e43)
![Screen Shot 2024-03-24 at 11 23 31 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/186a1cb0-3d2e-4588-b132-760b9110cb58)
3. Select "Active Directory Domain Services" from the list of roles and follow the wizard to install it.
![Screen Shot 2024-03-24 at 11 24 07 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/0c5d1bf3-0662-4381-a5c9-359ccc78f3ad)
![Screen Shot 2024-03-24 at 11 24 16 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/5a82b358-3f41-48ba-88e6-020df90bb4d2)
![Screen Shot 2024-03-24 at 11 24 43 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/1a99a328-85b2-4ff6-a467-9f8142fc20f9)
![Screen Shot 2024-03-24 at 11 24 52 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/75ff41d8-d99a-43fc-82e2-82ef5359dcaf)
4. Once installation is complete. Select "Promote this server to domain controller"
![Screen Shot 2024-03-24 at 11 26 54 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/dd86a9f0-cc45-45c7-82cd-e2cd65fca060)
  Select "Add a new forest" and enter a Domain name (e.g., "mydomain.com").
![Screen Shot 2024-03-24 at 11 28 41 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/b6cf7b23-d1e0-4347-82fd-7d4e7e42ea94)
   Unselect "Domain Name System (DNS) Server"
   Type in Admin Password
![Screen Shot 2024-03-24 at 11 29 21 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/842a7c2e-9b2b-46e9-add1-499e10c26b60)
![Screen Shot 2024-03-24 at 11 29 58 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/8f72faad-247b-42cc-8fbd-798e54a83b8e)
![Screen Shot 2024-03-24 at 11 30 11 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/42054510-fe2d-4620-97e7-7305b7c423a7)
![Screen Shot 2024-03-24 at 11 30 20 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/e15eda75-bc3b-4b52-bd34-04ad62dbc03c)
![Screen Shot 2024-03-24 at 11 30 44 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/7b1a359b-5be0-4d98-a3fd-67d26fed4421)
Once the Active Directory setup wizard has completed the system will restart.
 
### Step 6: Testing
1. Log in with the new Domain Controller
![Screen Shot 2024-03-24 at 11 41 30 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/a69ce886-c5e7-409f-8045-5aafa1425c83)  
3. Ensure that the Active Directory installation is successful by selecting Tools in the Server Manager Dashboard and confirming the new Active Directory tools 
![Screen Shot 2024-03-24 at 11 43 23 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/816e2e10-3d4a-4a3e-9897-1d40a5a3f8d7)
4. By clicking "Active Directory Users and Computers" you can verify the Installation was succesfull if you see the Domain you created.
![Screen Shot 2024-03-24 at 11 43 59 AM](https://github.com/CarlosValdiviaJr/InstallingActiveDirectory/assets/164792743/040c3ce6-4fd7-434d-a897-5cb241b143c1)

## Conclusion
By following this guide, you should have successfully set up Active Directory on Oracle VirtualBox, allowing you to simulate a Windows Server environment locally for various testing and development purposes.
