Ansible Configuration
This repository contains Ansible playbooks and roles for configuring servers and services.

About
This Ansible configuration was used to deploy a real-time chat application with React to a CentOS 7 target server. The automation and configuration is applied from an Ubuntu control machine using Ansible.

Getting Started
Ensure Ansible is installed on the Ubuntu control node

Update inventory/hosts with the IP address or hostname of the CentOS 7 target

Update the ansible_user variable for the target in inventory/hosts

Ping the target to verify connectivity:

Copy code

ansible web -m ping -i inventory/hosts
Review and update the playbooks/chat_app.yml playbook for deploying the chat application

Run the playbook:

Copy code

ansible-playbook -i inventory/hosts playbooks/chat_app.yml
The chat application should now be deployed and configured on the target!

Playbooks
chat_app.yml

This playbook handles deploying the chat application to the target. It will:

Install base dependencies like Node.js
Copy over the application code
Install application dependencies with npm
Configure and start the React app
