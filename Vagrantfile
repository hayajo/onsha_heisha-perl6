# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "boxcutter/centos72"

  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end

  config.vm.provision "shell", inline: <<-SHELL
    # ビルド用ライブラリ、ツールのインストール
    sudo yum -y groupinstall 'Development Tools'
    sudo yum -y install git
    sudo yum -y install perl-autodie

    # rakudobrewのインストール
    su -l vagrant -c "git clone https://github.com/tadzik/rakudobrew ~/.rakudobrew"
    su -l vagrant -c "echo 'export PATH=~/.rakudobrew/bin:$PATH' >> ~/.bash_profile"

    # Rakudo、Pandaのインストール
    su -l vagrant -c "rakudobrew build moar"
    su -l vagrant -c "rakudobrew build panda"

    # Rakudo Starのモジュールのインストール
    su -l vagrant -l -c "panda install Task::Star"
  SHELL
end
