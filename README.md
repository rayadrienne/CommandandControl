- set up VMware Workstation Pro for Personal Use. I installed version 17.6
- ![image](https://github.com/user-attachments/assets/133ecdf0-391c-4996-934e-4c876eb6ab1b)

- Workstation Pro 17 is now free for everyone, make sure you tic personal use. 
![image](https://github.com/user-attachments/assets/055b052e-f4fe-4509-b301-bd1572ff20f6)

- Download the VMware version of Windows 11 from Windows Developer here: https://developer.microsoft.com/en-us/windows/downloads/virtual-machines/
- Be mindful of the expiration date of this virtual machine. For example, mine will only last until October 23rd, 2024. If I need another one after that, I can always download it again. 

![image](https://github.com/user-attachments/assets/24c9ab19-05e3-42a6-afbb-2ca2e8ece62d)

- It will take a few minutes to download. Once complete, unzip the downloaded package and double click on the .ovf file. Choose to open the file with VMWare. Provide a name and storage path for the VM. (I put the exp. date in the title of this VM and kept the default storage location)
- 
![image](https://github.com/user-attachments/assets/bb92cf64-f1ec-4662-8c39-100d622272c1)

<b> Install the Ubuntu Server </b>
- Get Ubuntu Server ISO here-  https://releases.ubuntu.com/22.04.1/ubuntu-22.04.1-live-server-amd64.iso
- The server version comes preinstalled with required packages. If you get the desktop version it won't work right.
- 
- ![image](https://github.com/user-attachments/assets/7a02a7cf-96aa-4197-8f44-a315c4f0d04d)

- Click "Create a New Virtual Machine" on the Home tab of VMWare
- Choose the ubuntu iso that you just downloaded as the installer disc image file
- ![image](https://github.com/user-attachments/assets/340ceda6-7059-427b-a315-67f6f4cc9cc3)

- I reduced my disk size to 14gb, the recommended is 20gb.

  ![image](https://github.com/user-attachments/assets/725e3e50-6a76-4d51-a0c6-9fe76bf44888)

  - On the next page, click "customize hardware"

  ![image](https://github.com/user-attachments/assets/3f25bf3c-0005-4565-88e2-582d831b60ce)

  - I reduced the memory to 2gb from 4gb and kept the processors at 2. Keep all the other defaults the same and continue. 
 
    ![image](https://github.com/user-attachments/assets/5329fc5a-fd06-4d26-9b49-5bb752e28e8e)

- When you get to this screen, stop! We need to find the gateway IP address of the NAT network.
  - In the VMware workstation, click "edit" at the top
  - Click “Virtual Network Editor”
  - Select the “Type: NAT” network
  - Click “NAT Settings…”

 ![image](https://github.com/user-attachments/assets/48420ff5-08a1-4434-a863-7fdd4dbf82d5)

- Write down your Subnet IP and Gateway IP addresses, we will need them next. 
![image](https://github.com/user-attachments/assets/0aa2757c-37d2-4dfc-aba4-c52848bc8e38)

- You can close out of these screens and go back to the Ubuntu server screen.
- Press Tab to cycle and Enter to select.
  
![image](https://github.com/user-attachments/assets/89f5a885-0f08-478f-aed0-86e9109ec5f3)

- Select Manual.
  
![image](https://github.com/user-attachments/assets/2996a6e7-0fb9-4f65-abc6-04ccfe5db4d3)

- Input the subnet and gateway IPs that you wrote down. add /24 to the end of the subnet IP to designate the size of the subnet.

  ![image](https://github.com/user-attachments/assets/6988179f-2749-431f-8bdf-721827823ca9)

- In the Address field, insert the DHCPv4 address above in grey font, minus the cidr notation at the end. 

![image](https://github.com/user-attachments/assets/77fd3ad4-1ddb-4ad0-ad9f-bfbb6c2b533c)

- Write down this static IP address- you're going to need it a few more times.

  ![image](https://github.com/user-attachments/assets/498c699f-b67c-4802-bd46-fb780bdbd114)

- Press done a few more times until you get to this screen. I was super original and chose my name to be User, My server name to be Attack, Username to be user and password to be password. You can choose whatever you would like, security isn't a huge concern, we will nuke these machines when we are done. 

































