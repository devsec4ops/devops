#**Ports and IP Address**

### **What?**
-   **Ports**: Ports are like different doors in a big building. Each door leads to a different room where different services or activities happen.
-   **IP Address**: An IP address is like a home address for your computer or device on the internet. It helps data find its way to the right place, just like a home address helps mail reach the right house.

```
IP Address + PORT number = Socket Address
```

### **Why?**
-   **Ports**: They allow multiple services to operate on the same device without getting mixed up.
-   **IP Address**: It ensures that data reaches the correct device on the internet.

### **How?**

#### **Ports**: 
Each service or program running on a device listens to a specific port number for incoming data. When data arrives at the device, it's directed to the appropriate port, just like a letter is directed to the right room through a specific door.

| Port Number | Service | Protocol | Description |
| --- | --- | --- | --- |
| 21 | FTP | TCP | File Transfer Protocol (FTP) |
| 22 | SSH | TCP | Secure Shell (SSH) for secure remote access |
| 23 | Telnet | TCP | Telnet protocol for remote login |
| 25 | SMTP | TCP | Simple Mail Transfer Protocol (SMTP) for email transfer |
| 53 | DNS | TCP/UDP | Domain Name System (DNS) for translating domain names |
| 80 | HTTP | TCP | Hypertext Transfer Protocol (HTTP) for web browsing |
| 110 | POP3 | TCP | Post Office Protocol version 3 (POP3) for email access |
| 143 | IMAP | TCP | Internet Message Access Protocol (IMAP) for email access |
| 443 | HTTPS | TCP | HTTP Secure (HTTPS) for secure web browsing |
| 3306 | MySQL | TCP | MySQL Database server |
| 3389 | RDP | TCP | Remote Desktop Protocol (RDP) for remote access |

#### **IP Address**: 
- Devices are assigned unique IP addresses, similar to how houses have unique addresses. When data is sent over the internet, it's labeled with the destination IP address so that routers know where to send it.
- IP has mainly two versions 
    -   IPv4:
        -   Major Use: Legacy protocol.
        -   Address Format: 32-bit decimal (e.g., 192.168.1.1).
        -   Address Space: Limited (4.3 billion addresses).
        -   Challenges: Address exhaustion.
    -   IPv6:
        -   Major Use: Next-generation protocol.
        -   Address Format: 128-bit hexadecimal (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334).
        -   Address Space: Vast (practically limitless).
        -   Features: Improved security and support for more devices.
    
- IP addresses are divided into five classes: A, B, C, D, and E (D & E can be ignored tho)

    -   **Class A**:
        - In real networking terms, Class A addresses are like a large country with many states but only a few major cities. We divide it this way because we need a lot of addresses in each state, even though there aren't many states.
        - Major Use: Public networks, mainly by large organizations or internet service providers (ISPs).
        - Default Subnet Mask: 255.0.0.0
        - Range: 1.0.0.0 to 126.0.0.0
        - Example: ISPs assigning IP addresses to their customers.
    
    -   **Class B**:
        - Class B addresses are comparable to a big state with several counties but fewer cities in each county. We divide it like this because we want each county to have its own set of addresses, even if there aren't many counties.
        - Major Use: Both public and private networks, commonly by medium-sized organizations or educational institutions.
        - Default Subnet Mask: 255.255.0.0
        - Range: 128.0.0.0 to 191.255.0.0
        - Example: Companies setting up their own internal networks.
   
    -   **Class C**:
        - Class C addresses resemble a small town with only a few streets and houses on each street. We divide it this way because we want each street to have its own addresses, even if there aren't many streets.
        - Major Use: Private networks, often by small businesses or home networks.
        - Default Subnet Mask: 255.255.255.0
        - Range: 192.0.0.0 to 223.255.255.0
        - Example: Home Wi-Fi networks or small office networks.
   
-   **Subnetting**:
    -   When a network becomes overcrowded, we divide it into smaller neighborhoods (subnets) so that each group of devices (network) can have its own space without overcrowding. It helps us organize the network better and makes communication between devices smoother.



### **Real World Example**
-   Consider a computer with a web server using port 80 and an email server using port 25. Without ports, data collisions would occur. Ports provide designated spaces for each application to communicate, avoiding confusion.
-   If you have two computers with web servers using port 80, each computer's IP address ensures that data sent to port 80 reaches the intended web server on that specific computer

### **Assignments**
-   Identify the port numbers commonly used for web traffic, email, and secure web browsing.
-   Configure a firewall to allow traffic on specific ports only.

### **Interview Questions**
-   What is the purpose of ports in networking?
-   How does an IP address help in sending data over the internet?
-   Can you give an example of a real-world scenario where ports and IP addresses are used?