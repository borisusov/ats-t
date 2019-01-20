Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "512"]
  end

  # CentOS server.
  config.vm.define "cen" do |cen|
    cen.vm.hostname = "tomcat1"
    cen.vm.box = "centos/7"
    cen.vm.network :private_network, ip: "192.168.60.11"
    cen.vm.provision "shell", inline: "swapoff -a"
  end
 
  # Ubuntu server.
  config.vm.define "ubu" do |ubu|
    ubu.vm.hostname = "loalbalancer"
    ubu.vm.box = "ubuntu/bionic64"
    ubu.vm.network :private_network, ip: "192.168.60.13"
    ubu.vm.provision "shell", inline: "swapoff -a"
  end

end