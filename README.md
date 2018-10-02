ServerCity | Install manager
=========

Install Manager installs package based on server env type.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

### This role is easily cofigured for every type of usage:
Below is the description of the default variables and how you can change it to work for your enironment:<br>

```
install_packages:
 - package_name
 - package_name
```
This is example is two of the default files. the development and base servers packages that are ready for installations<br>

install_packages: | Default Contents of: default_package_vars/package_dev.yml
----------------- | -------------
ansible         | code 
 git              | ansible-lint

install_packages: | Default Contents of: default_package_vars/package_base.yml
----------------- | -------------
epel-release  | ansible
mc | htop
iptraf-ng | nmap
tcpdump | python-pip
iotop | yum-utils
device-mapper-persistent-data | lvm2
python-devel | python-docker-py
munin-node




Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

Usage Example:
**Setting the deployment variable to a host**
```markdown
Default values that you can use with **depll** variable:
* production
* development
* staging
```

    ansible-playbook -i inventory test.yml -e depll=production -t set_dep -l hostname

**Create a package_file.yml
package_creator.yml -e pkg_ow=redo_Statx
main.yml


License
-------

BSD

Author Information
------------------

- Johan Sörell 
