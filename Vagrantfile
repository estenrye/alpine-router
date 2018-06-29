Vagrant.configure("2") do |config|
  config.vm.box = "generic/alpine38"
  config.vm.network "public_network", bridge: "Kitchen-NAT" => "eth1", ip: "192.168.200.1" 
  config.vm.network "public_network", bridge: "External_Switch" => "eth0", type: "dhcp"
  
  config.vm.provision "shell", path: "./iptables.sh"
  config.vm.provision "shell", path: "./dnsmasq.sh"
end
