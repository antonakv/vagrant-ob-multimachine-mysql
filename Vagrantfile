
Vagrant.configure("2") do |config|  
  (1..2).each do |i|
    config.vm.define "web0#{i}" do |web|
      web.vm.box = "aakulov/nginx64"
      web.vm.hostname = "web#{i}"
      web.vm.network "private_network", ip: "192.168.101.#{100+i}"
    end
  end
  
  config.vm.define vm_name="mysql" do |mysql|
    mysql.vm.box = "aakulov/mysql64"
    mysql.vm.hostname = vm_name
    mysql.vm.network "private_network", ip: "192.168.102.101"
  end

end
