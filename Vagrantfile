# -*- mode: ruby -*-
# vi: set ft=ruby :

targets = [
  "debian/bookworm64",
  "debian/bullseye64",
  "debian/buster64",
  "ubuntu/jammy64",
  "ubuntu/bionic64",
  "ubuntu/focal64"
]

Vagrant.configure("2") do |config|
  targets.each_with_index do |target, index|
    config.vm.define "machine#{index}" do |machine|
      machine.vm.hostname = "machine#{index}"
      machine.vm.box = target
      machine.vm.synced_folder ".", "/vagrant", disabled: true

      if index == targets.count - 1
        machine.vm.provision "ansible" do |ansible|
          ansible.playbook = "playbook.yml"
          ansible.limit = "all"
          ansible.compatibility_mode = "2.0"
          # ansible.verbose = "v"
        end
      end
    end
  end
end
