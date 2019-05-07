COUNT = 1

Vagrant.configure(2) do |config|
    config.vm.box = "chavo1/xenial64base"
    config.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    
    end

    1.upto(COUNT) do |n|
      config.vm.define "test0#{n}" do |test|
        test.vm.hostname = "test0#{n}"
        test.vm.network "private_network", ip: "192.168.56.#{50+n}"

      end
    end
  end