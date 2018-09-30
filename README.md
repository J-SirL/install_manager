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
This is example is the default package_dev.yml file containing the development servers packages that are ready for installations<br>
```
install_packages:
 - package_name
 - package_name
```
```
| install_packages: | Description |
| -----------------:| -----------:|
| - ansible         |
| - code            |
| - git             |
| - ansible-lint    |

```
A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

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



License
-------

BSD

Author Information
------------------

- Johan Sörell 
