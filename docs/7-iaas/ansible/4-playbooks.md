#**Playbooks**

## **What** is Playbook ?
Ansible Playbooks are like recipe books for setting up computer systems. They list servers (like ingredients) and tasks (like cooking steps) to set up certain IT settings, kind of like making a dish. They're written in YAML, which is simple and easy to read, almost like plain English.

## **Why** Playbook ?
Ansible playbooks are like your computer's to-do list, automating multiple tasks in one go. Rather than doing tasks one by one, you list them in a playbook, and Ansible handles them all, saving time and reducing errors by ensuring consistency.

## **How** to use it ?
This playbook is a set of instructions to install an Apache web server on a group of computers called web_servers. It does three main things:
- Installs Apache using something called the yum module.
- Makes sure Apache starts now and whenever the computer restarts.
- Copies an index.html file to the place on the server where web pages are stored.

<pre>playbooks/setup_web_server.yml<code>
# This is the beginning of an Ansible playbook. Playbooks are files where we tell Ansible what to do.

- name: Setup Apache Web Server  # This is the name of our task list. It helps us remember what this playbook does.
  hosts: web_servers             # This tells Ansible to run the tasks on machines that are labeled as "web_servers".
  become: yes                    # This means that Ansible will use superuser (admin) permissions to run tasks.

  tasks:                         # Here we start listing the tasks we want to do on the web_servers.

  - name: Install Apache         # This is the first task. Its name helps us remember it's for installing Apache.
    yum:                         # This tells Ansible to use the yum package manager, common in certain Linux distributions.
      name: httpd                # This is the name of the package we want to install: httpd (Apache).
      state: present             # This tells Ansible we want the httpd package to be installed (present on the system).

  - name: Start Apache           # This is the second task. We're starting Apache and making sure it runs automatically.
    service:                     # This tells Ansible to use the service management system.
      name: httpd                # This specifies which service we're talking about: httpd (Apache).
      state: started             # This makes sure the Apache service is running.
      enabled: yes               # This makes sure Apache will start automatically whenever the server restarts.

  - name: Deploy Homepage        # This is the third task. We're putting a custom homepage onto the web server.
    copy:                        # This tells Ansible to copy a file from one place to another.
      src: /src/index.html       # This is the source file we want to copy. It's the custom homepage.
      dest: /var/www/html/index.html # This is where we want to copy the file to, the default directory for Apache web pages.

</code></pre>

## **Commands**
-   Run: `ansible-playbook playbook.yml`
    -   Inventory: `-i inventory_file` (Choose which computers to run the tasks on)
    -   Limit hosts: `--limit "host1"` (Pick a specific computer from your list)
    -   Tags: `--tags "tag1"` (Run only parts of your tasks marked with this tag)
    -   Skip tags: `--skip-tags "tagname"` (Ignore tasks marked with this tag)
    -   Syntax check: `--syntax-check` (Check if your list of tasks has any mistakes)
    -   Dry run: `--check` (Test your tasks without making real changes)
    -   Extra vars: `-e "var=value"` (Add extra details or changes just for this run)
    -   Verbose: `-vvv` (Get more detailed information while tasks are running)
    -   Parallel: `-f 10` (Run tasks on up to 10 computers at the same time)

## **Assignments**

1.  **Create a Playbook to Install and Configure a MySQL Database**:

    -   Ensure MySQL is installed.
    -   Configure MySQL to start on boot.
    -   Set a root password (use Ansible Vault for securing the password).
    -   Create a database and a user with privileges to that database.
  
2.  **Write a Playbook for User Management**:

    -   Create a user with sudo privileges.
    -   Set a password for the user (again, use Ansible Vault).
    -   Copy an SSH key to the user's `.ssh/authorized_keys` from a file.
  
3.  **Develop a Playbook to Configure a Firewall**:

    -   Install `firewalld`.
    -   Ensure it starts on boot.
    -   Open port 80 (HTTP) and 443 (HTTPS).
    -   Ensure all other incoming connections are denied by default.

## **Interview Questions**

1.  What is an Ansible playbook and how is it used?
    - A playbook is an Ansible file where you write automation tasks in YAML format. Playbooks can perform a variety of tasks such as configuring server software, deploying applications, and more.
  
2.  How do you secure sensitive data like passwords in Ansible playbooks?
    - Ansible Vault is used to encrypt sensitive data within Ansible playbooks. It allows you to keep sensitive data such as passwords or keys in encrypted files, rather than as plaintext in playbooks or roles.
  
3.  Explain the difference between the `ansible` command and the `ansible-playbook` command.
    - The `ansible` command is used for running single tasks, while `ansible-playbook` is used for running Ansible playbooks that can contain multiple tasks and provide more complex automation sequences.
  
4.  What is idempotence in the context of Ansible, and why is it important?
    - Idempotence refers to the property of certain operations in Ansible to produce the same outcome regardless of how many times they're executed. This is important for reliability and efficiency, ensuring that scripts can be run multiple times without causing unexpected side effects.

