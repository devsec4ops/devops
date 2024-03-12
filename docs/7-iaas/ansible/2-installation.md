# Installation

1. **Update Ubuntu Package Repository**: 
        Execute `sudo apt update` to refresh your package lists.
2. **Install Software Properties Common**: 
        Run `sudo apt install software-properties-common` to allow for additional repository management.
3. **Add Ansible PPA**: 
        Use `sudo add-apt-repository --yes --update ppa:ansible/ansible` to add the official Ansible Personal Package Archive.
4. **Install Ansible**: 
        Install Ansible by running `sudo apt install ansible`.
5. **Verify Installation**: 
        Check your Ansible installation with `ansible --version`, which displays the installed Ansible version.