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

