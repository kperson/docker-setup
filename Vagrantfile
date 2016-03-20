Vagrant.configure(2) do |config|

  config.vm.box = "tallypix/tallyho"
  config.vm.box_url = "https://s3.amazonaws.com/tallyhovirtualbox/tallyho.json"
  config.ssh.password = "vagrant"
  config.ssh.username = "vagrant"

  config.vm.provider :virtualbox do |p|
    p.name = "docker-demo"
    p.memory = 1024
    p.cpus = 1
    p.customize ["modifyvm", :id, "--cpuexecutioncap", "75"]
  end
  config.vm.network :forwarded_port, guest: 22, host: 2233
  config.vm.hostname = "demo.tallyho.net"
  config.vm.network "private_network", ip: "172.16.200.205"

end
