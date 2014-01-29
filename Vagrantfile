Vagrant.configure("2") do |config|
  config.vm.box = "precise64"
  
  config.vm.network :private_network, ip: "10.168.111.22"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision/setup-devserver.yml"
    ansible.inventory_path = "provision/hosts"
    ansible.host_key_checking = false
  end
end
