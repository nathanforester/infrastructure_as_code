# Install required plugins
required_plugins = ["vagrant-hostsupdater"]
required_plugins.each do |plugin|
    exec "vagrant plugin install #{plugin}" unless Vagrant.has_plugin? plugin
end

Vagrant.configure("2") do |config|
  config.vm.define "web" do |web|
    web.vm.box = "ubuntu/bionic64"
    web.vm.network :private_network, ip: "192.168.33.10"
    web.vm.hostname = "web"
    web.hostsupdater.aliases = ["web"]
    web.vm.provision "shell", path: "environment/web/provision.sh"
    #web.vm.provision "ansible" do |ansible|
      #ansible.playbook = "playbook.yml"
    #end
  #   web.vm.synced_folder "environment/web_playbook", "/home/vagrant"
  end
  config.vm.define "app" do |app|
    app.vm.box = "ubuntu/bionic64"
    config.ssh.insert_key = false
    app.vm.network :private_network, ip: "192.168.33.11"
    app.vm.hostname = "app"
    app.hostsupdater.aliases = ["app"]
    app.vm.synced_folder "app", "/home/ubuntu/app"

  end

  config.vm.define "db" do |db|
    db.vm.box = "ubuntu/bionic64"
    config.ssh.insert_key = false
    db.vm.network :private_network, ip: "192.168.33.12"
    db.vm.hostname = "db"
    db.hostsupdater.aliases = ["db"]
 end
end
