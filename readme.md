# Vagrant
---
가상환경을 구성해주는 파일이다.
여기있는 파일을 가지고 만약 실행을 하게 된다면 VirtualBox에 가상환경이 생겨나게 된다.

## Example source code
---
```
config.vm.define "rocky_vm1" do |rocky_vm1|
    rocky_vm1.vm.hostname = "rocky-vm1"
    rocky_vm1.vm.network "private_network", ip: "192.168.56.20"
    rocky_vm1.vm.provider :virtualbox do |vb|
      vb.memory = 2048
      vb.cpus = 2
    end
  end
```

### Vagrantfile 명령어들

```vagrant up [설치 & 시작하고싶은 환경]```

```vagrant destroy [지우고 싶은 환경]```