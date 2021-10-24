# Infrastructure as Code

This repository contain the automation files for deploying a K8S clustr on vCenter Environment.

For this infrastructure there is two Configuration Management Tool:

1. **Terraform:** This will be used to deploy and destroy the infrasturce's virtual machines.
2. **Ansible:** This will be used to configure the infrasturce services. That including:

	1. Kubernetes master and worker nodes.

## Terraform:

Terraform files are available at the terraform directory.

- [Supported Terraform Version](#supported-terraform-version)
- [Terraform Role Usage](#terraform-role-usage)

### Supported Terraform Version
This terraform module is tested using the following Terraform version:

```
$ terraform -v
Terraform v0.13.5
```

### Terraform Role Usage:

1. Pull the git repo:

```
$ git clone https://github.com/mohanadelamin/k8s-setup-automation-vsphere.git
```

2. Change directory to terraform

```
$ cd k8s-setup-automation-vsphere/terraform/
```

3. Change the variable files to meet your requirements.
	* `variables.tf`* 


4. Run the Terraform module:

```
$ terraform init
$ terraform plan
$ terraform apply -auto-approve
```                          

## Ansible

Ansible files are available at the terraform directory. 

- [Supported Ansible Version](#supported-ansible-version)
- [Roles](#roles)
- [Ansible Roles Usage](#ansible-roles-usage)

### Supported Ansible Version

This ansible roles are tested using the following Ansible version:

```
$ ansible --version
ansible 2.9.10
  config file = /Users/melamin/.ansible.cfg
  configured module search path = ['/Users/melamin/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/local/lib/python3.7/site-packages/ansible
  executable location = /usr/local/bin/ansible
  python version = 3.7.6 (default, Dec 30 2019, 19:38:28) [Clang 11.0.0 (clang-1100.0.33.16)]
```

### Roles

There is 1 roles that is part of this repository.

1. **k8s-role**


### Ansible Roles Usage

1. Pull the git repo:

```
$ git clone https://github.com/mohanadelamin/k8s-setup-automation-vsphere.git

```

2. Change directory to ansible

```
$ cd k8s-setup-automation-vsphere/ansible/
```

3. Change the variable files to meet your requirements.


4. Run the ansible play-book:

```
$ ansible-playbook playbook.yaml
```