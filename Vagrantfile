vagrant.configure("2") do |config|
 config.vm.box = "hashicorp/bionic64"
 
config.vm.provider "virtualbox" do |v|
v.memory = 2048
v.cpus = 2


 (1..2).each do |i|
   config.vm.define "web#{i}" do |web|
     web.vm.network "private_network", ip: "192.168.50.#{i+10}" 
     #install webserver
     web.vm.provision "shell", inline: "apt-get update ; apt-get install -y nginx"

end
end
end
end
