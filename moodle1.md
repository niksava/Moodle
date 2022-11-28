# Instal·lar Moodle

Per configurar el meu moodle jo hem fet servir la conexio per ssh a traves de la meva maquina real amb la maquina real de ubuntu.

Pero per instal·lar el moodle hem de instal·lar el apache2 i el php aixo ho podem trobar al seguent link: 

Primer hem de instal·lar el apache2 per instal·lar-ho hem de fer el seguent:

sudo apt-get update

Primer actualitzem els nostres repositoris de la nostra distribusio, per asegurar-nos que estem instal·lant els ultims paquets del programa.

Ja despres hem de procesir a instal·lar el apache2 que es amb la seguent comanda.

sudo apt-get install apache2

Una vegada ho tenim procedim a instal·lar el MySQL o mariadb jo he triat mariadb

# Instal·lació de mariadb

Instal·lem mariadb amb la seguent comanda:

sudo apt-get install mariadb-server

Durant la instal·lació aurem de ficar la contrasenya root.
Quan es aigi acabat fem la seguent comanda aurem de executar mariadb.

sudo mysql_secure_installation

I ara per executar i crear bases de dades ho executarem amb la seguent comanda:

sudo mysql -u root -p

# Instal·lació del PHP

Per instal·lar el PHP hem fer la seguent comanda:

sudo apt install php libapache2-mod-php php-mysql

Una vegada ho tenim tot instal·lat hem de modificar un arxiu per a que el apache ens monstriguin el index.php en lloc de index.html aquesta es la comanda i el directori per modificar el arxiu.

![image](https://user-images.githubusercontent.com/114423315/204345223-b76feb24-533e-4fad-abad-ea59100891f7.png)

A de ser igual com aqui:

![image](https://user-images.githubusercontent.com/114423315/204345370-391d1705-1ce5-4d31-851b-5474bda52ff9.png)

En cas de modificar algo despres ho aurem de guardar amb Ctrl+X o Ctrl+O.

Ja despres reinisiem el apache2, amb la seguent comanda:

sudo service apache2 restart

I comprobem el estat del apache2, amb la seguent comanda.

sudo service apache2 status

![image](https://user-images.githubusercontent.com/114423315/204345865-f50265f0-662a-483c-9ade-69d0c819fd1b.png)

Ara modificarem una arxiu PHP i ficarem el seguent.
sudo nano /var/www/html/index.php

I dins del arxiu introduim el seguent.

![image](https://user-images.githubusercontent.com/114423315/204346603-b4dafc7d-86d4-4c5d-9b8c-901b6045f809.png)

![image](https://user-images.githubusercontent.com/114423315/204346705-67a94d8e-e1e5-4430-a958-690abb0d68e6.png)

I amb aixo ho comprobem les versions de php instal·lat i si en general funciona el php.
I ara com ho hem vist que funciona tot correctament ho de eliminar el fitxer per que aixo ho poden veure tots i aixo pot resultar perillos per a nosaltre per tant, ho eliminem amb la seguent comanda: 

sudo rm  /var/www/html/index.php

![image](https://user-images.githubusercontent.com/114423315/204151549-c9d6de24-019c-4d3e-b0f6-7c3a16946252.png)

Una vegada nos hem conectat a la meva maquina virtual hem de instal·lar el moodle que es fa amb la seguent comanda.

![image](https://user-images.githubusercontent.com/114423315/204151789-b2ba1bd3-92d4-4ef4-8da2-858b8f8cf543.png)

Per avans de desampaquetar aquest arxiu hem de instal·lar el unzip amb la seguent comanda:

![image](https://user-images.githubusercontent.com/114423315/204152706-0503face-c5c6-45dd-964b-2952817361d4.png)

I ara fem la seguent comanda.

![Selecció_004](https://user-images.githubusercontent.com/114423315/204152896-f28f43dd-92ee-4c16-845b-34897141b684.png)

![image](https://user-images.githubusercontent.com/114423315/204153267-c27bbd8c-9a43-4a56-81a9-2adf98bade50.png)

## I ara anem a crear el directori de fitxers.

I ara crarem el moodledata dintre del directori /home:

![image](https://user-images.githubusercontent.com/114423315/204153471-604376ab-edaa-4674-95f4-894fc77e3b3a.png)

Aqui es pujaran tots els fitxer de moodle.

## Configuracio de base de dades.

Pero avans hem de tindre Mariadb instal·lat perque sino ens donara un error. Per tant ho instal·lem de la seguent manera.

![image](https://user-images.githubusercontent.com/114423315/204299886-bd1d61c3-a6c4-49c6-ad7d-a666437109d7.png)

Ja despres fer el seguent:

![image](https://user-images.githubusercontent.com/114423315/204300171-313aefcd-8ead-4eb1-979f-e8903e317cdb.png)
![image](https://user-images.githubusercontent.com/114423315/204300292-7570dd03-36b3-420c-a5d2-296db47da6f8.png)

I ara crearem i configurarem una base de dades amb les seguents comandes.

![image](https://user-images.githubusercontent.com/114423315/204300749-8be810b9-6b4f-4fe6-8cfd-d3a71e45afe5.png)

# Configuració Moodle

I ara anem a configurar el nostre Moodle.

Per poder accedir al moodle ho faig de la seguent manera, pero com que ho he configurat el servidor per ssh he de ficar el seguent al navegador.

![Selecció_010](https://user-images.githubusercontent.com/114423315/204351585-815e161f-cbcb-4e43-8bca-fa954a81f7a8.png)

I sino fique (localhost) en lloc de la IP.
Quan ho tinguesem triem el idiome que volem i fem clic seguent.

Ara ens faltaria instal·lar el php curl que es de la seguent manera.

![image](https://user-images.githubusercontent.com/114423315/204352883-05b8b7bb-441f-428f-b15d-561c91298835.png)

Primera comanda:

sudo apt install php7.3-curl

![Selecció_011](https://user-images.githubusercontent.com/114423315/204352924-6b22213a-49b9-4f58-826a-ed1be3ac0c16.png)

sudo apt install php7.3-zip

![Selecció_012](https://user-images.githubusercontent.com/114423315/204353160-40c823d4-3692-4333-b654-f98171d84795.png)

Fem un restart del apache2:

![image](https://user-images.githubusercontent.com/114423315/204353577-9ce15b3d-0cec-4877-8779-f455d5a64a03.png)

I ara a la seguent finestra hem de ficar el seguent aixo esta baix de tot.

![image](https://user-images.githubusercontent.com/114423315/204354131-ffc48176-bf36-4a4a-913e-78adbf2c550d.png)

Aquest es la carpeta que hem crear avans.

![image](https://user-images.githubusercontent.com/114423315/204354632-10365401-1b73-431f-ba0b-d39ac22beb6e.png)

I ara hem triem aquesta opcio i fem clic seguent.

Una vegada hem arribat a aquesta finestra hem de escriure el usuari i la contrasenya la resta ho deixem tal qual com esta.

![image](https://user-images.githubusercontent.com/114423315/204356310-42ec9210-acc1-4dbc-bdc5-f2c862cf3dd5.png)

Hem de fer la comanda anterior

I ens apareisera la seguent finestra ho aurem de fer seguent.

![image](https://user-images.githubusercontent.com/114423315/204356638-6a10ba01-c0e2-49f7-99e4-90afe4d4ca0c.png)

# Error 

Ara quan ho reiniciessim ens surtira uns error que els solusionarem instalant-les extencións.

![image](https://user-images.githubusercontent.com/114423315/204359680-97d9a701-c24f-4c41-9e17-0a212632458d.png)

![image](https://user-images.githubusercontent.com/114423315/204359930-6e8bb1e1-2a4c-499c-989b-842d27807d91.png)

![image](https://user-images.githubusercontent.com/114423315/204360142-ca93cb93-fcb7-491d-a193-8af3cca429de.png)

![image](https://user-images.githubusercontent.com/114423315/204360299-a025ae1c-9a1b-4969-902c-3581d0a06c7c.png)

![image](https://user-images.githubusercontent.com/114423315/204360424-6c860fa0-0e23-4810-b2f7-7b5b520effed.png)

I quan ho tinguesim les extincion instalades reiniciem el apache2 i fem clic seguent.

sudo service apache2 restart

Ara anem ficar una altra contrasenya i les dades nessesaries.

![image](https://user-images.githubusercontent.com/114423315/204362285-aa500983-f924-4a31-816f-8ba1d9441ad8.png)
