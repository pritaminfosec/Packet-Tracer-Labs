**Lab 1. Configuring DHCP with an Access Point and Wireless Devices**

**Objective:**
•	Connect devices to establish a network with both wired and wireless components.
•	Enable wireless capability on the laptop using the WPC300N adapter.
•	Configure the router's interfaces with IP addresses.
•	Exclude specific router IPs from DHCP assignment.
•	Set up DHCP pools for automatic IP allocation.
•	Assign IP addresses to PCs via DHCP.
•	Configure the access point with SSID and WPA2-PSK security.
•	Connect the smartphone to the wireless network using WiFi credentials.
•	Test network connectivity by pinging devices across the network.

**Description**
This lab focuses on setting up a network using a router, a switch, PCs, a laptop, and an access point to enable wireless connectivity. The primary goal is to configure DHCP on the router, enable automatic IP assignment for connected devices, and test wireless connectivity through an access point.

**What is an Access Point?**
An Access Point (AP) is a networking device that provides wireless connectivity to devices within a specific range. It acts as a bridge between wired and wireless networks, enabling wireless devices to connect to the LAN.

**Why is it needed?**
1.	Enhanced Mobility: Allows devices like laptops and smartphones to connect wirelessly, providing flexibility and ease of access.
2.	Extending Network Coverage: Expands the network's reach by providing wireless connectivity in areas where wired connections are impractical.
3.	Simplified Network Access: Enables multiple devices to connect seamlessly using wireless protocols, reducing the need for physical connections.

**Steps to Perform**
1.	Hardware Setup:
•	Connect one router, one switch, two PCs, and a laptop to the switch.
•	Connect one access point, one laptop, and one smartphone to the access point.

2.	Configure Wireless Network Interface:
•	On the laptop connecting to the access point:
•	Go to the hardware configuration.
•	Remove the NIC port and add the WPC300N wireless interface.

![Image](https://github.com/user-attachments/assets/d08d969e-b520-47e0-b491-0e71134ebd73)
 
The WPC300N is a wireless network adapter designed for laptops to enable WiFi connectivity. It is a PCMCIA card that provides support for the 802.11n standard, ensuring faster speeds and better range compared to older standards like 802.11g. The adapter is ideal for connecting to wireless networks in environments where a built-in WiFi module is not available or needs an upgrade. It supports robust encryption methods, such as WPA2-PSK, for secure wireless communication.

3.	Configure DHCP on the Router:
-	Access the router and enter configuration mode: conf t
-	Configure Gig 0/0/0 interface: 
-	int Gig 0/0/0
-	ip add 192.168.1.1 255.255.255.0
-	no shut
-	Configure Gig 0/0/1 interface: 
-	int Gig 0/0/1
-	ip add 192.168.2.1 255.255.255.0
-	no shut
-	Exclude router IP addresses from the DHCP pool:
-	ip dhcp excluded-address 192.168.1.1
-	ip dhcp excluded-address 192.168.2.1
-	Create DHCP pools:
-	For 192.168.1.1 network:
-	ip dhcp pool 192.168.1.1
-	default-router 192.168.1.1
-	network 192.168.1.0 255.255.255.0
-	For 192.168.2.1 network:
-	ip dhcp pool 192.168.2.1
-	default-router 192.168.2.1
-	network 192.168.2.0 255.255.255.0
-	Save the configuration: do wr

5.	Assign IP to PCs via DHCP:
•	On PCs connected to the switch, enable DHCP to assign IP addresses automatically.

6.	Configure the Access Point:
-	Navigate to the configuration panel of the access point:
-	Go to Config -> Global -> Port 1.
-	Set the SSID (WiFi name) under SSID.

An SSID (Service Set Identifier) is a unique name assigned to a wireless network. It is used to identify and distinguish one Wi-Fi network from another. When devices search for available networks, they display a list of SSIDs within range. The SSID can be a default name set by the router or customized by the network administrator.

-	Configure authentication: 
-	AuthN -> WPA2-PSK
-	PSK Pass -> [Enter WiFi password]

WPA2-PSK (Wi-Fi Protected Access 2 - Pre-Shared Key) is a security protocol used to protect wireless networks. It is the most common encryption method for home and small business Wi-Fi networks.

-	WPA2: Refers to the second generation of the Wi-Fi Protected Access security protocol, which offers stronger encryption than its predecessor (WPA).
-	PSK (Pre-Shared Key): The "pre-shared key" is a password or passphrase that both the router and the devices (such as laptops, smartphones, etc.) use to authenticate the connection.
-	Encryption: WPA2-PSK uses AES (Advanced Encryption Standard) to encrypt data, providing a high level of security.
-	Usage: WPA2-PSK is commonly used in home networks where simplicity is needed for secure Wi-Fi access. Devices connect to the network by entering the pre-shared key (password).
-	Security: While WPA2-PSK offers strong security, its effectiveness depends on the strength and secrecy of the pre-shared key. If the key is weak or shared inappropriately, the network may be vulnerable to unauthorized access.

![Image](https://github.com/user-attachments/assets/049ae6e5-4a6f-485c-87bc-19fb518eaef6)
 
7.	Connect the Smartphone to WiFi:
•	On the smartphone:
•	Go to Config -> Wireless 0.
•	Enter the SSID (WiFi name).
•	Set authentication:
	AuthN -> WPA2-PSK
	Write WiFi Pass -> [Enter WiFi password]

![Image](https://github.com/user-attachments/assets/9db226cb-29f8-476c-9366-a5fac6fcfa02)

![Image](https://github.com/user-attachments/assets/8e38defe-175e-46bd-9117-892a475003dc)
 
8.	Test Connectivity:
o	Use the smartphone to ping devices on the other side of the network to verify connectivity.
 
![Image](https://github.com/user-attachments/assets/3361fc20-de4a-4d2a-b733-fbf8086ed9ba)

![Image](https://github.com/user-attachments/assets/3b205bb3-7cc1-432b-86bd-0c9c58c41ce9)

Final Network Architecture

 ![Image](https://github.com/user-attachments/assets/64381fd7-2f6b-4f7f-9f0f-cbb2b68296ac)
________________________________________


