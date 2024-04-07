# **OSI Layer** 

## **What?** 

-   The OSI Model is like a factory assembly line for data communication, divided into 7 stages (layers). Each layer has a specific role, ensuring the product (data) is built correctly from start (creation) to finish (delivery).

## **Why?** 

-   Standardizes network communication for different technologies.
-   Simplifies troubleshooting by segmenting the network into manageable layers.
-   Promotes interoperability and compatibility among various network products.
-   Facilitates modular engineering, allowing changes in one layer without affecting others.


## **Architecture** 
![OSI Model](<OSI-Model.png>)
                        
Source : BybyteGo
## **Real-World Example:** Simple Web Application

Imagine you've built a simple blog where users can create accounts, post articles, and comment. The web application is accessible from any web browser.

#### OSI Model Layers in Action:
A protocol is a set of rules that govern how data is transmitted and received over a network.

1.  #### Physical Layer (Layer 1)

-   What It Does: Handles the physical connection between devices, like cables and Wi-Fi signals.
-   Protocols: Ethernet (for wired connections), Wi-Fi (for wireless connections).

#### Data Link Layer (Layer 2)

-   What It Does: Makes sure data packets go to the right device within a local network using hardware addresses.
-   Protocols: Ethernet (for addressing with MAC addresses), 
               PPP (Point-to-Point Protocol).

#### Network Layer (Layer 3)

-   What It Does: Routes data across the internet, finding the best path for it to travel from source to destination.
-   Protocols: IP (Internet Protocol, for routing), 
               ICMP (Internet Control Message Protocol, for error reporting).

#### Transport Layer (Layer 4)

-   What It Does: Breaks down data into packets for sending and then puts them back together at the destination. It checks if all data arrives correctly.
-   Protocols: TCP (Transmission Control Protocol, ensures data is received in order and intact), 
               UDP (User Datagram Protocol, for faster transmission without error checking).

#### Session Layer (Layer 5)

-   What It Does: Manages the start, keep-alive, and end of data exchanges or 'sessions' between two points.
-   Protocols: NetBIOS (Network Basic Input/Output System), 
               RPC (Remote Procedure Call).

#### Presentation Layer (Layer 6)

-   What It Does: Translates data between the application and the network. Converts data formats and encrypts/decrypts data.
-   Protocols: SSL/TLS (Secure Sockets Layer/Transport Layer Security, for encryption),
               JPEG, GIF (for image formats).


#### Application Layer (Layer 7)

-   What It Does: The layer you interact with directly. It's what you see and use, like websites or email.
-   Protocols: HTTP/HTTPS (HyperText Transfer Protocol/Secure, for web browsing), 
               FTP (File Transfer Protocol, for file downloads and uploads), 
               SMTP (Simple Mail Transfer Protocol, for sending emails).

## **User Interaction Flow**:

-   A user wants to read an article on your blog, so they type your blog's URL into their web browser.
-   Their computer sends a request across the internet to find your server where the blog is hosted.
-   The request travels down through the layers on the user's side, out into the network, and then up through the layers on the server side.
-   Your server processes the request (application layer), prepares the data (presentation layer), maintains the session (session layer), ensures correct delivery (transport layer), finds the route (network layer), sends it over the physical network (data link layer), and finally, through the cables or Wi-Fi to the user's device (physical layer).
-   The user's browser receives the data, interprets it, and displays the blog article for them to read.