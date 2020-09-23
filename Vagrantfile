Vagrant.configure("2") do |config|

   # Install Plugin to Resize Disk
  required_plugins = %w( vagrant-vbguest vagrant-disksize )
  
  config.vm.box = "ubuntu/bionic64"
  config.disksize.size = "40GB"
  
  # VBoxManage for VM Customizations
  config.vm.provider :virtualbox do |vb|
    # Headless Mode
    vb.gui = true
    vb.name = "udev1"
    # VBoxManage for VM Customizations
    vb.customize [
      "modifyvm", :id,
      "--memory", "4096"
    ]
    vb.customize ['modifyvm', :id, '--clipboard', 'bidirectional']
  end
end
