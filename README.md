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
