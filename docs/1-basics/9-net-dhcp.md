#DHCP

## **What?**
- DHCP is like a waiter in a restaurant who assigns tables (IP addresses) to customers (devices) as they come in, ensuring everyone gets seated and served without having to wait too long.
## **Why?**
- Simplifies network administration by automating IP address allocation.
- Eliminates the need for manual IP configuration, reducing human errors.
- Supports dynamic IP address assignment, optimizing IP address usage.
- Facilitates easy addition and removal of devices from the network.
## **How?**
- When a device connects to the network, it sends a DHCP discover message.
- A DHCP server responds with an offer, providing an available IP address.
- The device sends a request for the offered IP address.
- The DHCP server acknowledges the request and assigns the IP address to the device.
- The device configures its network settings using the assigned IP address, subnet mask, default gateway, and DNS servers.

## **Interview Questions:**
- What is DHCP, and why is it used in networking?
- Explain the DHCP lease process.
- How do DHCP relay agents work, and when are they used?
- What are the benefits of using DHCP in a large-scale network environment?
- How does DHCP help in AWS DevOps environments, and what are DHCP option sets used for?