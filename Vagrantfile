Vagrant.configure("2") do |config|
  config.vm.box = "generic/alpine38"
  config.vm.network "public_network", bridge: "External_Switch", type: "dhcp"
  config.vm.network "public_network", bridge: "Kitchen-NAT", ip: "192.168.200.1" 
   
  config.vm.provision "shell", path: "./iptables.sh"
  config.vm.provision "shell", path: "./dnsmasq.sh"
end
