github---
layout: default
title: "SP2 Gestió de la Informació del Sistema i Administració"
---

# Sistemes de fitxers i particions

### Mida del sector

Un sector es la mida minima fisica que se guarden en un disco, que son 512 bytes.

### Mida del block

Un sector es la mida minima logica que se guarden les dades en un OS, que son 4096 bytes. Esta mida es pot modificar quan es formatem.

<img width="656" height="163" alt="image" src="https://github.com/user-attachments/assets/ce386712-9bef-41e2-b52e-3eb44443acb3" />

<img width="655" height="129" alt="image" src="https://github.com/user-attachments/assets/74a0ab07-f3b9-406b-bfc9-d837e258696f" />

<img width="659" height="228" alt="image" src="https://github.com/user-attachments/assets/3e5405ab-5ee0-4d95-a410-0549d2cc9dbf" />

### Fragmentació interna

La fragmentacio interna es tot el espai desaprofitat dintre de la particio.

Podem modificar la mida dels blocs per a canviar la mida.

### Fragmentació externa

La fragmentació externa es l'espai lliure en una memòria o sistema d'emmagatzematge que està dividit en petits blocs.

En windows tenim el desfragmentador per a rediur la fragmentacio

En linux se diu que es bo i es treballa tan be que no necesita desfrgmentado, pero tambe en te.

<img width="817" height="462" alt="image" src="https://github.com/user-attachments/assets/74cb2cf9-72e2-4d74-a9ab-20c5058ddb95" />

---

# Tipus de sistemes de fitxers

Un sistema de fitxers és un component fonamental en informàtica que controla com es emmagatzemen i recuperen les dades en un dispositiu d'emmagatzematge. Aquí tens una explicació més detallada:

- Organització de dades: El sistema de fitxers estructura les dades en fitxers i carpetes, facilitant la seva gestió i accés.
- Interfície entre l'usuari i el sistema operatiu: Actua com un intermediari que permet als usuaris i aplicacions interactuar amb el maquinari d'emmagatzematge.
- Gestió de l'espai: Controla com s'assigna l'espai d'emmagatzematge, incloent la creació, lectura, escriptura i eliminació de fitxers.
- Tipus de sistemes de fitxers: Hi ha diversos tipus, com ara NTFS, FAT32, ext4, entre d'altres, cadascun amb les seves característiques i avantatges.

---

# Tipus de formateig

El formateig és el procés de preparar un dispositiu d'emmagatzematge per a l'ús, i hi ha diverses maneres de fer-ho. Aquí tens una llista dels principals tipus de formateig:

### Nivell Alt:

Formateig complet: Aquest tipus de formateig esborra totes les dades del dispositiu i verifica si hi ha sectors defectuosos. És ideal quan vols assegurar-te que no quedi cap dada anterior i que el dispositiu estigui en perfectes condicions per a un nou ús.

### Nivell Mitjà:

Formateig ràpid: El formateig ràpid elimina la informació de la taula de fitxers, però no esborra realment les dades del disc. És útil si vols reutilitzar un dispositiu d'emmagatzematge sense necessitat de netejar completament les dades, i és molt més ràpid que el formateig complet.

### Nivell Baix:

Formateig de baixa nivell: Aquest és un procés més antic que es feia per preparar un disc dur per a l'ús, creant pistes i sectors. Actualment, no és necessari per a la majoria dels usuaris, ja que els discs durs moderns vénen preformatats.

---

# Particions/Volums

Una particio es una divisio del disco a nivell logic, el volum es una capa de apstraccio que es posa per damunt de la particio.

Per a fer les probes començarem per anar al emmagatzematge de la maquina virtual i crearem un nou disk de 10 Gb:

<img width="1052" height="603" alt="image" src="https://github.com/user-attachments/assets/9ddb39cb-91f2-4ce4-a91d-f18831f2942a" />

Dintre de la maquina, revisarem que esta creada:

<img width="732" height="471" alt="image" src="https://github.com/user-attachments/assets/16cfb196-240b-43e5-a602-3f8812bbb928" />

Utilitzarem la companda fdisk /dev/sdc per a crear una nova particio dintre del nou disc i crearem dos particions de 5Gb cadascuna:

<img width="946" height="473" alt="image" src="https://github.com/user-attachments/assets/cf5c5cec-b99e-4785-9d32-807a52e8fbea" />

<img width="941" height="267" alt="image" src="https://github.com/user-attachments/assets/33e69e9e-6cf0-48d5-8ac6-a5cb41485136" />

Revisem que estiguen creades:

<img width="941" height="267" alt="image" src="https://github.com/user-attachments/assets/6369edbb-1f9e-48c7-aee8-3b232515438a" />



### Comandes

Per a fer el formateig per terminal, utilitzarem la comanda mkfs.ext4 -b 2048 /dev/sdc1:

<img width="941" height="267" alt="image" src="https://github.com/user-attachments/assets/08b4adfb-8477-48f4-ad4d-2ef82211cac7" />

### GPARTED

La segona particio sdc2 la fromateigarem amb la interficie grafica del programari GParted i la farem ntfs:

<img width="756" height="530" alt="image" src="https://github.com/user-attachments/assets/7fa53bb3-c5a6-45de-9306-ec15b5bd3194" />

Revisem que amb la comanda anterior el tamany del block de la particio sdc1 estigue creat be, mentres que en la particio sdc2 no sortira res ja que esta formateixat en ntfs:

<img width="817" height="140" alt="image" src="https://github.com/user-attachments/assets/e0b440c6-7120-447a-a99e-e69baf2c3976" />

Ara a la carpeta /mnt crearem una carpeta que li direm Particio1, entrarem i crearem un fitxer que es dira hola, llavors amb la comanda mount -t ext4 /dev/sdc1 /mnt/Particio1 montarem la particio del disco sdc1 de forma temporal a la carpeta de Particio1:

<img width="819" height="280" alt="image" src="https://github.com/user-attachments/assets/9861318f-ca67-414c-b20d-10301a742098" />

Crearem a la particio montada una carpeta que se dira prova:

<img width="454" height="85" alt="image" src="https://github.com/user-attachments/assets/334e2f3a-ce41-4d31-a6fc-29e67d3825a4" />

Per a comprovar que se a guardat be primer sortirem per a que la particio deixe de estar i despres farem un ls a la carpeta:

<img width="471" height="88" alt="image" src="https://github.com/user-attachments/assets/3ef01d5d-819d-4cd7-8c53-2502e2c613a8" />

Si volem que els canvias del mount siguen permanents, anirem al fitxer /etc/fstab i introduirem la linia de codic que es veu en la seguent captura per a dirli on volem que es monte una carpeta al directori que volem:

<img width="734" height="483" alt="image" src="https://github.com/user-attachments/assets/94a83c2f-ddef-459f-9cec-691114a97815" />

---

# Gestió d'usuaris, grups, permisos

El fitxer /etc/passwd és un fitxer de configuració que actua com una base de dades de text pla per a la informació dels comptes d'usuari locals del sistema.

La seva funció principal és emmagatzemar la informació essencial de cada usuari necessària durant l'inici de sessió i per al funcionament general del sistema.

<img width="1718" height="879" alt="image" src="https://github.com/user-attachments/assets/0bfc7abf-43a4-4a45-8ca8-58885e669088" />

El fitxer /etc/group serveix com a base de dades de text pla per a la informació dels grups locals al sistema Ubuntu.

Mentre que /etc/passwd defineix els usuaris individuals, /etc/group defineix els grups i quins usuaris pertanyen a cadascun d'ells.

<img width="1718" height="879" alt="image" src="https://github.com/user-attachments/assets/23767c59-1e6b-40a3-8382-8d9733999212" />

El fitxer /etc/shadow és un fitxer de configuració de seguretat que treballa conjuntament amb /etc/passwd i /etc/group.

La seva funció principal és emmagatzemar de manera segura les contrasenyes xifrades (hàshs) i la informació de caducitat dels comptes d'usuari.

<img width="1718" height="879" alt="image" src="https://github.com/user-attachments/assets/e3db412e-b5d8-4b25-a1de-9cd31034277c" />

El fitxer /etc/gshadow fa lo mateix que la de /etc/shadow, però aplicada als grups en lloc dels usuaris individuals: emmagatzema les contrasenyes xifrades (hàshs) per als grups locals i la informació de l'administració dels grups.

<img width="1718" height="879" alt="image" src="https://github.com/user-attachments/assets/ba0e8b63-c394-4d83-b2af-35357b6d404b" />

Ara farem una prova, començarem per crear un usuari en adduser:

<img width="1718" height="879" alt="image" src="https://github.com/user-attachments/assets/7f1390b2-81ad-4116-b9f1-9d7ca6888daa" />

Ara utilitzarem la comanda cat group, shadow, passwd | grep gina per a revisar la informacio relacionada en l'usuari gina que hem creat anteriorment:

<img width="531" height="208" alt="image" src="https://github.com/user-attachments/assets/3a4136f3-f20c-4046-bad1-af2e9cbe5006" />

Farem un ls, com podrem veure la carpeta del usuari gina esta buida, per a que es creen els fitxers per defecte de un usuari primer tenim que iniciar sessio per primera vegada en aquest usuari, un cop iniciat tornarem a fer un ls i veurem que la carpeta ja no esta buida:

<img width="531" height="208" alt="image" src="https://github.com/user-attachments/assets/b51a16cc-4581-4433-9300-518265fce793" />

Ara crearem un nou usuari que es dira vesper pero en useradd, que es la forma rapida de crear un usuari sense informacio, despres li posarem la contrasenya al usuari amb passwd vesper i despres usermod -s /bin/bash/ vesper per a establir la nova ruta del shell del usuari, per ultim farem un cat passwd | grep vesper per a revisar que tot estigue be:

<img width="559" height="243" alt="image" src="https://github.com/user-attachments/assets/a9a97ea0-6e45-4048-8639-79723ba18685" />

Ara anirem al /home i farem un ls, com podem apreciar no hi ha una carpeta vesper ja que al crearlo amb useradd no es crea, la crearem nosaltres manualment amb mkdir i amb la comanda chown vesper:vesper vesper per a canviar el propietari del directori, ara amb un ls -l podrem veure que el propietari es vesper, pero ara tindrem que fer lo mateix que amb gina, iniciarem sessio per primera vegada amb vesper per a crear els fitxers i directoris:  

<img width="558" height="465" alt="image" src="https://github.com/user-attachments/assets/c03abb52-8668-4754-92e4-e0504d1b0eb0" />

Ara farem una prova pero en comptes de adduser sera amb deluser, crearem un usuari de prova i provarem a eliminarlo amb la comanda deluser, se borrara el usuari pero si fem un ls a home la carpeta del usuari encara existeix:

<img width="705" height="260" alt="image" src="https://github.com/user-attachments/assets/ae2ce597-f5e9-4b72-b4a7-496dfaa1e182" />

Ara amb un altre usuari fem un deluser -r i veiem que a part de borrar el usuari tambe borra el directori home del usuari:

<img width="688" height="113" alt="image" src="https://github.com/user-attachments/assets/e3d69a74-9114-4c35-9ef1-5ae982773b4e" />

Ara farem una altra prova, crearem un usuari amb adduser revisem el fitxer shadow del usuari, a continuacio li apliquem la comanda usermod -L i tornem a revisar el fitxer shadow, si ens fixem be, al començament de tot trobarem un ! que anteriorment no estava aixo lo que indica que el usuari te la contrasenya bloquejada, la comanda usermod -L bloqueja el inici de sessio de un usuari:

<img width="706" height="211" alt="image" src="https://github.com/user-attachments/assets/bc5432ff-6bb5-4911-aa19-50a262dc46dc" />

Per a desbloquejar la contrasenya es usermod -U:

<img width="701" height="104" alt="image" src="https://github.com/user-attachments/assets/7b64521f-1ba6-4705-b08b-bc9546e255fc" />

Ara farem proves pero amb els grups, crearem uns quants usuaris i amb la comanda addgroup crearem el grup proves, a continuacio revisem la paraula proves dintre del fitxer group i veurem que esta creat pero res mes, ara utilitzarem tres metodes per a afeguir un usuari dintre de un grup, adduser usuari1 proves, gpasswd -a usuari2 proves i usermod -a -G proves usuari3, un cop fet tornem a revisar el fitxer group i veurem que ara el grup proves te els 3 usuaris dintre afeguits:

<img width="681" height="442" alt="image" src="https://github.com/user-attachments/assets/4aa42671-73db-4d88-a3c6-4c3c7e571347" />

Per a eliminar un ussuari de un grup farem el mateix de dos formes diferents, deluser usuari3 proves i gpasswd -d usuari2 proves

<img width="594" height="212" alt="image" src="https://github.com/user-attachments/assets/a1cc99b6-70e7-4ef5-ba6e-ae7e064fbaed" />

Ara amb la comanda usermod -g modificarem el nou grup primari de un dels usuaris que hem eliminat del grup, si revisem el group no apareixera com a usuari del group pero si revisem el passwd podem veure que el grup primari es proves:

<img width="594" height="212" alt="image" src="https://github.com/user-attachments/assets/7a0334c2-e491-4de3-a712-b1e6878275f6" />

Ara intentem utilitzar la comanda delgroup en el grup proves, pero ens dira que no el podem eliminar, de primeres pensariem que es perque encara hi ha un usuari dintre del grup, pero no, es per culpa del usuari que hem dit que proves sigue el seu grup primari, doncs canviem una altra vegada el grup primari i ho tornem a intentar, aquesta vegada no ens dira res i s'eliminara:

<img width="594" height="212" alt="image" src="https://github.com/user-attachments/assets/bb42329f-830c-4c4b-af68-dcff671134f4" />

Despres en /etc tambe tenim una serie de fitxers importants per a la customitzacio com per exemple els seguents:

El fitxer /etc/adduser.conf és el fitxer de configuració predeterminat utilitzat pels scripts adduser i deluser a Ubuntu i sistemes basats en Debian.

Aquest fitxer controla el comportament, les opcions per defecte i la política de creació i eliminació d'usuaris i grups al sistema. Si es modifica aquest fitxer, els canvis afectaran totes les futures execucions de les ordres adduser i deluser.

Com podreu veure en la seguent imatge farem una prova modificant el parametre FIRST_UID = 2000:

<img width="1027" height="930" alt="image" src="https://github.com/user-attachments/assets/089d650d-9407-425a-b417-9a1102bcfa20" />

El fitxer /etc/login.defs a Ubuntu és un fitxer de configuració crucial que defineix les polítiques predeterminades i globals per als comptes d'usuari i la seguretat del sistema.

Aquest fitxer és utilitzat per les utilitats de gestió de comptes de nivell inferior, com ara useradd, usermod, i userdel, i defineix valors per defecte que afecten el procés d'inici de sessió i les polítiques de caducitat de contrasenyes.

Com podreu veure en la seguent imatge farem una prova modificant el parametres PASS_MAX_DAYS, PASS_MIN_DAYS, PASS_WARN_AGE:

<img width="1027" height="930" alt="image" src="https://github.com/user-attachments/assets/b16249da-c196-4e27-935a-17b2709cc975" />

El fitxer /etc/default/adduser és un fitxer de configuració relativament senzill i poc freqüent que s'utilitza principalment per sobrescriure (override) algunes de les opcions de configuració definides globalment a /etc/adduser.conf.

Aquest fitxer permet a l'administrador del sistema establir valors per defecte per a les ordres adduser i addgroup sense haver de modificar el fitxer de configuració principal /etc/adduser.conf.

Com podreu veure en la seguent imatge farem una prova modificant el parametre SHELL=/bin/bash:

<img width="1027" height="930" alt="image" src="https://github.com/user-attachments/assets/26bb30d0-9da4-41c7-aa62-47ef4be4e4a4" />

Per a veure si les proves s'han aplicat de forma correcta crearem un nou usuari amb adduser i revisarem els fitxers shadow i passwd, com veurem s'han aplicat be: 

<img width="1010" height="715" alt="image" src="https://github.com/user-attachments/assets/01aa355c-4893-4e00-817c-62da3564a3db" />

Ara provem a creear un usuari amb useradd:

<img width="1008" height="187" alt="image" src="https://github.com/user-attachments/assets/25082115-498b-4b6a-b5b5-4911f8d610fe" />

Ara revisarem els fitxers que hi han dintre del directori /etc/skel, la funció principal d'/etc/skel és garantir que cada nou usuari que es crea tingui un directori personal  ben configurat amb un conjunt bàsic de fitxers i directoris predeterminats.

El contingut d'/etc/skel sol incloure fitxers de configuració essencials per a l'entorn de l'intèrpret d'ordres (shell) i la sessió de l'escriptori. Aquests fitxers són sovint ocults:

- .bashrc: Conté àlies i funcions per a sessions interactives de Bash.
- .profile: Configuració d'inici de sessió que s'executa quan l'usuari inicia sessió.
- .bash_logout: Ordres que s'executen quan l'usuari tanca la sessió.
- Directoris: Poden incloure directoris predeterminats per a l'escriptori com ara Desktop/, Documents/, Downloads/, etc.

<img width="1027" height="930" alt="image" src="https://github.com/user-attachments/assets/17336996-8b42-4aa0-9d52-97c8d14510e6" />

El fitxer .profile és un script de configuració essencial que es troba al directori personal /home/nom_usuari de cada usuari.

La seva funció principal és establir les variables d'entorn i executar ordres que només s'han d'aplicar a sessions d'inici de sessió interactives.

<img width="860" height="589" alt="image" src="https://github.com/user-attachments/assets/6e74b99e-df70-4c55-931e-2193eef0c9c5" />

El fitxer .bashrc és l'script de configuració més important per a l'intèrpret d'ordres Bash. Es troba al directori personal /home/nom_usuari de cada usuari.

La seva funció principal és establir configuracions i personalitzacions per a sessions del shell que no són d'inici de sessió.

En aquest ultim farem una modificacio per a fer una prova, posarem la seguent linia de comanda alias conexio="ls -la", cada cop que en la terminal posessem conexio sera com executar un ls -la
<img width="860" height="589" alt="image" src="https://github.com/user-attachments/assets/fe4b03c1-39f5-40b0-99ff-fad0213bf28b" />

El fitxer .bash_logout és un script de configuració opcional que es troba al directori personal /home/nom_usuari de cada usuari.

La seva funció principal és executar ordres específiques just abans que un usuari tanqui la sessió del shell Bash.

En aquest ultim farem una modificacio per a fer una prova, posarem la seguent linia de comanda rm -r /var/"$USER"/imatges/*, lo que fara aquesta comanda es que eliminara tot el contingut de la carpeta imatges cada cop que es tanca la sessio de cualsevol usuari:

<img width="860" height="589" alt="image" src="https://github.com/user-attachments/assets/c79375d0-ba14-4e0e-97f2-1bb9b0cc14a6" />

Entrarem en la terminal i farem les proves de comprovacio:

<img width="1125" height="710" alt="image" src="https://github.com/user-attachments/assets/cd33976b-6e77-4555-8cc1-d6200e3124a8" />

### Permisos

Ara farem un par de proves de permisos amb 4 nous usuaris, groc, blau, verd, roig:

<img width="701" height="325" alt="image" src="https://github.com/user-attachments/assets/47bae3b7-574d-4549-aad1-acdda648d9a7" />

Crearem una carpeta que es dira compartida:

<img width="701" height="325" alt="image" src="https://github.com/user-attachments/assets/24c0c703-030a-475b-9b54-a4d750e5d368" />

Farem a groc propietari de la carpeta i afeguirem un grup que es dira parchis i amb la comanda chmod 750 -R compartida/ fareem lo seguent:

750: És el codi de permís octal, format per tres dígits:

-- 7 (Usuari Propietari): 4 (lectura) + 2 (escriptura) + 1 (execució) = Permís total (rwx).

-- 5 (Grup Propietari): 4 (lectura) + 0 (escriptura) + 1 (execució) = Només lectura i execució (r-x).

-- 0 (Altres/Everyone Else): 0 (lectura) + 0 (escriptura) + 0 (execució) = Cap permís (---).

-- -R: Recursiu, aplica els permisos al directori i a tot el seu contingut.

<img width="701" height="325" alt="image" src="https://github.com/user-attachments/assets/df42e080-4ecb-4348-8a0f-99c0df64a6a4" />

Farem la prova d'usuari groc i veurem quins permisos te:

<img width="701" height="325" alt="image" src="https://github.com/user-attachments/assets/3593726c-6a45-4e41-b66f-56251b686180" />

Farem la prova d'usuari blau i veurem quins permisos te:

<img width="701" height="325" alt="image" src="https://github.com/user-attachments/assets/8629e212-2eee-463c-a02b-3f3aa48a68ba" />

Farem la prova d'usuari verd i veurem quins permisos te:

<img width="701" height="325" alt="image" src="https://github.com/user-attachments/assets/bbeb2619-d9e0-49d4-b5f9-61c87456ff05" />

Ara farem porves amb la comanda getfacl, aquesta comanda mostra els permisos en un format més granular i revela si s'han aplicat Llistes de Control d'Accés (ACL). Les ACLs permeten donar permisos a usuaris o grups específics que no siguin ni el propietari ni el grup principal.

<img width="701" height="325" alt="image" src="https://github.com/user-attachments/assets/15bdf541-bbd6-449d-a812-2729f29ac1a6" />

Llavors crearem una nova ACL i crearem un usuari que es dira morat i li donarem acces a ña carpeta compartida encara que no estigue dintre del grup:

<img width="698" height="304" alt="image" src="https://github.com/user-attachments/assets/f9a7ce91-8d8f-4e80-bcd9-79d2c628b9bc" />

Farem la prova d'usuari morat i veurem quins permisos te:

<img width="698" height="304" alt="image" src="https://github.com/user-attachments/assets/9e056def-75f8-458c-a9f7-6a27b0ba30ea" />

Ara farem lo mateix amb l'usuari roig pero no li donarem els permisos:

<img width="698" height="304" alt="image" src="https://github.com/user-attachments/assets/fd961d05-15cc-4f77-b96a-616af0755ec9" />

Farem la prova d'usuari roig i veurem quins permisos te:

<img width="698" height="304" alt="image" src="https://github.com/user-attachments/assets/1f1f83a5-0700-4c41-b6f8-508dd4f6f708" />

Amb la comanda setfacl -b eliminem totes les ACL de la carpeta /compartida

<img width="702" height="415" alt="image" src="https://github.com/user-attachments/assets/edcbb445-dd15-49dc-adff-954f24424dda" />

Tornem a canviar al propietari per root i amb la comanda chmod 777 donem aquests permisos a la carpeta /compartida:

-- 7 (Usuari Propietari): Lectura, escriptura, execució (rwx).

-- 7 (Grup Propietari): Lectura, escriptura, execució (rwx).

-- 7 (Altres/Everyone Else): Lectura, escriptura, execució (rwx).

<img width="702" height="415" alt="image" src="https://github.com/user-attachments/assets/8b632876-8323-447c-a3f4-3f34ae1e2c9b" />

Farem la prova d'usuari blau i veurem quins permisos te:

<img width="702" height="415" alt="image" src="https://github.com/user-attachments/assets/39a705a0-8394-4a2d-aea9-acd1395d6eb5" />

Farem lo mateix pero ara amb la comanda chmod 1777, aixo afeguira el Sticky Bi. El Sticky Bit és un permís especial que s'aplica principalment als directoris. Quan s'activa, permet a qualsevol usuari crear fitxers dins d'aquest directori, però només el propietari original del fitxer (o l'usuari root) pot esborrar o canviar el nom d'aquest fitxer.

<img width="675" height="158" alt="image" src="https://github.com/user-attachments/assets/95e6d2fc-bbfb-47db-9dcb-e0ac90da9b91" />

Farem la prova d'usuari verd i veurem quins permisos te:

<img width="703" height="237" alt="image" src="https://github.com/user-attachments/assets/f8f66dc9-65c0-49a6-94e1-921785f8bf3b" />

# Còpies de seguretat i automatització de tasques

## Teoria copies de seguretat

Una còpia de seguretat és una còpia de les dades emmagatzemades en un dispositiu d'emmagatzematge, com ara un disc dur, una unitat USB o un servei de núvol. Aquesta còpia es fa per protegir les dades contra la pèrdua en cas de fallada del dispositiu, error humà, desastre natural o atac de programari maliciós.

Tipus de copies de seguretat:
- Completa:  Aquest tipus de còpia implica copiar tots els fitxers i dades seleccionats alhora. És la còpia de seguretat més completa, ja que inclou tot el que necessites.
- diferencials: Aquestes còpies només copien els fitxers que han canviat des de l'última còpia de seguretat completa. Això significa que la primera còpia de seguretat diferencial copiarà tots els fitxers, però les còpies posteriors només copiaran els canvis des de la còpia completa.
- incrementals: Aquestes còpies només copien els fitxers que han canviat des de l'última còpia de seguretat, ja sigui completa o incremental. Això fa que les còpies incrementals siguin les més ràpides i que ocupin menys espai d'emmagatzematge.

## Teoria comandes backup

### cp

Es una copia simple, no es inteligent i nomes se utilitza en sistemes locals.

### rsync

Es per a sincronitzar carpetes, es pot fer en local i en remot, es pot conectar amb ssh. Es inteligent.

### dd

Es per a clonar particions o discos. No es inteligent.

## practica comandes backup

Primerament afeguirem dos discos de 10 GB a la maquina virtual i els formatejem:

<img width="791" height="455" alt="image" src="https://github.com/user-attachments/assets/8e1be535-82a6-4961-a7dd-8eb6334e3073" />

### cp
Ara farem una proba amb el cp (copia i pegar), amb la comanda "cp -R /home/Saul/Documents/* /var/copies/" farem una copia de tot lo que hi ha a documents i pegarem a la carpeta copies:

<img width="817" height="578" alt="image" src="https://github.com/user-attachments/assets/1f7007cd-680d-4436-8260-90d5aefed60a" />

### rsync
La comanda rsync -av --delete /origen /desti s'utilitza per transferir i sincronitzar arxius de manera molt més eficient que cp, ja que només copia els fitxers que han canviat. Ho podem veure en la seguent prova:

<img width="883" height="549" alt="image" src="https://github.com/user-attachments/assets/abf3248e-4244-4b13-9fd8-c4f06a0a597e" />

### dd
La comanda dd if=/dev/sdd of=/dev/sde1 bs=1M status=progress s'utilitza per realitzar còpies a baix nivell (a nivell de bytes o blocs), essent l'eina estàndard per a la clonació de discos o la creació d'imatges.

<img width="883" height="549" alt="image" src="https://github.com/user-attachments/assets/fcdab8d9-66a6-4392-804d-68bc28e89891" />

## practica programes backup

### Deja-dup

### Duplicity

## Teoria automatitzacio scripts, cron i anacron

Un script es un conjunt d'instruccions o ordres que s'executen en seqüència per dur a terme una tasca específica.

Serveix per a automatitzar tasques, simplificar processos i fer que els ordinadors facin el treball per tu. La seva utilitat depèn del llenguatge de script utilitzat i de la tasca que es vol dur a terme.
El Cron es un servei del sistema operatiu que serveix per a automatitzar tasques per a usuaris en un apartat i hora en concret, si el ordinador s'apaga, la tasca es perd.

El Anacron es un servei del sistema operatiu que serveix per a automatitzar tasques de manteniment p tasques generals, si el ordinador s'apaga, el anacron espera a que es torne a enjagar i l'executa. Anteriorment treballaben per separat, actualment treballen conjuntament.

## Practica automatitzacio
### Cron

En /etc/crontab permet a l'administrador del sistema programar qualsevol comanda per executar-se automàticament en intervals de temps regulars. 

<img width="931" height="469" alt="image" src="https://github.com/user-attachments/assets/938c486b-fc1d-4142-8b2d-48a91d68ddea" />

Aquests són fitxers de text que contenen les regles per a les tasques programades:

-- cron.d: Un directori on les aplicacions poden deixar els seus propis fitxers de crontab individuals, evitant tocar el fitxer mestre /etc/crontab.

-- cron.daily: Tots els scripts dins d'aquest directori s'executen cada dia.

--cron.hourly: Tots els scripts dins d'aquest directori s'executen cada hora.

-- cron.monthly: Tots els scripts dins d'aquest directori s'executen cada mes.

-- cron.weekly: Tots els scripts dins d'aquest directori s'executen cada setmana.

<img width="586" height="218" alt="image" src="https://github.com/user-attachments/assets/a53c716d-db4e-4114-a188-992cf4a9ae60" />

Amb la comanda crontab -e permet a l'usuari actual editar el seu propi fitxer de crontab personal. Les tasques que s'afegeixen aquí només s'executen sota la identitat d'aquest usuari:

<img width="491" height="311" alt="image" src="https://github.com/user-attachments/assets/7c63a95a-d821-4839-85bc-18ed3ca26956" />

Ara crearem un script personalitzat que es dira copies.sh:

<img width="461" height="310" alt="image" src="https://github.com/user-attachments/assets/35bd6956-c3a7-409f-9d65-8684a0792071" />

Al script li direm amb TIMESTAMP que agare la data, i amb tar -cvf lo nom i el directori que volem copiar i despres posem lo directori de desti on se fara aquesta copia:

<img width="716" height="115" alt="image" src="https://github.com/user-attachments/assets/d349a705-0ab8-4bd3-b8cd-fbbdc038e292" />

Per ultim a /etc/crontab li donarem la instruccio de execuccio del script a l'hora designada:

<img width="892" height="475" alt="image" src="https://github.com/user-attachments/assets/00d8c3fc-bdb3-4362-8065-b45357e2f606" />

Comprovacio completa:

<img width="892" height="475" alt="image" src="https://github.com/user-attachments/assets/80e839c6-1f3b-4dc7-bc10-424e4eaefdae" />




### Anacron

El /etc/anacront6ab es el fitxer de configuracio base per a tot el anacron, aqui configurarem el fitxer cron.dialy:

<img width="876" height="274" alt="image" src="https://github.com/user-attachments/assets/fae2c244-4c70-42f4-8c07-4f84907fa125" />

Modificarem el 5 per un 1 per a que tarde nomes 1 minut en començar el dia en executar el script:

<img width="731" height="259" alt="image" src="https://github.com/user-attachments/assets/2423f455-a8b5-4de0-82c0-aee5af262a6f" />

Farem una copia del script anterior en el directori cron.dialy:

<img width="960" height="242" alt="image" src="https://github.com/user-attachments/assets/b4c0e114-b450-4561-8076-6bf8ff73921b" />

Comprovacio de que la copia s'ha creat:

<img width="906" height="405" alt="image" src="https://github.com/user-attachments/assets/229c7ac7-35d7-4cb3-b71c-dfe905c66a93" />
