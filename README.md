# Ansible-SSH

## SSH Setup Script for Multiple Nodes

This script automates the process of setting up SSH keys and establishing SSH connectivity to multiple remote nodes, often used in cluster management.

It performs the following tasks:

1. **Prompt for Username and Password**:  
   It asks the user to input the username and password for the remote nodes, same for each node.

2. **Ensure `.ssh` Directory Exists**:  
   It checks if the `.ssh` directory exists in the local user's home directory. If it doesn't, the script creates it with appropriate permissions.

3. **Generate SSH Keys**:  
   If SSH keys don't already exist, the script generates a new RSA SSH key pair.

4. **Install `sshpass`**:  
   It checks if the `sshpass` utility is installed (which allows password-based SSH operations) and installs it if necessary.

5. **SSH Key Copy and Connectivity Test**:  
   The script loops through a list of remote node IPs or hostnames, copies the SSH public key to each node, and tests SSH connectivity to ensure that the setup was successful.
