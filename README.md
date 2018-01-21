Setup local development environment.  Installs Apache, PHP and Node.js.  See main.yml for more details.

```
mkdir centos_dev && cd centos_dev
vagrant init bento/centos-6.8
sed -i '' -e 's/# config.vm.network "private_network", ip: "192.168.33.10"/config.vm.network "private_network", ip: "192.168.33.10"/' Vagrantfile
vagrant up
vagrant ssh
sudo yum -y install git
git clone https://github.com/s-ike/php_nodejs_for_centos6.git
cd php_nodejs_for_centos6
./run.sh
exec $SHELL -l
```





