Ansible Role : Webapp-apache
=========

Deploy an Apache Web Server with Ansible and Docker.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

```
# defaults file for webapp-apache
system_user: vagrant
container_name: webapp
container_port: 80
apache_port: 80
template_file: index.html.j2
ansible_python_interpreter: /usr/bin/python3

# vars for html page
background_color: blue
contents: "Nice deployment!"

```
Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles : None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: webapp-apache }
