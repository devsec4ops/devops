Certainly! Here's the Ansible cheat sheet in Markdown format:

```markdown

# Ansible Cheat Sheet

## Basic Concepts

- **Playbook**: YAML files for defining what Ansible does. A playbook maps a group of hosts to some roles.

- **Role**: A predefined way for organizing playbooks and other files in order to facilitate sharing and reusing portions of provisioning.

- **Inventory**: A file that lists all your hosts, typically organized into groups. Ansible uses this to determine which servers to affect with given commands.

- **Module**: A piece of software that Ansible pushes out to manage nodes.

## Key Commands

- **ansible**: Runs a single task on a set of hosts

  ```shell

  ansible [pattern] -m [module] -a "[module options]"

  ```

- **ansible-playbook**: Runs Ansible playbooks

  ```shell

  ansible-playbook [playbook file]

  ```

- **ansible-galaxy**: Downloads roles from an Ansible Galaxy and manages them

  ```shell

  ansible-galaxy install [role]

  ```

- **ansible-vault**: Encrypts Ansible data files

  ```shell

  ansible-vault [create|edit|view|decrypt] [file]

  ```

## Basic Playbook Structure

```yaml

---

- name: Example Ansible Playbook

  hosts: webservers

  vars:

    http_port: 80

    max_clients: 200

  tasks:

    - name: ensure apache is at the latest version

      ansible.builtin.yum:

        name: httpd

        state: latest

    - name: write the apache config file

      template:

        src: /srv/httpd.j2

        dest: /etc/httpd.conf

  handlers:

    - name: restart apache

      ansible.builtin.service:

        name: httpd

        state: restarted

```

## Important Directives

- `hosts`: Specifies which hosts to run the given tasks on.

- `vars`: Defines variables for use in the playbook.

- `tasks`: Lists the tasks to be executed.

- `handlers`: Special tasks that run at the end of a playbook if notified by another task.

## Inventory Example

```ini

[webservers]

web1.example.com

web2.example.com

[dbservers]

db1.example.com

db2.example.com

```

## Tips

- Use roles for organizing complex playbooks.

- Encrypt sensitive data using `ansible-vault`.

- Keep your inventory file updated and well-organized.

- Test your playbooks with `--check` before running them.

```

Feel free to save this cheat sheet for quick reference as you work with Ansible!