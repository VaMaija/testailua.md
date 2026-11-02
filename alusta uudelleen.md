Alusta uudella Ubuntulla: 

Asensin virtuaalikoneeksi Debian live 13.7.0-amd64.iso -levykkeeltä Trixien. Se löytyy [täältä](https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/).   

    maija@hallitsija:~$ sudo apt-get update  
    maija@hallitsija:~$ sudo apt-get upgrade
    maija@hallitsija:~$ sudo apt-get install build-essential linux-headers-$(uname -r) dkms -y  //guest additions-lisäys  Googlen tekoäly prompti kysymykseen "miten asennetaan ubuntuun guest additions"  
    maija@hallitsija:~$ sudo mount /dev/cdrom /mnt
    maija@hallitsija:~$ cd /mnt  
    maija@hallitsija:~$ sudo ./VBoxLinuxAdditions.run  
    maija@hallitsija:~$ sudo reboot 
    maija@hallitsija:~$ sudo apt-get install nano micro apache2 python3 ufw ssh  
- nano ja micro ovat tekstieditoreja   
- apache2 on verkkopalvelintyökalu   
- python3 tarvitaan ansiblen seuraksi  

seuraavaksi SSH-käyttöönotto Tero Karvisen ohjeiden mukaan [täältä](https://terokarvinen.com/ssh-public-key-login-without-password/):  
    `maija@hallitsija:~$ sudo systemctl enable --now ssh`  
    `maija@hallitsija:~$ ssh localhost`
    "yes" to fingerprint
    `maija@hallitsija3:~$ w`  
    
    

    








https://terokarvinen.com/2008/05/02/install-apache-web-server-on-ubuntu-4/index.html  



maija@hallitsija:~$ ip addr  
maija    




Lähteet: 
https://terokarvinen.com/2008/05/02/install-apache-web-server-on-ubuntu-4/index.html  
