
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
<img width="649" height="397" alt="1  apache localhost" src="https://github.com/user-attachments/assets/027073a0-305d-43ec-a6a8-6da7fdd41c31" />


- nano ja micro ovat tekstieditoreja   
- apache2 on verkkopalvelintyökalu   
- python3 tarvitaan ansiblen seuraksi  

seuraavaksi SSH-käyttöönotto Tero Karvisen ohjeiden mukaan [täältä](https://terokarvinen.com/ssh-public-key-login-without-password/):  
    `maija@hallitsija:~$ sudo systemctl enable --now ssh`  
    `maija@hallitsija:~$ ssh localhost`
    "yes" to fingerprint  
    `maija@hallitsija3:~$ w`  

<img width="521" height="221" alt="2  sisällä localhostissa ssh-yhteydellä " src="https://github.com/user-attachments/assets/c05fdcfe-e460-499c-8785-05946867c095" />  

    maija@hallitsija3:~$ ssh-keygen  
    maija@hallitsija3:~$ ssh-copy-id localhost
    maija@hallitsija3:~$ sudo cat /home/maija/.ssh/id_ed25519  //yksityinen avain kotihakemistosta
    maija@hallitsija3:~$ sudo cat /home/maija/.ssh/id_ed25519.pub  //Julkinen avain kotihakemistosta  <img width="344" height="307" alt="Näyttökuva 2026-11-03 005236" src="https://github.com/user-attachments/assets/d7bacf43-62b9-4138-bd2c-f8a260c7b9c4" />


[UpCloudista](https://upcloud.com/) vuokrasin pilvipalvelua 3€/kk-hinnalla leikkimiseen ja testailuun. Tein paketin Aatu Niemen mainioilla [ohjeilla](https://github.com/AONCODES/linux-course/blob/main/h4.md)   

<img width="391" height="353" alt="Näyttökuva 2026-11-02 180311" src="https://github.com/user-attachments/assets/a1767e2f-5e7b-47df-9929-d2bbb3d59fab" />  

<img width="431" height="390" alt="Näyttökuva 2026-11-02 180449" src="https://github.com/user-attachments/assets/1d9d1e38-4b53-42fc-aaba-7d7208ea75ce" />  

<img width="436" height="424" alt="Näyttökuva 2026-11-02 180503" src="https://github.com/user-attachments/assets/b7053fa2-3b69-4827-a9ec-fe5e49e6134f" />  

<img width="430" height="392" alt="Näyttökuva 2026-11-02 180526" src="https://github.com/user-attachments/assets/cfae1487-7289-4c49-b830-a306cb0b8412" />  

<img width="434" height="355" alt="Näyttökuva 2026-11-02 180547" src="https://github.com/user-attachments/assets/e9115744-c62e-4b08-a1ce-a02bd752f6bd" />  

<img width="428" height="258" alt="Näyttökuva 2026-11-02 180855" src="https://github.com/user-attachments/assets/a97b8b8a-4a3b-42e4-8b04-b01406975333" />    








    
    
    
    
    

    








https://terokarvinen.com/2008/05/02/install-apache-web-server-on-ubuntu-4/index.html  



maija@hallitsija:~$ ip addr  
maija    




Lähteet: 
https://terokarvinen.com/2008/05/02/install-apache-web-server-on-ubuntu-4/index.html  
