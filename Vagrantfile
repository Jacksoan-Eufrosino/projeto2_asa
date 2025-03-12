Vagrant.configure("2") do |config|
  config.vm.box = "roboxes/ubuntu2204"
  config.vbguest.auto_update = false

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
  end

  config.vm.define "JacksoanEufrosino" do |aluno|
    aluno.vm.hostname = "JacksoanEufrosino"
    aluno.vm.network "private_network", ip: "192.168.57.10"

    aluno.vm.provider "virtualbox" do |vb|
      vb.name = "JacksoanEufrosino"
      vb.memory = 1024
    end

  end
end
