# Ansible and Infrastructure as Code

- IAC
- Config mgmt
- What is ansible
- Why Ansible

- Installing Ansible
- Creating a multi environment
- Use Ansible to configure 
- File structures and Ansible
- Adohock commands
- Playbooks

### Infrastructure as code

- Reduces repitition 
- Setting up infrastructure as code
- As opposed to clicking/more robust than isolated scripts

### Config mgmt tools

- Tools that put IAC into practice along with orchestration mgmt
- Config tools include: Chef (Ruby), Puppet, Ansible

#### Orchestration tools
These tools aim more to config the networking and deployment at scale
These tools include:
- Ansible
- Terraform (hashicorp)
- Others(?)

### What is Ansible?

- Ansible is a high level language for dealing with powershell vs bash environments. For dealing with different package managers and generally abstracting the most used commands and operations in provisioning so that you become more infrastructure agnostic
- four pillars of devops: flexibility, ease of use, robustness, cost ($/£)
- Ansible is open source (?)
- Built on Python
- Robustness++ due to IAS and configuration mgmt
- Accessible use
- just set up a yaml file for playbooks
- It allows for a multi and hybrid environment mgmt (orchestration)
- Allows us to set up and track several machines:
 - webserver
 - db
 - aws

### Installing ansible

- On windows, get a vm and install it
- On mac, use python.

