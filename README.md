# MiTM-Ettercap / Linux

### Installer ettercap et nmap

`sudo apt install ettercap-graphical`<br>
`sudo apt-get install nmap`


### Vérifier les versions ettercap / namp
`ettercap -v`<br>
`nmap -v`


### Identifier qui est sur le réseau sans-fil, et qui est on est
`sudo nmap -sP [HOST IP/24]`
<br>

## ETTERCAP / ARP POISONING

Pour que l'attaque MiTM fonctionne, il faudra lancer ettercap, et scan la liste de host ip.<br>
Trouver l'ip du routeur et trouver l'ip de la machine à attaquer.<br>
Les ajouter en target, et lancer ARP Poisoning.

![image](https://user-images.githubusercontent.com/97962049/198290353-fe36b25d-71c0-43c3-9826-9493e056bea2.png)


**Test ARP POISONING** <br>
Pour cela, je vais utiliser un test de vulnérabilité de login en http.<br>
http://testphp.vulnweb.com/login.php et http://www.wisemed.cn/demo/index.php/index/login_c.html<br>
<br>
![image](https://user-images.githubusercontent.com/97962049/198310862-af87b0c4-1030-4bae-b243-a440ed826466.png)

Fonctionnel!<br>
Ettercap intercepte les données envoyées au routeur en passant d'abord par ma machine.

`REMARQUE : ettercap ne convertit pas les caractères spéciaux (é = %C3%A9) (no UTF-8 ?)`
<br>
<br>
<br>

## WireShark 


