# Introduction
## **What** is Ansible?
Open-source automation tool for IT tasks: configuration management, application deployment, and orchestration.
Simplifies complex tasks and streamlines IT operations.

## **Why** Use Ansible?
- **Simplicity**: Uses YAML for playbook definitions, making it readable and easy to learn.
- **Agentless**: Operates over SSH or PowerShell, no agents to install on target systems.
- **Flexibility**: Manages both Unix-like and Windows systems.
- **Idempotency**: Ensures repeatable deployments and configurations without side effects.

## Ansible **Architecture**:
- **Control Node** : The machine where Ansible is installed and runs playbooks.
- **Managed Nodes** : Targets of Ansible automation (servers, devices).
- **Inventory:** : Defines groups of managed nodes.
- **Modules:** Units of code Ansible executes. Playbooks call modules.
- **Playbooks:** YAML files that define automation jobs. Dictate how to perform tasks.
- **Roles:** Organize playbooks for reusable content.
- **Tasks:** Individual actions performed by playbooks.
- **Facts:** Information retrieved from managed nodes for use in playbooks.
- **Handlers:** Special tasks executed at the end of playbooks if notified by another task.

## Documentation for Full Clarity:
For comprehensive details, refer to the official [Ansible Documentation](https://docs.ansible.com/ansible/latest/getting_started/introduction.html)

