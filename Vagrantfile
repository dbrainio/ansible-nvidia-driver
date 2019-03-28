Vagrant.require_version ">= 2.0.0"

Vagrant.configure(2) do |config|

    config.vm.define "xenial" do |xenial|
        xenial.vm.box = "ubuntu/xenial64"
      end
    
      config.vm.define "bionic" do |bionic|
        bionic.vm.box = "ubuntu/bionic64"
      end

  config.ssh.insert_key = false

  config.vm.provision "shell", inline: "apt-get update && apt-get install -y python-pip"

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = true
    ansible.become = true
    ansible.groups = {
      "gpu" => ["xenial", "bionic"]
    }
    ansible.playbook = "tests/test.yml"
    ansible.extra_vars = {
      headless: false
    }

  end
end
