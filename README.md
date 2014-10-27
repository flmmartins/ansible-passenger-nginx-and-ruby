
ansible-passenger-nginx-and-ruby
========

Role that installs, from a tarball, the following softwares using the version of your choosing:

* Ruby
* Ruby Gems
* Passenger

The installation path from those 3 softwares are default

The passenger installation also includes the instalation of the nginx module.

I DO NOT install things with root so change the username inside defaults prior using this.

Requirements
------------

* OS: CentOS 6.5 (didn't test on other versions)

* Change the nginx conf file in templates folder prior running this

* Don't forget to set the variables bellow prior running the role

Role Variables
--------------

Inside defaults:

* Dependencie packages for Ruby

* ruby_version

* rubygems_version

* passenger_version

Outside defaults please define the name of the user where everything will be installed

Dependencies
-------------------------

Install EPEL: https://github.com/flmmartins/ansible-epel

If you wish to disable selinux: https://github.com/flmmartins/ansible-disable-selinux

Example Playbook
-------------------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ruby, user: my-user }


Author Information
------------------

Fernanda Martins (flmmartins@gmail.com)
LinkedIn: https://www.linkedin.com/in/flmmartins
