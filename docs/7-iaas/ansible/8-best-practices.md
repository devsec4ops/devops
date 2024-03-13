#Best Practices 

##Project Structure 
<pre><code>
ansible-project/

├── inventories/

│   ├── production/

│   │   ├── hosts               # Production servers inventory

│   │   └── group_vars/

│   │       └── all.yml         # Variables for all prod servers

│   └── staging/

│       ├── hosts               # Staging servers inventory

│       └── group_vars/

│           └── all.yml         # Variables for all staging servers

├── roles/

│   ├── webserver/

│   │   ├── tasks/

│   │   │   └── main.yml        # Tasks for setting up the web server

│   │   ├── handlers/

│   │   │   └── main.yml        # Handlers for restarting services

│   │   ├── templates/

│   │   │   └── httpd.conf.j2   # Apache config templates

│   │   └── vars/

│   │       └── main.yml        # Variables specific to the webserver role

│   └── firewall/

│       └── ...                 # Similar structure for firewall setup

└── playbooks/

    └── setup_web_server.yml    # Main playbook that applies roles
</pre></code>