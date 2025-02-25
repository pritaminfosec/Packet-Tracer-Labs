**Lab 2. Assigning Static IP address to PC’s**


**Objective:**
1.	Assigning static IP addresses to PC 1 and PC 2.
2.	Checking connectivity between the PCs using the ping command.

**Description**

In this lab, we will use Class B IP addresses:
•	PC 1: 191.168.1.1
•	PC 2: 191.168.1.2

These are classful IP addresses, so the subnet mask will be automatically assigned by default during IPv4 configuration. We will configure static IPs and test connectivity between the two PCs by sending ping requests.

**Steps to Perform**
1. Assign Static IP Addresses

For PC 1:
1.	Go to PC 1.
2.	Open the Desktop Tab.
3.	Select the first option, IP Configuration.

![Image](https://github.com/user-attachments/assets/0eca65d3-91ea-4f7c-9364-c7b712052c7d)

4.	Under "IP Configuration," set the following:

o	IPv4 Address: 191.168.1.1
o	The default subnet mask will appear automatically.

![Image](https://github.com/user-attachments/assets/e4e38502-1170-4e74-8f38-97abf405085a)
 
For PC 2:
1.	Go to PC 2.
2.	Open the Desktop Tab.
3.	Select the first option, IP Configuration.
4.	Under "IP Configuration," set the following:
o	IPv4 Address: 191.168.1.2
o	The default subnet mask will appear automatically.

![Image](https://github.com/user-attachments/assets/053e8328-2ac4-4f43-9e92-20f191e16262)
 
2. Verify Connectivity
1.	On PC 1, go to the Desktop Tab and open Command Prompt.
2.	Type the following command:
ping 191.168.1.2
o	This sends a ping request from PC 1 to PC 2.

![Image](https://github.com/user-attachments/assets/03cc90fc-f92c-4c41-8b04-60fe56a96818)
 
4.	Check for a reply:
o	If a reply is received, the PCs are successfully connected.
o	If no reply is received, troubleshoot the IP configuration or connectivity.

![Image](https://github.com/user-attachments/assets/0006ca59-a5a5-40af-805c-765d92e80555)


________________________________________
