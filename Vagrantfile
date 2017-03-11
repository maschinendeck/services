Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/xenial64"

  config.vm.provider "virtualbox" do |vb|
    #   # Display the VirtualBox GUI when booting the machine
    #   vb.gui = true
    #
    #   # Customize the amount of memory on the VM:
    vb.memory = "1524"
  end

  config.vm.provision "ansible" do |p|
    p.playbook = "site.yml"
    # p.sudo = true
    # p.host_key_checking = false
    # p.verbose = true
    # p.verbose = "v"
    # p.extra_vars = {
    #   var1: "value1",
    #   ..
    # }
  end

end
