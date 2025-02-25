**Lab 2. DHCP Configuration**

**Objective:**
•	Set up a DHCP server and assign it a static IP address.
•	Enable DHCP services to assign dynamic IP addresses to devices.
•	Verify that devices on the network can communicate using dynamically assigned IP addresses.

**Description**
This lab demonstrates how to configure a DHCP server to assign IP addresses dynamically to devices in a network. You will set up a server as the DHCP host, enable DHCP services, and verify that devices on the network can communicate with each other.

What is DHCP and Why Do We Need It?
Dynamic Host Configuration Protocol (DHCP) is a network management protocol that automates the process of assigning IP addresses and other network configuration parameters (like subnet mask, gateway, and DNS servers) to devices on a network.

Why We Need DHCP
1.	Automation: DHCP eliminates the need for manual IP address configuration, saving time and reducing errors.
2.	Scalability: It is particularly useful in networks with many devices, ensuring efficient IP address allocation.
3.	Flexibility: DHCP allows devices to obtain IP addresses dynamically, making it easier to connect new devices or relocate existing ones without reconfiguration.

**Steps to Perform**
1.	Set Up the Network Devices:
o	Take one switch, one server (for DHCP configuration), three PCs, and one laptop.

2.	Assign an IP Address to the DHCP Server:
o	Access the server’s settings and assign it a static IP address: 192.168.1.1

![Image](https://github.com/user-attachments/assets/bd43474a-36e3-4c47-9ff2-68dc8180c3d4)
 
3.	Enable DHCP Services:
o	On the server, navigate to Services and select the DHCP option.
o	Enable the DHCP service, which will automatically configure the DHCP scope.

4.	Default IP Address Range:
o	The DHCP server will assign IP addresses dynamically from the default range: 192.168.0.1 to 192.168.255.255

![Image](https://github.com/user-attachments/assets/fbddc13c-6389-496c-a2de-1c9b0ba9e442)
 
5.	Verify IP Address Assignment:
o	Check the IP address assigned to each PC and laptop to confirm they have received a dynamic IP address from the DHCP server.

6.	Test Network Connectivity:
o	Use the ping command from one PC to another to verify communication between devices. For example: ping 192.168.x.x

![Image](https://github.com/user-attachments/assets/d268b744-0d4c-4b18-9327-c7e80b9f1c18)

![Image](https://github.com/user-attachments/assets/3c1d1624-c0a0-449d-904b-5c3120759c31)

![Image](https://github.com/user-attachments/assets/ef0a6d09-a8ce-46dd-9166-4af532b9a52e)

7.	Confirm Successful Configuration:
o	If the devices reply to the ping requests, it confirms that the DHCP service is working and that the devices are properly connected.

**Final Network Architecture**
![Image](https://github.com/user-attachments/assets/bac6c45b-a5e8-4769-af74-7a157ee41c90)
________________________________________
