я настраивал сеть через netplan мой конфиг был такой 
моя удаленная машина была в одной подсети с хостом
днс был роутер 
настройка сети VB была выставлена -  сетевой мост 

# This file is generated from information provided by the datasource.  Changes
# to it will not persist across an instance reboot.  To disable cloud-init's
# network configuration capabilities, write a file
# /etc/cloud/cloud.cfg.d/99-disable-network-config.cfg with the following:
# network: {config: disabled}
network:
  version: 2
  renderer: networkd  
  ethernets:
    enp0s8:
     dhcp4: no
     addresses: [ 192.168.0.201/24 ]
     routes:
      - to: default
        via: 192.168.0.1
     nameservers:
        addresses: [ 192.168.0.1 ]  
  
