Automated Infrastructure with Terraform and Nginx on Google Cloud Platform (GCP)
This project automates the process of setting up infrastructure on Google Cloud Platform (GCP) using Terraform. It includes the configuration of virtual machines (VMs) with Nginx, an automatic scaling system for VMs, health checks, and more.

Table of Contents
Project Description

System Requirements

Installation and Usage

Variable Definitions

Running Terraform

Running the Script and Explanation

Additional Information

Project Description
This project includes the following components:

Nginx Setup: A script that installs Nginx on a virtual machine (VM) running Debian 12 and serves a "Hello World" page.

Google Cloud Provider: Terraform configuration to set up the necessary credentials and settings to deploy resources to Google Cloud.

Managed Instance Group (MIG): Creation of a Managed Instance Group in GCP to manage VMs automatically.

Auto-scaling: Configuration for auto-scaling the number of VMs in the group based on CPU utilization.

Health Check: A health check configuration to monitor the health of the VM instances and ensure they are operating properly.

System Requirements
Terraform: Ensure that Terraform is installed on your machine. You can download it from here.

Google Cloud Account: You need a Google Cloud account to create the necessary resources (VMs, networks, etc.).

Service Account Key: The project requires a Google Cloud service account key in JSON format. This key will be used for authentication during Terraform execution.

Installation and Usage
Clone this repository to your local machine:

bash
Copy
Edit
git clone https://github.com/MiryamMann/miri-mbj-infra.git
cd miri-mbj-infra
Ensure your Google Cloud credentials (service account key) are available. Place the service-account-keys.json file in the project directory.

Initialize the Terraform environment:

bash
Copy
Edit
terraform init
Review the plan that Terraform will apply:

bash
Copy
Edit
terraform plan
Apply the Terraform configuration to provision the infrastructure:

bash
Copy
Edit
terraform apply
Terraform will create the VM instances, health checks, and scaling configurations as specified.

Variable Definitions
Here are the key variables used in the Terraform configurations:

project_id: The ID of your Google Cloud project.

region: The GCP region where resources will be deployed (default is me-west1).

instance_name: The name prefix for the virtual machine instances.

machine_type: The type of machine to use for the VMs (default is e2-micro).

Running the Script and Explanation
The project uses a startup script (startup.sh) to:

Install Nginx on the VM.

Create a directory for the web content at /var/www/html.

Write a simple "Hello World" HTML page to the index.html file.

Restart the Nginx service to apply the changes.

This script is executed when each new VM instance is launched.

Additional Information
This project automates the creation and management of Google Cloud infrastructure using Terraform, which allows for easy scaling and management of VMs in GCP. It is ideal for applications that require high availability and need to handle varying loads with automatic scaling.

Feel free to adjust this further if you want to add any more specific details!








