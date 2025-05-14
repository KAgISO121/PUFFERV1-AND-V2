# PUFFERV1-AND-V2

             V2 
                                              puffer panel2

1) apt update
2) apt install sudo
3) apt install systemctl

4) curl -s https://packagecloud.io/install/repositories/pufferpanel/pufferpanel/script.deb.sh?any=true | sudo bash

5) sudo apt update
6) sudo apt-get install pufferpanel
7) sudo pufferpanel user add
8) sudo systemctl enable --now pufferpanel              

again start your panel
      
sudo systemctl enable --now pufferpanel  


             V1 

sudo su
apt update
apt upgrade

$ mkdir -p /var/lib/pufferpanel
$ docker volume create pufferpanel-config
$ docker create --name pufferpanel -p 8080:8080 -p 5657:5657 -v pufferpanel-config:/etc/pufferpanel -v /var/lib/pufferpanel:/var/lib/pufferpanel -v /var/run/docker.sock:/var/run/docker.sock --restart=on-failure pufferpanel/pufferpanel:latest
$ docker start pufferpanel
$ docker exec -it pufferpanel /pufferpanel/pufferpanel user add

again start your panel
      
docker start pufferpanel
