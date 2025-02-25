**Lab 1. Switch Configuration and Remote Management Using Telnet**

**Objective:**
-	Establish a console connection between a laptop and a switch for initial setup.
-	Configure the switch hostname for identification.
-	Assign an IP address to VLAN 1 to enable remote connectivity.
-	Set up Telnet for remote access management.
-	Divide devices into departments and verify connectivity between them.
-	Test and verify remote access to the switch using Telnet.

**Description**
This lab demonstrates the configuration of a switch using a console connection and enabling remote access through Telnet. You will assign an IP address to the switch's VLAN, configure Telnet for remote management, and verify connectivity between devices in different departments.

**What is Telnet, and Why Do We Need It?**
Telnet is a network protocol used to remotely manage devices over a network by establishing a text-based command-line interface. It allows administrators to access and configure devices from anywhere within the network, saving time and effort compared to physical access. However, Telnet transmits data in plain text, making it less secure compared to alternatives like SSH.

**Steps to Perform**
1.	Connect the Laptop to the Switch:
•	Use an RS-232 cable to connect the laptop’s serial port to the console port of the switch.

2.	Access the Switch Terminal:
•	Open terminal software on the laptop  to start configuring the switch.

3.	Change the Switch Hostname:
•	Enter global configuration mode: conf t
•	Set the hostname to SW1: hostname SW1

![Image](https://github.com/user-attachments/assets/2ca4d5eb-53be-45db-b501-d3c129bbd345)
 
4.	Assign IP Address to VLAN 1:
-	View VLAN details: show vlan brief
-	Enter interface VLAN 1 configuration mode: interface vlan 1
-	Assign an IP address to VLAN 1: ip address 192.168.1.1 255.255.0.0
-	Enable the interface: no shutdown

![Image](https://github.com/user-attachments/assets/07e2dc10-32c3-40e4-84a6-6c31e91eb26b)
 
5.	Verify VLAN IP Configuration:
-	Check and confirm the assigned IP in the running configuration file: sh run

![Image](https://github.com/user-attachments/assets/4f0b42df-43d6-4229-b805-2475a7026a55)
 
6.	Configure Telnet on the Switch:
-	Enter line VTY configuration mode: line vty 0 4
-	Set a password for Telnet access: password ccna 
The above command is used to configure the Virtual Terminal (VTY) lines, which are logical connections allowing remote access to the device via protocols like Telnet or SSH. 0 4: Refers to the range of VTY lines being configured. Most Cisco devices have 5 VTY lines numbered 0 to 4 by default, which means up to 5 concurrent remote sessions can connect.
-	Enable login authentication: login

![Image](https://github.com/user-attachments/assets/a227fff1-01b9-40d3-998e-3c94e10d3a10)
 
7.	Divide Devices into Departments:
-	Assign IP addresses to devices in HR, Sales, and HelpDesk departments.

8.	Verify Device Connectivity:
-	Test connectivity between departments using the ping command.
 
![Image](https://github.com/user-attachments/assets/187c976f-5a9b-405f-a8db-597721a058cd)

![Image](https://github.com/user-attachments/assets/6cb3e1a1-32ad-4831-b9d1-787351ca90fc)

9.	Test Telnet Access to the Switch:
-	From any computer, type the following command in the terminal: telnet 192.168.1.1
-	Enter the Telnet password (ccna) when prompted to gain remote access to the switch.

![Image](https://github.com/user-attachments/assets/d0761888-ba63-46bd-b884-a273b86c603d)

**Final Network Architecture**

![Image](https://github.com/user-attachments/assets/f2274a3f-a175-426d-b393-297b5e183ff4)

________________________________________
