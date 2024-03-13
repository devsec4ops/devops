#Installation

## macOS

1.  Using Homebrew
    - Open a terminal.
    - Install Homebrew by running `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
    - Update Homebrew with `brew update`
    - Install Ansible with `brew install ansible`

## Windows

1.  Using Windows Subsystem for Linux (WSL)
    - Ensure WSL is enabled on your Windows system. You might need to install it through the Windows Features panel or with PowerShell.
    - Install your preferred Linux distribution via the Microsoft Store (e.g., Ubuntu).
    - Launch your Linux distribution from the Start Menu.
    - Update the package manager with `sudo apt update` (for Debian/Ubuntu distributions).
    - Install Ansible with `sudo apt install ansible` (for Debian/Ubuntu distributions).`

## Linux
1.  Debian/Ubuntu
    - Open a terminal.
    - Update the package manager with `sudo apt update`
    - Install Ansible with `sudo apt install ansible`
2.  Red Hat/CentOS
    `- Open a terminal.
    - Install EPEL repository with `sudo yum install epel-release`
    - Update the package manager with `sudo yum update`
    - Install Ansible with `sudo yum install ansible`
3.  Fedora
    - Open a terminal.
    - Install Ansible directly with `sudo dnf install ansible`