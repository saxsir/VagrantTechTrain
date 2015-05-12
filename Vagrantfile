# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "puppetlabs/centos-6.6-64-puppet"

  config.vm.define :app do |ap|
    ap.vm.hostname = "treasure2015-ap"
    ap.vm.network :private_network, ip: "192.168.56.220"
    ap.vm.provider :virtualbox do |vb|
      vb.name = "treasure2015-ap"
    end
    ap.vm.provision :puppet, :options => '--modulepath="/vagrant/puppet/modules":"/vagrant/puppet/roles"' do |puppet|
       puppet.manifests_path  = ["vm","/vagrant/puppet/manifests"]
       puppet.manifest_file  = "app.pp"
    end
  end

  config.vm.define :ci do |ci|
    ci.vm.hostname = "treasure2015-ci"
    ci.vm.network :private_network, ip: "192.168.56.320"
    ci.vm.provider :virtualbox do |vb|
      vb.name = "treasure2015-ci"
    end
  end
end
