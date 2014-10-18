Vagrant.configure("2") do |config|
  config.vm.box       = "trusty64_mri_puma"
  config.vm.box_url   = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"

  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end

  config.vm.network "public_network", ip: "192.168.0.100", bridge: "wlp2s0"
  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ruby-webapp.yml"
    ansible.verbose = "v"
  end
end
