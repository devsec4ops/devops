#Modules

##**What** is Module ?

Think of preparing a large meal for a party. You, as the chef, have a recipe book (the playbook) that outlines various dishes. In your kitchen, you have different appliances and tools (modules) like a blender, oven, or mixer, each designed for a specific task like blending, baking, or mixing. Your goal is to make a delicious meal (configure your IT environment or system). Each tool has its function, like the oven bakes your cake or the blender makes your sauce, working seamlessly under your direction to create each part of the meal. Just as you don’t need to know how to build an oven to bake a cake, in Ansible, you use these tools (modules) to complete tasks without knowing the underlying complexities.

Ansible had over 3,000 modules. The exact number can vary as new modules are added and old ones are deprecated

##**Why** to use modules ?
Using modules makes automating tasks easy. You don't have to create complicated scripts yourself. Instead, you use Ansible's ready-made modules for usual tasks. This saves time and makes your work more consistent and reliable.

##**How** to use modules ?
**Example 1:** Using the apt module to install nginx
```
- name: Install nginx on a Debian-based system
  hosts: all
  become: true
  tasks:
    - name: Ensure nginx is installed
      apt:
        name: nginx
        state: present

```
**Example 2:** Using the copy module to copy a file to a target system
```
- name: Copy local file to target system
  hosts: all
  tasks:
    - name: Copy sample.txt to /tmp
      copy:
        src: /path/to/local/sample.txt
        dest: /tmp/sample.txt

```

## **Assigments**

1.  **Write a Playbook Using the `user` Module**
    
    Create a playbook that adds a user called `devuser` with a home directory to a Linux system. Use the `user` module.

2.  **Automate Package Updates**
    
    Write a playbook that updates all packages on a system using the appropriate module for the system's package manager (e.g., `apt` for Debian-based systems, `yum` for Red Hat-based systems).

3. **Deploy a Simple HTML Website**    
    
    Use the `copy` module to copy a local HTML file to the web server directory (e.g., `/var/www/html/index.html`) on a target machine where nginx or Apache is installed. Ensure the web server service is running using the `service` module.

## **Interview Questions**
1.  **What is an Ansible module, and how is it used?**

    An Ansible module is a piece of software that Ansible executes on the managed nodes. Each module is designed to handle a specific task and can be invoked directly in playbooks or through other Ansible tools. Modules abstract away the complexities of interacting with different systems, services, and operations.

2.  **How do you choose which module to use for a task?**

    The choice of module depends on the specific task and the target system. Ansible documentation provides a comprehensive list of modules and their purposes, which can guide you in selecting the appropriate module. Factors to consider include the operating system of the target node, the type of resource you're managing (service, file, package, etc.), and the specific operation you want to perform.

3.  **Can you modify or extend existing Ansible modules? How?**

    Yes, Ansible modules can be modified or extended. You can write custom modules in any language that can return JSON (though Python is the most common choice due to its readability and the extensive library support). Custom modules must be placed in a directory recognized by Ansible, such as a `library/` directory next to your playbook.

4.  **Explain the idempotence of Ansible modules and its importance.**

    Idempotence is a property that ensures a module can be run multiple times without changing the system's state after the first run (assuming no changes). It's crucial because it allows Ansible playbooks to be executed safely multiple times, making automation scripts more reliable and predictable. For example, an idempotent module to install a package will only attempt the installation if the package isn't already installed, preventing unnecessary changes to the system.