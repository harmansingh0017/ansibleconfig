# PhotoApp Deployment with Azure DevOps on CentOS VM

## Overview

This Ansible playbook, combined with Azure DevOps, automates the deployment of a PhotoApp application, consisting of a React app and an API, on a CentOS VM. The playbook, when integrated with Azure DevOps, performs the following tasks:

1. **Create /photoapp directory:**
   - Creates the `/photoapp` directory with specified ownership.

2. **Clone React app repository from GitHub:**
   - Clones the React app repository from [https://github.com/harmansingh0017/photogallery-react-app.git](https://github.com/harmansingh0017/photogallery-react-app.git) into the `/photoapp` directory.

3. **Add EPEL repo:**
   - Adds the EPEL repository to the system.

4. **Install Node.js:**
   - Installs Node.js and npm packages.

5. **Install client side dependencies:**
   - Installs app dependencies for the client side of the application.

6. **Install API side dependencies:**
   - Installs app dependencies for the API side of the application.

7. **Run the API server on port 7000:**
   - Starts the API server on port 7000 asynchronously.

8. **Run the client server on port 3000:**
   - Starts the client server on port 3000 asynchronously.

## Usage with Azure DevOps

1. **Set up Azure DevOps Pipeline:**
   - Configure an Azure DevOps pipeline to execute the Ansible playbook on your CentOS VM.

2. **Clone the Ansible playbook repository:**
   ```bash
   git clone https://github.com/your-repo-url.git
   cd your-repo-directory
   ```

3. **Configure Azure DevOps Pipeline:**
   - Define the pipeline YAML file to run the Ansible playbook.

4. **Run the Azure DevOps Pipeline:**
   - Trigger the Azure DevOps pipeline to execute the deployment.

5. **Access the PhotoApp:**
   - After successful execution, the PhotoApp should be accessible.
   - Client: [http://your-server-ip:3000](http://your-server-ip:3000)
   - API: [http://your-server-ip:7000](http://your-server-ip:7000)

## Notes

- Adjust playbook variables such as repository URL, destination directory, and user ownership according to your environment.
- This playbook assumes a Linux environment with `yum` package manager. Modify package management tasks for other distributions.

Feel free to customize the playbook and readme to fit your specific deployment requirements within the Azure DevOps environment.
