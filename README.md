# Tech Solutions Inc. Part 2





## Scenario / Objective

### Business Scenario: Tech Solutions Inc.

**Company Overview:**
Tech Solutions Inc. is a growing IT consulting firm that provides network solutions and cybersecurity services to small and medium-sized businesses. The company has recently moved into a new office building and needs to set up a robust and secure network infrastructure to support its operations. The office layout includes the following departments:

1. **Administration**
2. **Sales and Marketing**
3. **Technical Support**
4. **Research and Development (R&D)**
5. **Finance**
6. **Human Resources (HR)**

**Network Requirements:**

1. **Network Layout:**
    - The network should include separate VLANs for each department to enhance security and manageability.
    - The main office network will consist of three floors, each housing different departments.
2. **IP Addressing:**
    - Implement a suitable IP addressing scheme using private IP addresses (e.g., 192.168.X.0/24).
    - Each department (VLAN) will have its own subnet.
3. **Routing:**
    - Use a core router to handle inter-VLAN routing.
    - Implement dynamic routing protocols (e.g., OSPF) to ensure efficient routing between different subnets.
4. **Switching:**
    - Use Layer 2 switches to handle intra-VLAN traffic.
    - Implement trunking between switches to support VLANs across multiple switches.
5. **Wireless Network:**
    - Set up a wireless network with access points for guest access and employee mobility.
    - Configure a separate SSID for guests with limited access to the network.
6. **Security:**
    - Implement Access Control Lists (ACLs) on the router to restrict unauthorized access between VLANs.
    - Use port security features on switches to prevent unauthorized devices from connecting to the network.
    - Configure a firewall to protect the network from external threats.
7. **Internet Access:**
    - Configure Network Address Translation (NAT) on the router to enable internet access for all internal devices.
    - Set up a proxy server to monitor and control internet usage.
8. **Servers:**
    - Install and configure essential servers, including a DHCP server, DNS server, and a file server.
    - Ensure redundancy and backup solutions for critical data.
9. **VoIP:**
    - Implement a VoIP system to handle internal and external communication needs.
    - Ensure Quality of Service (QoS) to prioritize VoIP traffic.
10. **Monitoring and Management:**
    - Set up network monitoring tools to track performance and detect issues.
    - Implement a centralized management system to manage devices and configurations.

### Detailed Network Design:

**First Floor (Administration and Sales/Marketing):**

- VLAN 20: Administration (192.168.20.0/24)
- VLAN 30: Sales and Marketing (192.168.30.0/24)

**Second Floor (Technical Support and R&D):**

- VLAN 40: Technical Support (192.168.40.0/24)
- VLAN 50: R&D (192.168.50.0/24)

**Third Floor (Finance and HR):**

- VLAN 60: Finance (192.168.60.0/24)
- VLAN 70: HR (192.168.70.0/24)

**Guest Wi-Fi:**

- VLAN 80: Guest Wi-Fi (192.168.80.0/24)

**Equipment:**

- **Core Router**: Cisco ISR Router
- **Layer 2 Switches**: Cisco 2960 Series Switches
- **Wireless Access Points**: Cisco Aironet
- **Servers**: DHCP, DNS, File Server, Proxy Server
- **Firewall**: Cisco ASA

### Key Objectives:

- Design a scalable and secure network infrastructure.
- Ensure seamless connectivity and communication across all departments.
- Implement robust security measures to protect sensitive company data.
- Provide reliable and controlled internet access.
- Enable efficient network management and monitoring.



## Skills Learned



- **VLAN Configuration:** Demonstrated ability to set up and manage multiple VLANs for network segmentation and enhanced security, including Guest Wi-Fi, Corporate Wi-Fi, and management VLANs.
- **Inter-VLAN Routing:** Successfully configured subinterfaces on Core Layer Router for efficient inter-VLAN routing, ensuring seamless communication between different network segments.
- **Wireless LAN Controller (WLC) Setup:** Proficient in adding and configuring Wireless LAN Controllers (WLCs) within a network, utilizing online workarounds to overcome software limitations in Packet Tracer.
- **DHCP Configuration:** Expertly set up DHCP scopes for multiple VLANs, ensuring dynamic IP address allocation and network connectivity for devices on various VLANs.
- **Interface and Network Configuration:** Skilled in configuring network interfaces, assigning VLANs, and implementing wireless security protocols (WPA2-Personal) for secure and efficient network management.
- **Troubleshooting and Testing:** Adept at troubleshooting and resolving connectivity issues, validating network configurations through successful testing, including pings and web navigation.

## Tools Used



- **VLAN Configuration:**
    - Network Switches (for setting up VLANs)
- **Inter-VLAN Routing:**
    - Core Layer Router (for configuring subinterfaces)
- **Wireless LAN Controller (WLC):**
    - WLC Device (for managing Wi-Fi networks)
    - Lightweight Access Points (APs)
- **DHCP Configuration:**
    - DHCP Server (for setting up DHCP scopes)
- **Network Interfaces and Connectivity:**
    - PCs or Laptops (for testing connections)
    - Web Browser (for accessing WLC interface)
- **Troubleshooting Tools:**
    - Ping Command (for connectivity testing)
    - Network Interface Configurations (for adjusting connections)

## Steps



In part 1 of this project I implemented 5 of the 10 requirements listed above for Tech Solutions Inc.

- Network layout
- IP addressing
- Routing
- Switching
- Servers

In part 2 of my project I will be addressing the following:

- Wireless Networks

### Wireless Network

![part2-1.png](https://github.com/Daklan85/Tech-Solutions-Company-Part2/blob/main/screenshots/part2-1.png)

I have configured a VLAN for Guest Wi-Fi on all my switches. Next, I need to add VLANs for Corporate Wi-Fi and management to configure a Wireless LAN Controller (WLC). I will add these new VLANs to my switches, name them appropriately, and update the VLAN key to the left of my topology. Additionally, I will configure these VLANs as subinterfaces on my Core Layer Router to enable inter-VLAN routing between subnets. After connecting the Lightweight APs to the access layer switch, I will use an online workaround since Packet Tracer does not support normal WLC configuration. I will not detail the workaround in my lab report as it is not representative of real-world configurations. Once the connections are made and configured using the workaround, setting up the WLC will be identical to a real-world deployment, depending on the WLC used.

![part2-2.png](https://github.com/Daklan85/Tech-Solutions-Company-Part2/blob/main/screenshots/part2-2.png)

Next, I will add DHCP scopes for each new VLAN on my DHCP server. The three VLANs in my scope will be used for Guest Wi-Fi, Corporate Wi-Fi, and management. The WLC's IP address is 192.168.110.2.

![part2-3.png](https://github.com/Daklan85/Tech-Solutions-Company-Part2/blob/main/screenshots/part2-3.png)

I configure the Wireless LAN Controller and the PC with the IP configuration shown above. I then ping the WLC from the PC to ensure there is a connection. After a successful ping, I open the web browser on the PC and navigate to the WLC IP address.

![part2-4.png](https://github.com/Daklan85/Tech-Solutions-Company-Part2/blob/main/screenshots/part2-4.png)

I enter the credentials highlighted in the red box.

![part2-5.png](https://github.com/Daklan85/Tech-Solutions-Company-Part2/blob/main/screenshots/part2-5.png)

I enter a system name, assign a management IP address within my management VLAN subnet, and use VLAN ID 110 for management.

![part2-6.png](https://github.com/Daklan85/Tech-Solutions-Company-Part2/blob/main/screenshots/part2-6.png)

I create my first employee network and choose Guest since I am using WPA2-Personal for security. For this lab, I will use the same password, Password123!, for all configurations. I then hit "Next" and apply the configuration.

![part2-7.png](https://github.com/Daklan85/Tech-Solutions-Company-Part2/blob/main/screenshots/part2-7.png)

After initially setting up the WLC, the PC can no longer ping or reach it in the web browser due to the trunk link between the WLC and the switch. I moved the PC to another interface on the switch and configured that link as an access link for VLAN 110. I was then able to ping the WLC and use HTTPS in the address bar to navigate to the login screen.

![part2-8.png](https://github.com/Daklan85/Tech-Solutions-Company-Part2/blob/main/screenshots/part2-8.png)

After logging in, I first want to set up my interfaces. I navigate to the "Controller" tab at the top and then select "Interfaces" from the sidebar. I create a new interface named VLAN80 for my guest Wi-Fi and assign it to VLAN 80. The screen for the screenshot above appears, and I change the port to 1, referring to the physical interface connection between my WLC and switch. I identify VLAN number 80 and choose an IP address from my excluded list defined in my DHCP scope earlier. At the bottom, I enter my DHCP server address so my address scope can be assigned by DHCP to end users when they connect. I then hit "Apply.”

![part2-9.png](https://github.com/Daklan85/Tech-Solutions-Company-Part2/blob/main/screenshots/part2-9.png)

I then navigate to the "WLANS" tab at the top. I had already created a Guest Wi-Fi WLAN when I initially set up the WLC. I make sure it is enabled, change the interface to VLAN80, and hit "Apply." I initially set up the security for WPA2-Personal with a password earlier.

![part2-11.png](https://github.com/Daklan85/Tech-Solutions-Company-Part2/blob/main/screenshots/part2-11.png)

I create a new WLAN for Corporate Wi-Fi the same way I created the Guest Wi-Fi, using WPA2-Personal for security. I spent several hours trying to get my Radius Server to associate with the WLC for this account to use Radius server credentials, but it may not be possible with all these workarounds.

![part2-13.png](https://github.com/Daklan85/Tech-Solutions-Company-Part2/blob/main/screenshots/part2-13.png)

I set up two laptops: one connects to Guest Wi-Fi, and the other to Corporate Wi-Fi. Wi-Fi access is now set up and ready to use.
