# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|

  config.vm.box = "hashicorp/precise64"
  config.vm.provision :puppet, :module_path => 'manifests/' do |puppet|
    puppet.manifests_path = "manifests"
    puppet.manifest_file  = "base.pp"
    end
  
  config.vm.forward_port 80, 8888
  config.vm.host_name = 'sugarcrm'
  config.vm.network :hostonly, "192.168.50.4"
  config.vm.share_folder "www", "/var/www/html/", "../bsys-sugar-ws/src/sugar" , :owner => 'www-data', :group => 'www-data'
  #config.vm.share_folder "artifacts", "/tmp/share", "./share"
    
end
