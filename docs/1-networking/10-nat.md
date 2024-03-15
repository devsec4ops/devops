# NAT

##**What ?**
- NAT is like a receptionist in a building who translates incoming calls (packets) from the outside world to the correct internal extension (private IP address) and vice versa.
- It allows multiple devices in a private network to share a single public IP address, hiding internal IP addresses from external networks.

## **WHY ?**
- NAT conserves IPv4 addresses by allowing multiple devices in a private network to share a single public IP. 
- It enhances security by masking internal IP addresses from external networks. 
- NAT enables devices in private networks to access the internet while maintaining network privacy.

##**Types of NAT:**
1.  **Static NAT**:
- Maps a private IP address to a fixed public IP address.
- Provides one-to-one mapping between private and public IP addresses.
2.  **Dynamic NAT**:
- Maps multiple private IP addresses to a pool of public IP addresses.
- Assigns public IP addresses dynamically as needed, allowing devices to share public IP addresses.
3.  **PAT (Port Address Translation)**:
- Also known as NAT Overload or NAT with Port Address Translation.
- Maps multiple private IP addresses to a single public IP address using different port numbers.
- Enables many devices to share a single public IP address by using unique port numbers for each connection.

## **How ?**:
- Configure NAT on a router or firewall device that connects the private network to the public network.
- Define NAT translation rules specifying how private IP addresses should be mapped to public IP addresses.
- Choose the appropriate NAT type (static, dynamic, or PAT) based on network requirements and available IP address resources.
- Test and verify NAT functionality to ensure proper translation of IP addresses and connectivity between internal and external networks.

## **Interview Questions**:
1.  What is NAT, and why is it used in networking?
2.  Explain the difference between static NAT, dynamic NAT, and PAT.
3.  How does NAT help conserve IPv4 address space?
4.  What are the benefits and drawbacks of using NAT in network design?
5.  Describe the process of configuring NAT on a router or firewall device.
6.  How are NAT gateways used in cloud environments like AWS for outbound internet access?
7.  What are the security implications of using NAT in network architectures?