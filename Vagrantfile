Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/jammy64"

  config.vm.define "app" do |app|
    app.vm.hostname = "app-server"

    app.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 2
    end

    app.vm.network "private_network", ip: "192.168.56.10"
  end

  config.vm.define "db" do |db|
    db.vm.hostname = "db-server"

    db.vm.provider "virtualbox" do |vb|
      vb.memory = 768
      vb.cpus = 2
    end

    db.vm.network "private_network", ip: "192.168.56.11"
  end

end