# **Networking**

This module introduces you to the fundamentals of networking in Linux, including how to understand, configure, and manage network interfaces, utilize basic networking commands, and apply basic firewall and security measures using iptables and firewalld.

## **What** is Linux Networking ?

Networking in Linux allows your system to communicate with other computers and the internet. It involves various components such as network interfaces, IP addresses, DNS servers, and routing.

-   Network Interfaces: These are the gateways through which a Linux system interacts with the network. Examples include Ethernet (e.g., eth0), WLAN (e.g., wlan0), and loopback (lo).
-   IP Address: A unique identifier assigned to each device on a network, necessary for sending and receiving data.

## **How** to Configure Network Interfaces ?

Linux provides several tools for network configuration, including `ifconfig`, `ip`, and graphical tools like `NetworkManager`.

1.  Using `ifconfig` (deprecated):

    -   View all interfaces: `ifconfig -a`
    -   Configure an IP address: `sudo ifconfig eth0 192.168.1.2 netmask 255.255.255.0 up`
2.  Using `ip` command (recommended):

    -   List all interfaces: `ip link show`
    -   Set an IP address: `sudo ip addr add 192.168.1.2/24 dev eth0`
    -   Bring an interface up or down: `sudo ip link set eth0 up` or `down`
3.  Restarting the network service:

    -   On systems using systemd: `sudo systemctl restart NetworkManager`

## Basic Networking **Commands**

-   `ping`: Tests connectivity between your computer and a specified host.
    -   Usage: `ping google.com`
-   `traceroute` (tracert on some systems): Shows the path packets take to reach a host.
    -   Usage: `traceroute google.com`
-   `netstat`: Displays network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.
    -   Usage: `netstat -tuln`
-   `nslookup`: Queries Internet domain name servers for DNS details.
    -   Usage: `nslookup google.com`

## **Firewall** and **Security** Basics

Linux firewalls manage incoming and outgoing traffic based on predetermined security rules. Two popular firewall solutions in Linux are `iptables` and `firewalld`.

1.  iptables:

    -   Viewing rules: `sudo iptables -L`
    -   Allowing traffic on a port: `sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT`
    -   Blocking an IP address: `sudo iptables -A INPUT -s 123.45.67.89 -j DROP`
2.  firewalld (CentOS/RHEL 7 and above):

    -   Start/Enable firewalld: `sudo systemctl start firewalld && sudo systemctl enable firewalld`
    -   Check status: `sudo firewall-cmd --state`
    -   Allowing traffic on a port: `sudo firewall-cmd --permanent --add-port=80/tcp`
    -   Reloading firewall rules: `sudo firewall-cmd --reload`

    Remember, `firewalld` uses zones and services for managing rules, which can simplify or complicate configurations depending on your familiarity.

## **Assignments**

1.  Configure a static IP: Assign a static IP address to a network interface on your Linux machine.
2.  Analyze network traffic: Use `ping` and `traceroute` to analyze network traffic to your favorite website.
3.  Configure firewall rules: Add a rule to allow HTTP traffic (port 80) through your firewall using both `iptables` and `firewalld`.

## **Interview** **Questions**

1.  How do you assign a static IP address to a network interface in Linux?
2.  What is the difference between `iptables` and `firewalld`?
3.  How can you check the open ports on your Linux system?
4.  Explain the purpose of the loopback interface on a Linux system.
