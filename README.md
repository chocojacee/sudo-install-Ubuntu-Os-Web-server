# sudo-install-Ubuntu-Os-Web-server

Install Apache 2
# sudo apt update
# sudo apt install apache2
# sudo efw enable
# sudo efw app list
# sudo ufw allow 'Apache Full'
# sudo ufw status
# systemctl status apache2
You can also utilize your favorite web browser for the specified verification. To do so, open a web browser and check what the “localhost” web page beholds for you.

Install Ssh
# sudo apt update
# sudo apt install openssh-server openssh-client
# sudo systemctl status ssh
# sudo ufw allow ssh
# sudo ufw status
# sudo ufw enable
You can see that SSH port 22 is opened. If you have the same output as shown in the picture, then the system is ready for remote connections via SSH.

Install dan Setting ip
# ifconfig
# sudo nano /etc/netplan/00-installer-config.yaml
# sudo netplan apply
# sudo netplan –debug apply
# ifconfig

Install Mysql
# sudo apt update
# sudoapt -get install server mysql
# systemctl is-active mysql
# sudo mysql_secure_installation
# sudo mysql
As you can see, the following query will set the root password to “Password123#@!” and the authentication method to “mysql_native_password”.
Reload the grant tables in the MySQL database so that the changes can be applied without restarting the “mysql” service.
> FLUSH PRIVILEGES;
# mysql -u root -p
# systemctl status mysql.service