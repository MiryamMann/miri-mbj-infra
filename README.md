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

