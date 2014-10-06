Vagrant.configure("2") do |config|
  config.vm.box       = "ubuntu/trusty64"
  config.vm.box_url   = "https://cloud-images.ubuntu.com/vagrant/trusty/20140927/trusty-server-cloudimg-amd64-vagrant-disk1.box"
  config.vm.network   "forwarded_port", {guest: 80, host: 8080}
  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ruby-webapp.yml"
    ansible.verbose = "v"
  end
end
