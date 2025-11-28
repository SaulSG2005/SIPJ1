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

<img width="594" height="212" alt="image" src="https://github.com/user-attachments/assets/bb42329f-830c-4c4b-af68-dcff671134f4" />

<img width="1027" height="930" alt="image" src="https://github.com/user-attachments/assets/17336996-8b42-4aa0-9d52-97c8d14510e6" />

<img width="1027" height="930" alt="image" src="https://github.com/user-attachments/assets/089d650d-9407-425a-b417-9a1102bcfa20" />

<img width="1027" height="930" alt="image" src="https://github.com/user-attachments/assets/b16249da-c196-4e27-935a-17b2709cc975" />

<img width="1027" height="930" alt="image" src="https://github.com/user-attachments/assets/26bb30d0-9da4-41c7-aa62-47ef4be4e4a4" />

<img width="1010" height="715" alt="image" src="https://github.com/user-attachments/assets/01aa355c-4893-4e00-817c-62da3564a3db" />

<img width="1008" height="187" alt="image" src="https://github.com/user-attachments/assets/25082115-498b-4b6a-b5b5-4911f8d610fe" />

Fer prova personal en adduser i useradd.

<img width="860" height="589" alt="image" src="https://github.com/user-attachments/assets/6e74b99e-df70-4c55-931e-2193eef0c9c5" />

<img width="860" height="589" alt="image" src="https://github.com/user-attachments/assets/fe4b03c1-39f5-40b0-99ff-fad0213bf28b" />

<img width="860" height="589" alt="image" src="https://github.com/user-attachments/assets/c79375d0-ba14-4e0e-97f2-1bb9b0cc14a6" />

<img width="1125" height="710" alt="image" src="https://github.com/user-attachments/assets/cd33976b-6e77-4555-8cc1-d6200e3124a8" />



# Còpies de seguretat i automatització de tasques
# Gestió de procesos
