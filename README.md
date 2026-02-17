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

<img width="383" height="336" alt="Screenshot 2026-02-16 184350" src="https://github.com/user-attachments/assets/7f46ec2b-b1be-4f38-952b-a46f7b0ae0cf" />

<img width="380" height="338" alt="Screenshot 2026-02-16 184515" src="https://github.com/user-attachments/assets/713f0018-f151-404e-98db-04d0a119793b" />

After connecting to the VM, enable Internet Information Services(IIS) by opening the control Panel and selecting Turn Windows features on or off. Scroll through the list, find Internet Information Services (IIS), and check the box to enable it. Also enable CGI, go to World Wide Web Services -> Application Development Features -> [X] CGI

<img width="456" height="376" alt="Screenshot 2026-02-16 184658" src="https://github.com/user-attachments/assets/2c7bc4de-ff14-47b1-a122-50aba7757750" />

Next, use the provided download link to download all required files for installing and running osTicket. Within the osTicket Installation folder, find PHP Manager and install it to continue with the setup process. https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD 

<img width="456" height="354" alt="Screenshot 2026-02-16 184731" src="https://github.com/user-attachments/assets/9c645985-1738-487c-bbcd-7f7c6fec6206" />

In the same folder, proceed with installing the Rewrite Module to further confifure the  enviroment.

<img width="594" height="281" alt="Screenshot 2026-02-16 185037" src="https://github.com/user-attachments/assets/626da21f-892b-468c-91d2-80205485cc56" />

<img width="560" height="398" alt="Screenshot 2026-02-16 185138" src="https://github.com/user-attachments/assets/e2615ba3-9b41-4cfd-bf0f-c003af8aea48" />

Create a new folder at PHP. Then extract the contents of PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and place all the files into the C:\PHP directory.

<img width="442" height="274" alt="Screenshot 2026-02-16 185327" src="https://github.com/user-attachments/assets/b112a17f-0ae4-4b45-8e8d-f02e1cd75bdd" />

From the osTicket Installation folder, run VC_redist.x86.exe to install the required Visual C++ Redistributable componets needed for proper system functionality.

<img width="454" height="358" alt="Screenshot 2026-02-16 185432" src="https://github.com/user-attachments/assets/94907e78-7a41-486b-bace-51c5008bd999" />

From the osTicket Installation folder, run MySQL 5.5.62(mysql-5.5.62-win32.msi) to install and configure the MySQL database server.

<img width="459" height="346" alt="Screenshot 2026-02-16 185816" src="https://github.com/user-attachments/assets/8a29a971-5e5b-4895-b83c-426522cba1a1" />

Use "root" as both the username and password for this lab environment, then click execute.

<img width="663" height="573" alt="Screenshot 2026-02-16 185959" src="https://github.com/user-attachments/assets/9b628049-c8e7-46e2-81a5-06c969cf8afe" />

Launch IIS Manager with administrative privileges. Register PHP by setting up the required configurations, then restart the server by choosing Restart within IIS Manager.

<img width="706" height="159" alt="Screenshot 2026-02-16 190251" src="https://github.com/user-attachments/assets/b711b1ec-4e1f-4079-b58c-79e953b896df" />

<img width="612" height="196" alt="Screenshot 2026-02-16 190339" src="https://github.com/user-attachments/assets/519a5d37-f054-4291-9ba8-fcc6c2073962" />

Navigate to the osTicket-Installation-Files folder, extract osTicket-v1.15.8.zip, and copy the upload folder to C:\inetpub\wwwroot. Once copied, rename the upload to osTicket.



