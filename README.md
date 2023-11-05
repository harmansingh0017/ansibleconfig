# Ansible Configuration

This repository contains Ansible playbooks and roles for configuring servers and services.

## About

This Ansible configuration was designed for deploying a real-time chat application with React on a CentOS 7 target server. The automation and configuration are executed from an Ubuntu control machine using Ansible.

## Getting Started

To get started with this Ansible configuration, follow these steps:

1. **Ensure Ansible is installed on the Ubuntu control node.**

   Make sure you have Ansible installed on the Ubuntu machine that will serve as the control node. You can install Ansible by following the instructions in the [official Ansible documentation](https://docs.ansible.com/ansible/latest/installation_guide/index.html).

2. **Update the Inventory File (inventory/hosts)**

   Edit the `inventory/hosts` file to include the IP address or hostname of the CentOS 7 target server. Make sure to define the connection parameters, such as the SSH user, for the target server in this inventory file.

3. **Ping the Target Server**

   To verify connectivity with the target server, use the following Ansible command:

   ```bash
   ansible web -m ping -i inventory/hosts

4. **Review and Update the Playbook**

   Open the `playbooks/chat_app.yml` playbook file and review its content. This playbook is responsible for deploying the chat application to the target server. Make any necessary modifications to suit your specific application requirements.

5. **Run the Playbook**

   Once you are satisfied with the playbook configuration, execute it using the following command:

   ```bash
   ansible-playbook -i inventory/hosts playbooks/chat_app.yml

This will deploy and configure the chat application on the target CentOS 7 server.

The chat application should now be successfully deployed and configured on the target server.

## Playbooks

### chat_app.yml

This playbook handles the deployment of the chat application to the target server. It performs the following tasks:

1. Installs base dependencies like Node.js
2. Copies the application code to the target server
3. Installs application dependencies using npm
4. Configures and starts the React application



