Vagrant.configure("2") do |config|

  # requires a development version of vagrant (Vagrant 2.2.19.dev)
  
  # enable env plugin with VAGRANT_EXPERIMENTAL="cloud_init,disks"
  config.env.enable

  config.vm.define "focal-server-cloudimg-amd64-vagrant"

  config.vm.box = "focal-server-cloudimg-amd64-vagrant"

  config.vm.box_url = "https://cloud-images.ubuntu.com/focal/current/focal-server-cloudimg-amd64-vagrant.box"

  config.vm.provider "virtualbox" do |v|
    v.name = "cloud-init-ubuntu-test"
  end

  config.vm.cloud_init :user_data, content_type: "text/cloud-config", path: "user-data"

  config.vm.cloud_init :user_data do |cloud_init|
    cloud_init.content_type = "text/cloud-config"
    cloud_init.path = "user-data"
  end

end
