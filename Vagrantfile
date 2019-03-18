Vagrant.configure("2") do |config|
    config.vm.box = "bento/ubuntu-18.04"
    config.vm.define :master do |master_config|
        master_config.vm.network "private_network", ip: "172.30.1.5"
        master_config.vm.provision "ansible" do |ansible|
            ansible.playbook = "./playbooks/kube-dependencies-playbook.yml"
        end
    end
end