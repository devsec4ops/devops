#Roles

##**What** is Roles ?
Imagine you're a cook in a big restaurant. When you make a dish, you follow many steps like picking ingredients, preparing them, cooking, and serving. If you had to figure out these steps anew each time, it would be slow and easy to mess up.

That's where "recipes" come in. A recipe tells you what ingredients you need and what steps to follow to make a dish right every time. In Ansible, "roles" are like recipes. They gather everything you need (like variables, files, templates) and what you have to do (like tasks, handlers) to set up a server or start an app. You can share and use these roles again, just like recipes, to make sure your computer tasks are done well and without mistakes, saving time and effort.

##**Why** Roles ?
-   Efficiency: Reuse roles to save time setting up environments.
-   Consistency: Roles ensure tasks are done the same way, reducing mistakes.
-   Simplicity: Break complex playbooks into easier, smaller parts.
-   Shareability: Share roles with others for better collaboration.
-   Scalability: Apply standardized configurations to many servers easily.

##**How** to create Roles ?

###1) Create the Role Structure

First, generate the structure for your role with the `ansible-galaxy`
`ansible-galaxy init nginx_server`
This creates a directory structure under `nginx_server` with folders like `tasks`, `handlers`, `templates`, `files`, `vars`, `defaults`, `meta`, and `tests`.
  
###2) Define the Role Structure

In the `nginx_server/tasks/main.yml` file, you define the tasks that the role will perform:



```
- name: Install nginx
# This task is named "Install nginx" for clarity in playbook output and logs.

  apt:                 # Utilizes the apt module, which is used for managing packages with APT (used by Debian-based systems).
    name: nginx        # Specifies the package to be installed, in this case, nginx.
    state: present     # Ensures the package is installed; 'present' means it will install nginx if it's not already installed.
    update_cache: yes  # Updates the package cache on the target machine before installing, similar to running 'apt-get update'.
    become: yes        # Elevates privileges to become the root user, necessary for installing packages.

- name: Start nginx
# This task is named "Start nginx" and ensures the nginx service is running.

  service:             # Utilizes the service module to manage the service state.
    name: nginx        # Specifies the service to manage, here it is nginx.
    state: started     # Ensures the service is running; 'started' means the service will be started if it isn't already.
    enabled: yes       # Ensures the service is enabled to start at boot.
    become: yes        # Elevates privileges to become the root user, necessary for managing services..

```
###3) Using Your Role in a Playbook
Create a playbook named deploy_nginx.yml that uses your role:
```
# This section targets a group of hosts named "web_servers"

- hosts: web_servers
  become: true          # Elevates privileges to become the root user for all tasks in this playbook.
  roles:
    - nginx_server       # Applies the role named "nginx_server" to all hosts in the "web_servers" group.

```
This setup quickly establishes a reusable, modular approach to deploying nginx across your servers.

## **Commands**

1.  Creating a New Role: (Initializes a new role with a standard directory structure)
    -   `ansible-galaxy init role_name`
  
2.  Listing Installed Roles:
    -   `ansible-galaxy list`
3.  Installing Roles from Ansible Galaxy:
    -   `ansible-galaxy install username.role_name`
4.  Removing Installed Roles:
    -   `ansible-galaxy remove username.role_name`
5.  Specifying Role Dependencies:
    -   Inside your role, in `meta/main.yml`, list dependencies:
    <code><pre> 
        dependencies:
            - { role: another_role }
    </code></pre>
    This ensures `another_role` is executed before the current role.

6.  Overriding Role Defaults:
    -   In your playbook or `vars/main.yml` of your role, specify variables to override defaults:
    <code><pre> 
    vars:
        variable_name: value
    </code></pre>
7.  Running a Playbook with Roles:
    -   `ansible-playbook playbook.yml`

## Interview Questions

1.  **What is an Ansible role and how does it differ from a playbook?**

    An Ansible role is a reusable, standalone block that can be included in Ansible playbooks to automate complex tasks. It differs from a playbook in that a playbook is a list of instructions to execute on remote machines, while a role is a structured way to organize these instructions (including tasks, files, templates, and variables) into a reusable format.

2.  **How do you include a role in an Ansible playbook?**

    You include a role in an Ansible playbook using the `roles:` directive. You can specify the role directly under this directive, and Ansible will execute the tasks defined in the role's `tasks/main.yml` file.

3.  **Can you explain variable precedence in Ansible roles?**

    Variable precedence in Ansible determines which variable value will be used when duplicate variable names are defined in multiple places. In the context of roles, variables defined in playbooks have a higher precedence than those defined in roles. Within roles, variables in `vars/main.yml` have a higher precedence than those in `defaults/main.yml`, allowing default values to be overridden easily.

4.  **How do you manage dependencies between roles in Ansible?**
   
    You manage dependencies between roles in Ansible by defining them in the `meta/main.yml` file of your role. Inside this file, you list the roles that must be applied before the current role using the `dependencies:` section. Ansible resolves these dependencies and applies the roles in the specified order.