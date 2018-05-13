Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = "1024"
    v.cpus = 2
    v.customize ["modifyvm", :id, "--cpuexecutioncap", "70"]
  end
  config.vm.define "winAD01" do |winAD01|
    winAD01.vm.box = "mwrock/Windows2012R2"
    winAD01.vm.hostname = "winAD01"
    winAD01.vm.network "private_network", ip: "192.168.60.151"
  end
  config.vm.define "oHPCHead" do |oHPCHead|
    hdptest.vm.box = "bentoo/centos-6.7"
    hdptest.vm.hostname = "hdptest"
    hdptest.vm.network "private_network", ip: "192.168.60.162"
  end
end
