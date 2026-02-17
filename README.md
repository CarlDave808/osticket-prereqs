<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the system requirements and walks you through the installation process for the open-source help desk ticketing platform, osTicket.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine

- osTicket Installation files

- Heidi SQL

<h2>Installation Steps</h2>

<img width="1002" height="469" alt="Screenshot 2026-02-16 183103" src="https://github.com/user-attachments/assets/aee1f675-f37e-4187-80f5-c5e937170966" />

Create a resource group in Microsoft Azure called osTicket, then deploy a virtual machine inside that resource group. Select a Windows 10 Pro image for the VM and configure it with a minimum of 2 vCPUs. This virtual machine will be used as a practice environment.

<img width="537" height="297" alt="Screenshot 2026-02-16 183309" src="https://github.com/user-attachments/assets/5b71d4bf-62d0-43e9-a676-6525a98f3c93" />

Connect to the virtual machine using Remote Desktop Protocol(RDP). In the Microsoft Azure portal, copy the VM's Public IPv4 address and use it to initiate the RDP connection.

<img width="1035" height="184" alt="Screenshot 2026-02-16 183732" src="https://github.com/user-attachments/assets/bf2c16f2-a19f-4d46-84b7-8f07618e0a43" />

Within the VM (osticket-vm), download the https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”

<img width="383" height="336" alt="Screenshot 2026-02-16 184350" src="https://github.com/user-attachments/assets/7f46ec2b-b1be-4f38-952b-a46f7b0ae0cf" />

<img width="380" height="338" alt="Screenshot 2026-02-16 184515" src="https://github.com/user-attachments/assets/713f0018-f151-404e-98db-04d0a119793b" />

After connecting to the VM, enable Internet Information Services(IIS) by opening the control Panel and selecting Turn Windows features on or off. Scroll through the list, find Internet Information Services (IIS), and check the box to enable it. Also enable CGI, go to World Wide Web Services -> Application Development Features -> [X] CGI

