# simplify-web-container

## Introduction
This project is to install, configure and run a docker container by using ansible playbook in a single run

## Requirement
- System requirement
> 1. Centos 7 or the latest
> 2. Ansible
> 3. Python

## Prerequisite
1. Configure your Ansible host and change the hosts name in YAML file accordingly
2. Make sure the remote user has sudo access
3. Put [index.html](html/index.html) to your server and specify the directory accordingly
  >   src: "/apps/repo/www/html/index.html"

## Execution
1. Run syntax check on YAML file to make sure the syntax is correct
> ansible-playbook configure.yaml --syntax-check
2. Run the YAML file
> ansible-playbook configure.yaml
3. Validate that port 313 is accessible
> curl http://localhost:313/
