Vagrant.configure("2") do |config|
  config.vm.box = "docker-0.8.0"
  config.vm.box_url = "https://s3.amazonaws.com/static.orchardup.com/binaries/vagrant/vagrant-docker-0.8.0-virtualbox.box"

  config.ssh.forward_agent = true
  config.vm.network "private_network", :ip => "172.16.42.43"
  config.vm.provision :shell, :path => 'script/provision-vm'

  config.vm.provider :virtualbox do |vb|
    vb.customize ['modifyvm', :id, '--memory', ENV['VM_MEMORY'] || 1024]
    vb.customize ['modifyvm', :id, '--natdnshostresolver1', 'on']
    vb.customize ['modifyvm', :id, '--natdnsproxy1', 'on']
  end

  vagrantfile_extra = "#{ENV['VAGRANT_CWD']}/Vagrantfile_extra.rb"
  eval File.open(vagrantfile_extra).read if File.exists?(vagrantfile_extra)
end
