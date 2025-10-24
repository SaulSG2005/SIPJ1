github---
layout: default
title: "SP1 Avaluació, Instal·lació i Configuració de Xarxes i Sistemes Operatius"
---

# Virtualització i instal·lació del SO Ubuntu

### Virtualització
Per a procedir en la virtualització primer necessitarem saber els requisits que necessitarà l'ISO que instal·larem en la màquina virtual, en el nostre cas instal·larem una ISO Ubuntu 22.04, els requisits seran els següents:
- uns 3 GB de RAM suggerits
- 25 GB de memòria de disc dur suggerida

<img width="900" height="548" alt="image" src="https://github.com/user-attachments/assets/3f140448-be05-43e0-b433-da61de5617be" />

---
### Instal·lació del SO Ubuntu

Quan creéssim una màquina nova, ens sortirà la següent pantalla on li haurem de posar el nom a la màquina i les especificacions de la màquina que instal·larem:
<img width="869" height="604" alt="image" src="https://github.com/user-attachments/assets/146aae09-2064-4437-8f04-abbf0f0bb5e8" />

---

En la següent pantalla necessitarem posar la quantitat de RAM i processadors, posarem la quantitat recomanada tal com hem buscat amb anterioritat, en el cas dels processadors no sabem quina és la recomanada, així que en posarem 4 per a estar segurs. Atenció, la màquina virtual agarra tot això de la nostra màquina física, pot variar depenent del hardware de cada persona:
<img width="869" height="604" alt="image" src="https://github.com/user-attachments/assets/38673e87-1363-4014-b5f6-04fa2aee4dfc" />

---

Per últim, necessitarem posar la quantitat de Disc Dur que tindrà la nostra màquina. Atenció, la màquina virtual agarra tot això de la nostra màquina física, pot variar depenent del hardware de cada persona:
<img width="869" height="604" alt="image" src="https://github.com/user-attachments/assets/27fa97e7-b317-46fc-bc20-d1de6840479e" />

---
Un cop creada la màquina, anirem als settings, emmagatzematge i posarem manualment l'ISO de l'Ubuntu Desktop:
<img width="1051" height="605" alt="image" src="https://github.com/user-attachments/assets/bea14d86-4a0a-4b2c-a552-ca02eca88bb2" />

---
Per a procedir en la instal·lació, començarem per triar l'idioma:
<img width="1279" height="772" alt="Captura de pantalla de 2025-09-26 13-08-53" src="https://github.com/user-attachments/assets/243155af-1623-45fe-893c-bdb45a254b3c" />

---
Després la disposició del teclat:
<img width="1279" height="772" alt="Captura de pantalla de 2025-09-26 13-09-20" src="https://github.com/user-attachments/assets/3bdf70eb-cdb4-4828-90c0-9cfe8c635067" />

---
Li direm que aplique la instal·lació normal:
<img width="1279" height="772" alt="Captura de pantalla de 2025-09-26 13-09-36" src="https://github.com/user-attachments/assets/0ed6f76e-1561-4505-916d-f7579c24f3a5" />

---
A partir de aquí farem la part més important, les particions manuals, li donarem a més opcions:
<img width="1279" height="772" alt="Captura de pantalla de 2025-09-26 13-09-59" src="https://github.com/user-attachments/assets/5572e2b9-758f-4c9e-ab56-63b3eb45b016" />

---
Crearem una nou espai lliure sense assignar:
<img width="1279" height="772" alt="Captura de pantalla de 2025-09-26 13-12-06" src="https://github.com/user-attachments/assets/76be2186-25f5-4bc7-bd41-41a78eecb0c7" />

---
25 GB estaran assignats para la arrel:
<img width="1279" height="772" alt="Captura de pantalla de 2025-09-26 13-11-37" src="https://github.com/user-attachments/assets/91fa2f25-2237-469c-8c8d-0a0f6e42e44e" />

---
13 GB estaran assignats para el home:
<img width="1279" height="772" alt="Captura de pantalla de 2025-09-26 13-13-36" src="https://github.com/user-attachments/assets/53e67221-1c97-4421-9c1a-6320480f1b0d" />

---
2 GB estaran assignats para el swap:
<img width="1279" height="772" alt="Captura de pantalla de 2025-09-26 13-14-37" src="https://github.com/user-attachments/assets/07e5707e-332f-46be-be75-cd65a6ad90fb" />

---
1 GB estara assignat para el EFI:
<img width="1279" height="772" alt="Captura de pantalla de 2025-09-26 13-17-11" src="https://github.com/user-attachments/assets/7da5a0a4-dd45-4192-92fa-dc28d189888a" />

---
Aquestes seran totes les particions:
<img width="1279" height="772" alt="Captura de pantalla de 2025-09-26 13-17-43" src="https://github.com/user-attachments/assets/a845f726-e419-4ccc-9204-9a5dc025aec4" />

---
Un cop les tenim totes, continuarem amb la instal·lació:
<img width="1279" height="772" alt="Captura de pantalla de 2025-09-26 13-25-06" src="https://github.com/user-attachments/assets/5eb166b2-95bd-492f-b874-bb156ffbae3a" />

---
## Llicenciament
Anirem al seguent directori per la terminal i farem un ls, llavors podrem trobar totes aquestes llicencies-:
<img width="861" height="272" alt="image" src="https://github.com/user-attachments/assets/0b13d093-6e86-48db-bfe2-92d280d221f6" />

La llicència específica d'Ubuntu és la GNU General Public License (GPL), que és una de les llicències més reconegudes en el món del programari de codi obert. Aquesta llicència permet als usuaris:

- Modificar el programari.

- Redistribuir còpies del programari original i les seves modificacions.

- Utilitzar el programari de manera lliure, sempre que es respectin les condicions establertes.


A més de la GPL, Ubuntu també utilitza altres llicències per a diferents components del sistema operatiu, com ara:

- GNU Lesser General Public License (LGPL): Permet l'ús de biblioteques no lliures amb programari GPL.

- MIT License: Una llicència permissiva que permet una gran llibertat d'ús.

- Apache License: Permet la modificació i redistribució amb certes condicions.

## Instal·lacions duals i gestors d'arrancada
Per a preparar la instalacio del dual boot, primerament necesitarem anar a la configuracio de la maquina i activar la opcio UEFI:

<img width="1070" height="701" alt="image" src="https://github.com/user-attachments/assets/38004a0d-12fb-43dc-8e4c-ebcf17d180d6" />

---

Despres en emmagatzematge li posarem la ISO del windows 10 enterprise:

<img width="1070" height="701" alt="image" src="https://github.com/user-attachments/assets/3c6beae5-015b-4377-b3f9-f5b7e212e3a8" />

---

Un cop iniciada la maquina ens mostrara la pantalla de instal·lació del windows, continuarem amb la configuracio de la instal·lació fins a arrivar a la seguent pantalla on tindrem que seleccionar la opcio Personalizada:

<img width="1070" height="701" alt="image" src="https://github.com/user-attachments/assets/1592db24-ff7b-4b51-ab03-73593e4b0978" />

---

Crearem un nou disc de espain on li direm que instale el windows alli:

<img width="1029" height="765" alt="image" src="https://github.com/user-attachments/assets/3e260f4d-9bfd-4376-bd4c-68cf57bfb124" />

---

Anirem a les opcions hi comprovarem que s'ha instal·lat de forma correcta hi estan els dos sistemes operatius dintre de la maquina:

<img width="933" height="394" alt="image" src="https://github.com/user-attachments/assets/56c3f568-8efe-4fbf-9655-0a2e8c2a0d3c" />

---

Ara posarem el grub com a disc optic ja que al instal·lar el windows se ens carrega el grub del ubuntu i l'hem de reinstal·lar manualment:

<img width="1065" height="478" alt="image" src="https://github.com/user-attachments/assets/e00e8601-51b2-4001-9862-6267d72cc7e3" />

---

Anirem a la BIOS i li direm que arranque el Grub desde alli:

<img width="1065" height="478" alt="image" src="https://github.com/user-attachments/assets/9a804ad4-6a00-4d46-8356-1bfd48cc8bc5" />

---

Dintre de la interficie del Grub seleccionarem les seguents opcions:
<img width="642" height="621" alt="image" src="https://github.com/user-attachments/assets/fb5af60b-8396-4be9-afd7-d3746377e3af" />

<img width="642" height="621" alt="image" src="https://github.com/user-attachments/assets/0446bd50-d32f-4167-8c8d-59baf7df2e93" />

---

Un cop ho tindrem, haurem de entrar al Ubuntu tambe desde la BIOS i dintre del Ubuntu anirem a la terminal on haurem de posar la seguent comanda per reinstal·lar el Grub

<img width="878" height="611" alt="image" src="https://github.com/user-attachments/assets/7bf36ed8-d728-4a16-8fb7-398825b7e8bb" />

---

Un cop reinstal·lat, anirem i editarem el fitxer /etc/default/grub i posar la linea GRUB_DISABLE_OS_PROBER = false:

<img width="878" height="611" alt="image" src="https://github.com/user-attachments/assets/16f509b3-cb43-404c-8f8f-4250aaebc3fd" />

---

Un cop modificat el fitxer, el tindrem que actualitzar amb la comanda update-grub2:

<img width="878" height="611" alt="image" src="https://github.com/user-attachments/assets/2a559cec-2b02-4f3f-9075-697af7228a1a" />

---

Per ultim tindrem que modificar el ordre de arrancada del sistema i dir-li que el grub estigue el primer:

<img width="878" height="611" alt="image" src="https://github.com/user-attachments/assets/c6613904-1f07-421f-9bf4-abe90177485b" />

---

Per a canviar el ordre es la comanda efibootegr -o 000#(aqui anira el numero que pertany el Grub, despres tindrem que posar la resta):

<img width="878" height="611" alt="image" src="https://github.com/user-attachments/assets/140325d3-7394-4aa8-adfe-bb5fe3e27d13" />

---

Apagarem la maquina i la tornarem a iniciar per a comprovar que arranca de forma correcta:

<img width="1020" height="841" alt="image" src="https://github.com/user-attachments/assets/d0635b20-3bb3-4338-ac23-b5cb397d6ef7" />

## Particions i punts de restauració

###Particions

Per a fer les proves de les particions i punts de restauracio, anirem a la configuracio de la maquina i afeguirem un disc dur nou:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/2ec56a0b-7ac6-4a0c-a290-5bc9133faabb" />

---
Despres utilitzarem la comanda fdisk en la direccio de /dev/sdb/ ja que es el disc dur que hem creat antes per a fer les proves de particio i punts de restauracio:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/369176b0-10d2-49b6-ba9a-9fd4268b839b" />

---
Un cop iniciem fdisk, li direm que cree una particio primaria de 25 GB de tamany:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/97d54fad-73b0-4e3f-bc54-aca4a7ed5f0f" />

---
Comprovem que estigue ven creada:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/41dbb6f6-cfc2-4ef7-9d4c-d5485a6c59d8" />

---
A continuacio utilitzarem la comanda mkfs.ext4 /dev/sdb1 per a dirli que transforme el la particio que hem creat en format ext4:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/bc26a656-1e8c-45fb-ac3c-3f1c8df47824" />

---

###Punts de restauració

Per a fer punts de restauracio utilitzarem una eina que es diu timeshift, la instalem per terminal:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/b83bc87e-5f80-4b39-8f16-0f171545ebbd" />

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/ff8597ef-d8ea-4217-9aff-8a150da04995" />

---

Per a fer la prova crearem en Documents una carpeta i un fitxer de text:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/d5bb1d5b-4345-4245-a1cf-85e7ecdf792e" />

---

Despres iniciarem el programa i començarem per dirli que ens faigue una instantanea RSYNC:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/2671d84d-55af-4771-8e1a-db10a153c1c8" />

---

Despres seleccionarem la ubicacio on s'ubicara la instantanea:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/fbdff803-0c4b-4370-9fd4-4e9f55c6b75a" />

---

I despres el nivell de la instantanea:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/daead9a4-77ae-45b6-b905-6594f74c2432" />

---

Despres seleccionarem els fitxers que voldrem que es conserven dins de la instantanea, en lo nostre cas dels fitxers root:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/87071fe0-e023-4555-9ff0-7c2570513896" />

---

I dintre dels fitxers root excluirem cualsevol cosa menys Documents:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/ce57f801-831e-4ef2-addd-ad579828a3e4" />

---



## Configuració bàsica de la xarxa

Anirem a la configuracio de la maquina y posarem a les opcions de la xarxa Adaptador pont:

<img width="1060" height="596" alt="image" src="https://github.com/user-attachments/assets/73054810-0084-4499-aaca-f051698c9445" />

---

Iniciarem la maquina i a la terminal posarem ip a per a comprovar la nostra IP i en la interficie grafica abirem a red i a les opcions posarem IPv4:

<img width="1682" height="765" alt="image" src="https://github.com/user-attachments/assets/ff747b8a-e0b5-4419-a4ab-b50de41a0d70" />

---

Canviarem a manual i posarem la IP que ens a donat antes la terminal, despres a la mascara de red posarem 255.255.255.0 per a marcar que es /24, i per ultim a la porta de enllaç posarem la 192.168.0.1 que es la IP del router per defecte, tambe podem posar al DNS la 8.8.8.8:

<img width="1682" height="765" alt="image" src="https://github.com/user-attachments/assets/99046524-2a51-40a9-aabc-b0daae49a481" />

---

Un cop guardada la configuracio en la interficie grafica podem fer un ip a per a fer una comprovacio:

<img width="1682" height="765" alt="image" src="https://github.com/user-attachments/assets/b24389eb-844d-4788-b10f-e61c5030f66d" />

---

Despres fem un ping a google, a la IP 8.8.8.8 i tambe a la IP de la profesora o un company:

<img width="1682" height="765" alt="image" src="https://github.com/user-attachments/assets/0f32325a-35cb-446d-bcae-ff976adb3ff7" />

<img width="729" height="481" alt="image" src="https://github.com/user-attachments/assets/4c1236cd-7282-47a0-89b2-e6c79a21d72b" />

---

Ho tornem a deixar en automatic ja que ara ho canviarem amb la terminal:

<img width="796" height="575" alt="image" src="https://github.com/user-attachments/assets/c261f4bc-bcf1-43fa-a4fc-7d3a879e0f44" />

---

Anirem al fitxer /etc/netplan/01-network-manager-all.yaml:

<img width="796" height="575" alt="image" src="https://github.com/user-attachments/assets/ea76acc4-a230-43b4-8545-e42c0aebb086" />

---

Dintre ficarem les seguents linies de configuracio de fitxer, fara lo mateix que em fet anteriorment amb la interficie grafica:

<img width="796" height="575" alt="image" src="https://github.com/user-attachments/assets/9a213b9c-c799-4013-a395-20af17120c03" />

---

Despres un netplan apply per a aplicar la configuracio:

<img width="796" height="575" alt="image" src="https://github.com/user-attachments/assets/8dc9e809-50c7-42ea-af93-a72819415da3" />

---

Farem un ip a per a comprovar que els canvis s'han aplicat:

<img width="796" height="575" alt="image" src="https://github.com/user-attachments/assets/6282b1dd-f1fd-453e-874f-74e323106503" />

---

I per acabar farem les mateixes comprovacions que antes:

<img width="796" height="575" alt="image" src="https://github.com/user-attachments/assets/3023f4cc-f18b-4aee-a73e-e60057cab161" />

## Comandes generals i instal·lació d'aplicacions

###Pinning Packet

Primerament comprovarem les versions de un programa amb la comanda "apt-cache policy nom_paquet", en el nostre cas utilitzarem el Audacity

<img width="788" height="295" alt="image" src="https://github.com/user-attachments/assets/8411f6ae-69d9-475a-bb0c-3645bac1ef08" />


---
Despres anirem a la carpeta /etc/apt/preferences.d/ i aqui crearem un fitxer on dintre posarem el numero de preferencia de la versio del Audacity que volem instal·lar:

<img width="728" height="235" alt="image" src="https://github.com/user-attachments/assets/1a690a0d-2b9f-4c94-81d1-a5f8974e9fa6" />

---
Ara dintre del fitxer posarem la seguent informacio per a modificar la preferencia:

<img width="788" height="295" alt="image" src="https://github.com/user-attachments/assets/2b2324a0-232f-408e-8a93-f1dce3845da8" />

---

Farem un apt update per a actualitzar els paquets i per comprovar si s'ha fet correctament tornarem a repetir la primera comanda:

<img width="788" height="295" alt="image" src="https://github.com/user-attachments/assets/966b1f4f-7864-4e75-9a68-65b19959ceff" />

###Instal·lacio amb apt

###Instal·lacio amb dpkg

<img width="796" height="575" alt="image" src="https://github.com/user-attachments/assets/4f43415f-41bc-4b8c-b336-246aa45452cc" />

---

<img width="772" height="278" alt="image" src="https://github.com/user-attachments/assets/6d225cf2-57c3-42c1-9cd9-4312565951a5" />

---

<img width="830" height="527" alt="image" src="https://github.com/user-attachments/assets/60d7ff6c-cb56-4fe6-8bad-d47c7cf35fa7" />

---

###Instal·lacio amb aptitude

###Instal·lacio amb repositoris



