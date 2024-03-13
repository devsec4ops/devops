#Vault

##**What** is Vault ?

Ansible Vault is a feature within Ansible that allows you to encrypt sensitive information, ensuring it can only be accessed by authorized individuals with the decryption key. It helps keep passwords, private keys, and other confidential data secure in your automation tasks.

##**Why** Vault ?

Using Vault, such as Ansible Vault, is crucial because it protects sensitive information from unauthorized access and potential security breaches. By encrypting data like passwords and keys, it ensures that even if someone gains access to your files, they cannot understand or misuse the sensitive data without the encryption key. This is particularly important in automation and DevOps practices, where scripts and code that manage infrastructure often need to use sensitive information but must do so securely to prevent data leaks or security vulnerabilities.

##**How** to use Vault ?

To set up and use Ansible Vault for encrypting sensitive data, follow these concise steps:

1.  Vault is part of ansible , So no need of additional installation.
   
2.  **Create a New Encrypted File**:
     
    -   Use `ansible-vault create secret.yml` to create and encrypt a new file. You'll be prompted to set a password.

3.  **Edit Encrypted Files**:
    
    -   To edit, use `ansible-vault edit secret.yml`, entering the vault password when prompted.
  
4.  **View Encrypted Files**:
    
    -   Use `ansible-vault view secret.yml` to view an encrypted file, again entering the password.
    
5.  **Running Playbooks with Encrypted Content**:

    Use `ansible-playbook --ask-vault-pass myplaybook.yml` to run a playbook that requires a vault password, 

    or `ansible-playbook --vault-password-file /path/to/passwordfile myplaybook.yml` if you're using a password file.

## **Assignments**

1.  **Create and Encrypt a File**: Write a playbook that contains sensitive information. Use Ansible Vault to encrypt this playbook. Ensure the playbook still functions as expected when run with the `ansible-playbook` command and the `--ask-vault-pass` flag.

2.  **Change Vault Password**: Encrypt a file using Ansible Vault. Then, change the password of the vault-encrypted file. Verify that you can access the file with the new password but not with the old one.

3.  **Use Encrypted Variables**: Create a role that uses variables for sensitive data like database passwords. Encrypt these variables with Ansible Vault and write a playbook that uses this role, demonstrating that the role functions correctly with the encrypted variables.

##**Interview Questions**

1.  **What is Ansible Vault and why is it used?**

    -   Ansible Vault is a feature of Ansible that allows users to encrypt sensitive information, making it secure and accessible only to individuals with the password. It's used to keep sensitive data such as passwords and keys secure within Ansible playbooks and roles.
  
2.  **How do you run a playbook that contains vault-encrypted files?**

    -   To run a playbook containing vault-encrypted files, you use the `ansible-playbook` command with the `--ask-vault-pass` flag, which prompts for the vault password, or the `--vault-password-file` flag, where the password is stored in a file.
  
3.  **Can you explain the process of editing an encrypted file with Ansible Vault?**

    -   To edit an encrypted file, you use the `ansible-vault edit` command followed by the file name. This command prompts for the vault password, decrypts the file temporarily, opens it in the default text editor, and re-encrypts it with the same password upon saving and closing the editor.
  
4.  **What is the difference between encrypting an entire file with Ansible Vault and encrypting only certain variables within a file?**

    -   Encrypting an entire file with Ansible Vault makes the whole content of the file unreadable without the vault password. Encrypting only certain variables (using `ansible-vault encrypt_string`) within a file keeps the overall structure and other variables in plaintext, but secures specific sensitive data. This approach allows for a fine-grained encryption strategy, securing sensitive data while keeping the playbook or roles partially readable for easier maintenance and understanding.