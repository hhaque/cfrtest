# cfrtest
Test files

I created a .box file in Vagrant but it is too large to upload on github.

The playbook.yml, Vagrantfile and the roles folder can be used to Vagrant up the same cfr centos65 box by running:

sudo vagrant box add centos65 https://github.com/2creatives/vagrant-centos/releases/download/v6.5.3/centos65-x86_64-20140116.box
sudo vagrant up
sudo vagrant provision

I used Ansible Galaxy roles and customized them to make the following work:

PHP:  I was able to install version 5.4 using yum.  Tried to install version 5.5 from source, using source install options from geerlingguy.php module, got too many errors.
      I would need more time to make this work for php 5.5
      
Mysql: Installed per requriement, user accounts were created.

Apache: Installed per requirment, vhost configuration require more work.

Varnish:  Set up per requirement. X-Cache HIT or MISS notification set up.

Memcache:  Set up for one port only, need more time to set it up per requirment. Possibly using the below command as ansible task:
          memcached -l 0.0.0.0:11212,, 0.0.0.0:11214
Elastic Search: Installed 
Composer: Installed
Drush: Ansible role that I used threw error during installation, would need more time to make it work.






