# **Patching**

## Sytem Updates

### **What** are System Updates?

-   Updates make sure your Linux system has the latest features and security fixes. It's like updating your phone's operating system to get new features and stay safe.

### **Why** Update?

-   To protect your system from hackers.
-   To fix bugs that might cause problems.
-   To get the latest features and improvements.

### **How** to Update Your System:

1.  For Ubuntu/Debian systems:

    -   Check for updates: `sudo apt update`
    -   Install updates: `sudo apt upgrade`
2.  For Fedora/Red Hat systems:

    -   Check and install updates: `sudo dnf upgrade`

## Package Management

### **What** is Package Management?

-   Package management involves installing, updating, and removing software packages. Think of it as managing apps on your phone.

### **Why** Manage Packages?

-   To install new software or apps you need.
-   To remove software you don't use anymore.
-   To keep your software up to date with the latest versions.

### **How** to Manage Packages:

1.  Installing a new package:

    -   Ubuntu/Debian: `sudo apt install packageName`
    -   Fedora/Red Hat: `sudo dnf install packageName`
2.  Removing a package:

    -   Ubuntu/Debian: `sudo apt remove packageName`
    -   Fedora/Red Hat: `sudo dnf remove packageName`
3.  Searching for a package:

    -   Ubuntu/Debian: `apt search packageName`
    -   Fedora/Red Hat: `dnf search packageName`

* * * * *

## Example: Setting Up a Web Server

-   Objective: Install Apache web server on your Linux system.
-   Steps:
    1.  Update your system using the update commands mentioned above.
    2.  Install Apache:
        -   Ubuntu/Debian: `sudo apt install apache2`
        -   Fedora/Red Hat: `sudo dnf install httpd`
    3.  Check if Apache is running: `sudo systemctl status apache2` or `httpd` depending on your system.

* * * * *

## Assignments

1.  Install a Software: Choose any software, install it using your system's package manager, and then use it.
2.  Remove the Software: After trying the software, remove it from your system using the package manager.

* * * * *

## Interview Questions

1.  What command would you use to update all packages on a Ubuntu system?
2.  How do you install a package using DNF?
3.  What's the difference between `apt` and `apt-get`?
4.  How can you list all installed packages on your Linux system?

