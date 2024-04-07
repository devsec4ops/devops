# **Architecture**

Think of Docker like a magical shipping service for your software. This service has three main parts that make sure your software gets where it needs to go, safely and efficiently.

![Docker Architecture](<Docker Architecture.png>)
Source : GeeksforGeeks

## **Docker Client **(The Order Taker)

-   What It Does: Just like when you order a pizza, you tell the Docker Client what you want Docker to do (like creating a new container for your app).
-   How It Works: You give commands (like `docker run`), and it's like calling the pizza place to place your order. The Docker Client makes sure your request gets to the right place, which is the Docker Daemon.

## **Docker Daemon **(The Kitchen): 

-   What It Does: This is where the magic happens. The Docker Daemon prepares everything you need. If Docker was a restaurant, the Daemon would be the kitchen where your order (container) is prepared.
-   How It Works: It takes your order from the Docker Client, gets the ingredients (Docker images), and cooks up your order (runs your container). It makes sure your software runs exactly how you want it.

## **Docker Registry **(The Food Storage): 

-   What It Does: Imagine a giant fridge and pantry where all the ingredients (images) are kept. This is the Docker Registry, a place where images are stored.
-   How It Works: Before the Docker Daemon can cook your order, it needs ingredients. If it doesn't have them already, it goes shopping at the Docker Registry. You can use a big supermarket (Docker Hub) or your own private store.

## **Simplified Overview**

-   You Place Your Order: You use the Docker Client to say, "I want a container that runs my app."
-   The Kitchen Prepares Your Order: The Docker Daemon checks if it has the right ingredients (images). If not, it gets them from the Registry. Then, it cooks up your container.
-   Enjoy Your Dish: Your app runs inside the container just the way you wanted.

In this simplified view, Docker ensures your software runs smoothly in its container, just like a well-prepared meal, no matter where you decide to enjoy it!