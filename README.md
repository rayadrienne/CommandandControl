# Setup Guide for VMware Workstation Pro and Windows & Ubuntu Virtual Machines

Welcome to this guide on setting up VMware Workstation Pro for personal purposes, and installing Windows and Ubuntu Server virtual machines (VMs).

## Setting Up VMware Workstation Pro

VMware Workstation Pro is a powerful virtualization software that allows users to run multiple operating systems on a single physical machine. Here's how you can set it up for personal use.

### 1. Install VMware Workstation Pro

First, ensure you download and install version 17.6 of VMware Workstation Pro, as it is now free for personal use.

![VMware Workstation Pro Installation](https://github.com/user-attachments/assets/133ecdf0-391c-4996-934e-4c876eb6ab1b)

### 2. License for Personal Use

When you install VMware Workstation Pro, select "Personal Use" when prompted to ensure you're complying with the license agreement.

![VMware Workstation Pro License Selection](https://github.com/user-attachments/assets/055b052e-f4fe-4509-b301-bd1572ff20f6)

### 3. Download Windows 11 VM

You can obtain a pre-configured Windows 11 virtual machine, optimized for developers, from the official Windows Developer website:

[Download Windows 11 VM](https://developer.microsoft.com/en-us/windows/downloads/virtual-machines/)

> **Note:** This VM has an expiration date, after which you can re-download if needed. For instance, the VM I used will expire on October 23rd, 2024.

![Windows 11 VM Download](https://github.com/user-attachments/assets/24c9ab19-05e3-42a6-afbb-2ca2e8ece62d)

### 4. Import and Configure Windows 11 VM

- Once your download is complete, extract the contents and double-click the `.ovf` file. 
- Choose to open the file with VMware and set a name and storage path for the VM. Consider including the experiment date in the VM's title for easy reference.

![Import and Configure Windows 11 VM](https://github.com/user-attachments/assets/bb92cf64-f1ec-4662-8c39-100d622272c1)

## Installing Ubuntu Server on VMware

### 1. Download Ubuntu Server ISO

Get the image file for Ubuntu Server using the following link:

[Download Ubuntu Server 22.04.1 ISO](https://releases.ubuntu.com/22.04.1/ubuntu-22.04.1-live-server-amd64.iso)

![Ubuntu Server Download](https://github.com/user-attachments/assets/7a02a7cf-96aa-4197-8f44-a315c4f0d04d)

### 2. Create a New VM for Ubuntu Server

- Select "Create a New Virtual Machine" on the VMWare Home tab.
- For the installer disc image file, choose the downloaded Ubuntu ISO.

![Create New Ubuntu VM](https://github.com/user-attachments/assets/340ceda6-7059-427b-a315-67f6f4cc9cc3)

### 3. Adjust Hardware Specifications

Lower the disk size to what's practical for your use case—I chose 14GB, though 20GB is recommended.

![Adjust Hardware Specifications](https://github.com/user-attachments/assets/725e3e50-6a76-4d51-a0c6-9fe76bf44888)


### Customize Hardware

Navigate to the next configuration screen to adjust your hardware settings.

#### Memory and Processors

- On the **Customize Hardware** page, consider reducing the memory allocation. For example, a reduction from 4GB to 2GB is acceptable for most scenarios.
- Maintain the number of processors at 2 for balanced performance.

![Customize Hardware Memory](https://github.com/user-attachments/assets/3f25bf3c-0005-4565-88e2-582d831b60ce)

![Customize Hardware Processors](https://github.com/user-attachments/assets/5329fc5a-fd06-4d26-9b49-5bb752e28e8e)

### Network Configuration

Before continuing, it's essential to identify the network settings for your virtual environment.

#### Retrieve Network Information

- From the VMware Workstation menu, select **Edit > Virtual Network Editor**.
- Choose the NAT network option and click on **NAT Settings** to view the details.

![Network Editor](https://github.com/user-attachments/assets/48420ff5-08a1-4434-a863-7fdd4dbf82d5)

Document the Subnet IP and Gateway IP addresses as these will be required for the Ubuntu server network configuration.

![Subnet and Gateway IPs](https://github.com/user-attachments/assets/0aa2757c-37d2-4dfc-aba4-c52848bc8e38)

#### Manual Network Setup

After collecting the network information, proceed with the network setup by selecting **Manual** configuration during the VM setup process.

![Network Configuration Selection](https://github.com/user-attachments/assets/89f5a885-0f08-478f-aed0-86e9109ec5f3)

Input the Subnet and Gateway IPs you have noted and append `/24` to the Subnet IP to denote the subnet size.

![Manual Network Configuration](https://github.com/user-attachments/assets/2996a6e7-0fb9-4f65-abc6-04ccfe5db4d3)

For the Address field, use the suggested DHCPv4 address, excluding the CIDR notation.

![DHCPv4 Address Input](https://github.com/user-attachments/assets/77fd3ad4-1ddb-4ad0-ad9f-bfbb6c2b533c)

Record the designated static IP address; it will be necessary for subsequent stages in the setup.

![Static IP Address](https://github.com/user-attachments/assets/498c699f-b67c-4802-bd46-fb780bdbd114)

### Finalizing Ubuntu Server Installation

After setting the network configuration, complete the installation by providing a server name, username, and password. Additionally, enable the OpenSSH server to allow remote access.

![Ubuntu Server Installation Summary](https://github.com/user-attachments/assets/7031453c-a3c8-4ea8-9c5c-634d2b0fdc59)

In the event the installation process stalls, pressing enter can assist in resuming the setup.

Once installation completes, you will be prompted to log in with the credentials you have chosen.

![Ubuntu Server Login Prompt](https://github.com/user-attachments/assets/7d030113-ff93-4e44-9777-3e1434a1fbdb)

Verification of the setup is crucial. Confirm functional networking by pinging an external site such as Google.

![Ping Test](https://github.com/user-attachments/assets/c05c305e-6cad-45f6-a6bd-5acd084842ca)

## Setting Up Windows VM in VMware

After successfully installing the Ubuntu Server, return to VMware Workstation and power on the previously imported Windows 11 VM for additional configuration and usage.





























