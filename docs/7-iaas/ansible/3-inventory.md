#**Inventory**

## **What** is Inventory ?

**Ansible Inventory**: Ansible's inventory is like a phone book for your network, where you sort servers into groups for easy management, similar to how you might organize contacts by family or work. You can also give specific settings to groups or servers, just like assigning ringtones to contacts.

There are two types of inventories in Ansible:

1.  Static Inventory: A manually created and maintained list of servers.
2.  Dynamic Inventory: Automatically updates and fetches server lists from external sources like cloud providers.

The main difference is that static inventory is fixed until you change it, while dynamic inventory updates automatically based on the current state of your servers in the cloud or other environments.

## **How** to create an Inventory ?

**Static Inventory File**:

Create an inventory file named `hosts.ini`:

<pre>hosts.ini<code>
[webservers]
web1.example.com
web2.example.com

[dbservers]
db1.example.com
</code></pre>

**Dynamic Inventory File**:
Please refer projects folder for this example.

## **Why** to create an Inventory ?

For instance, to verify the uptime of all your web servers grouped in your Ansible inventory, you can utilize the following ad-hoc command:
<pre><code>
ansible webservers -i hosts.ini -m command -a "uptime"
</code></pre>   
In this command:

-   `webservers` is the group name specified in your `hosts.ini` inventory file, representing all your web server nodes.
-   `uptime` is the command executed on each server within the `webservers` group to check how long the servers have been running.
  

## **Assignments**
Assignment 1: Create an Inventory File

-   Create an inventory file that includes at least two groups: `app_servers` and `db_servers`.
-   Add at least two hosts to each group.
-   Assign a variable `ansible_user` to each group, with `app_servers` using `appadmin` and `db_servers` using `dbadmin`.

Assignment 2: Execute a Ping Module

-   Using the inventory file created, write an Ansible ad-hoc command to ping all hosts in the `app_servers` group.

## **Interview Questions**

1.  **What is an Ansible inventory, and why is it important?**
     - An inventory file defines the hosts and groups of hosts upon which commands, modules, and tasks in a playbook operate. It is crucial for organizing managed nodes and defining where Ansible should perform its automation tasks.
2.  **How can you group hosts in an Ansible inventory file, and what are the advantages of grouping?**
    -  Hosts can be grouped under a named group in an inventory file for easier management, parallel execution across the group, and the ability to assign group-specific variables. This organization enhances readability and efficiency in playbook execution.
3.  **Explain the difference between static and dynamic inventory in Ansible.**
    - A static inventory is defined in a file (like INI or YAML format) and does not change unless manually updated. A dynamic inventory pulls host information dynamically from external sources, such as cloud providers, making it suitable for environments where host configurations frequently change.
4.  **How can you specify a different SSH port for a host in the inventory file?**
    - You can specify a different SSH port for a host by defining it in the inventory file next to the host's address, using the syntax `hostname ansible_port=your_port_number`.