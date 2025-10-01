# Hitachi VSP One Object Storage YAML scripts
This repository is intended for internal use by the SEA DMS Object Team at Hitachi Vantara. It serves as a centralized location to store development scripts and related work created by the team. Note: This is not an official repository and is not intended for public presentation or formal release.
# Hardware requirements
VSP One Object 3.1
# Software requirements
Red Hat Ansible Core - 2.16, 2.17, 2.18, 2.19

Python - 3.7 or higher with the package "boto3-1.40.38" and "botocore-1.40.38" in the Python library, so that S3 connections can happen

# Supported operating systems
Oracle Enterprise Linux 8.9 or higher
Red Hat Enterprise Linux 8.9 or higher
# Recommended Host configuration
CPU/vCPU - 2
Memory - 4 GB
HardDisk - 30 GB

# Installation
Before using this collection, you need to install "hitachivantara.vspone_object" and "amazon.aws" modules with the Ansible Galaxy command-line tool:

ansible-galaxy collection install hitachivantara.vspone_object

ansible-galaxy collection install amazon.aws

Now clone the repository and use the Ansible YAML files to execute.
