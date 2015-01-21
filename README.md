
Requirements
============

* Vagrant 1.7.x or newer (http://vagrantup.com)
* VirtualBox 
* ChefDK (https://downloads.chef.io/chef-dk/)
* Vagrant Berkshelf plugin (`vagrant plugin install vagrant-berkshelf`)
* Vagrant Omnibus plugin (`vagrant plugin install vagrant-omnibus`)
* Vagrant Hostmanager Plugin (`vagrant plugin install vagrant-hostmanager`)

Recommended
===========

* Vagrant Cachier plugin (`vagrant plugin install vagrant-cachier`)

Installation
============

0. Change ip address or other server configuration of your vagrant box in magento.json

1. Simply start a vagrant box and start a shell session

    ```bash
    vagrant up && vagrant ssh
    ```

2. And proceed with command line installation instruction

    ```bash
    cd [your magento directory]
    php setup/index.php [your params]
    ```
    
3. Modify `app/etc/config.php` and specify session save path:
 
   ```php
   // ....
   'session' => 
     array (
       // ...
       'save_path' => BP . '/var/session'
     )
   // ....
   ```
   
4. Enjoy!