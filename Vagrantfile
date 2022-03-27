Vagrant.configure("2") do |config|
    config.ssh.insert_key= false

    config.vm.synced_folder "./provisioning", "/vagrant_data"

    config.vm.define "vagrant1" do |vagrant1|
        vagrant1.vm.box = "ubuntu/trusty64"
        vagrant1.vm.network :private_network, ip: "192.168.56.55"
        vagrant1.vm.network "forwarded_port", guest: 80, host: 8080
        vagrant1.vm.network "forwarded_port", guest: 443, host:8443
    end
end