Vagrant.configure(2) do |config|
    config.vm.box = "ubuntu/trusty64"

    config.vm.define "gitlab" do |gitlab|
        gitlab.vm.hostname = "gitlab"
        gitlab.vm.provider "virtualbox" do |vb|
            vb.name = "gitlab"
            vb.memory = "2048"
            vb.cpus = 2
        end
        gitlab.vm.network "private_network", ip: "10.0.0.20"
        gitlab.vm.provision "shell", inline: "cat /vagrant/key.pub >> /home/vagrant/.ssh/authorized_keys"
    end
end
