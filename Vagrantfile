VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "rockylinux/9"
  config.vm.boot_timeout = 1200
  config.vm.synced_folder "./", "/vagrant", disabled: true

  # VirtualBox Guest Additions 자동 업데이트 비활성화
  config.vbguest.auto_update = false if Vagrant.has_plugin?("vagrant-vbguest")

  # 디스크 사이즈 설정 (vagrant-disksize 플러그인 필요)
  if Vagrant.has_plugin?("vagrant-disksize")
    config.disksize.size = "50GB"
  end

  # 첫 번째 Rocky Linux VM
  config.vm.define "rocky_vm1" do |rocky_vm1|
    rocky_vm1.vm.hostname = "rocky-vm1"
    rocky_vm1.vm.network "private_network", ip: "192.168.56.20"
    rocky_vm1.vm.provider :virtualbox do |vb|
      vb.memory = 2048
      vb.cpus = 2
    end
  end

  # 두 번째 Rocky Linux VM
  config.vm.define "rocky_vm2" do |rocky_vm2|
    rocky_vm2.vm.hostname = "rocky-vm2"
    rocky_vm2.vm.network "private_network", ip: "192.168.56.21"
    rocky_vm2.vm.provider :virtualbox do |vb|
      vb.memory = 2048
      vb.cpus = 2
    end
  end

  # 세 번째 Rocky Linux VM
  config.vm.define "rocky_vm3" do |rocky_vm3|
    rocky_vm3.vm.hostname = "rocky-vm3"
    rocky_vm3.vm.network "private_network", ip: "192.168.56.22"
    rocky_vm3.vm.provider :virtualbox do |vb|
      vb.memory = 2048
      vb.cpus = 2
    end
  end
end