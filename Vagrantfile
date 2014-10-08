Vagrant.configure("2") do |config|
  config.vm.box       = "ubuntu/trusty64"
  config.vm.box_url   = "https://cloud-images.ubuntu.com/vagrant/trusty/20140927/trusty-server-cloudimg-amd64-vagrant-disk1.box"
  config.vm.network "public_network", ip: "192.168.0.100"
  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ruby-webapp.yml"
    ansible.verbose = "v"
  end
end
