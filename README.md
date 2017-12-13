# Ansible Role: Apache Maven 3 [Ansible Playbook Role To Install Maven]

Install Apache Maven 3, a distributed version control system, on any RHEL/CentOS Linux system.

## Requirements

None.

## Role Variables
```yml

#Maven vars
maven_major: 3
maven_version: 3.3.9
maven_home_parent_directory: /opt
maven_env_file: "/etc/profile.d/maven.sh"

```

## Dependencies

This role depends on avinash6784.oracle-java role. This is configured for ansible-galaxy install in requirements.yml.

**NOTE**: Requirements are installed as virtual user avinash6784 (avinash6784.oracle-java).

Be sure to install required roles with
```
ansible-galaxy install --role-file requirements.yml
```

## Usage and Example Playbook

Install from Ansible Galaxy
```
$ ansible-galaxy install avinash6784.maven
```
Or download manually
```
$ git clone https://github.com/avinash6784/ansible-maven.git 
```
The code should reside in the roles directory of ansible ( See ansible documentation for more information on roles ), in a folder maven.

## Run the playbook

First create a playbook including the git role, naming it maven.yml.
```yml
- name: Install maven
  hosts: maven
  become: true
  roles:
    - maven
    
$ ansible-playbook -i hosts maven.yml
```

## Author Informations

This role was created by [Avinash Pawar](http://devopstechie.com).
