# Comandos-de-Laboratorio-1
Comandos utilizados en las prácticas de Kali Linux SO3.
Prácticas de Kali Linux

Practica 2: Configuración de parametros de red.
ifconfig
ip addr

sudo ifconfig eth0 0.0.0.0
sudo ip address delete [IP]/[máscara] dev eth0

sudo ifconfig eth0 [IP] netmask [máscara]

sudo nano /etc/network/interfaces
sudo systemctl restart networking

sudo nano /etc/resolv.conf

nameserver 8.8.8.8
nameserver 8.8.4.4

Práctica 3: Gestión de usuarios y grupos
sudo adduser Nicol
sudo usermod -aG sudo Nicol
groups Nicol

sudo groupadd guest
sudo adduser invitado
sudo usermod -aG guest invitado
groups invitado

sudo deluser --remove-home invitado
sudo groupdel guest

getent passwd invitado
getent group guest

Práctica 4: Gestión de permisos de archivos

mkdir materia
cd materia
nano estudiante.txt

chmod 700 estudiante.txt
ls -l estudiante.txt

chmod 070 estudiante.txt
ls -l estudiante.txt

cd ..
mkdir materia2
sudo cp materia/estudiante.txt materia2/
ls materia2

rm -r materia
ls
ls materia2
