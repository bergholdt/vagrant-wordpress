# Vagrant Wordpress #

This is a [Vagrant][vagrant] setup for playing with Wordpress. Uses
[Chef Solo][chef] recipes for provisioning. The recipes used are can be found 
[here][cookbooks-opscode], they are all attached as git submodules.

## Requirements ##

* [Virtualbox][virtualbox]
* [Vagrant][vagrant]

    $ gem install vagrant

## To get started ##

    $ git clone git://github.com/bergholdt/vagrant-wordpress.git
    $ cd vagrant-wordpress
    $ vagrant up
    $ open http://localhost:8080

You'll need to install Wordpress (i.e. set up an admin user, name the Wordpress 
blog etc.). 

Your Ubuntu/PHP/MySQL box exists as a virtual machine. The website running on 
the virtual machine is pointing back at the wordpress directory on your local 
machine (but ignored by git). 

wp-content from within wordpress directory are mapped and will be keept in version control.

Destroy the virtual machine once you're finished or just whants to try over:

    $ vagrant destroy

[virtualbox]:https://www.virtualbox.org
[vagrant]:http://vagrantup.com
[chef]:http://wiki.opscode.com/display/chef/Chef+Solo
[cookbooks-opscode]:https://github.com/opscode-cookbooks
