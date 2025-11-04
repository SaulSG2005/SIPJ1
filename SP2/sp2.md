github---
layout: default
title: "SP2 Gestió de la Informació del Sistema i Administració"
---

# Sistemes de fitxers i particions
# Mida del sector
Un sector es la mida minima fisica que se guarden en un disco, que son 512 bytes.
# Mida del block
Un sector es la mida minima logica que se guarden les dades en un OS, que son 4096 bytes. Esta mida es pot modificar quan es formatem.
<img width="656" height="163" alt="image" src="https://github.com/user-attachments/assets/ce386712-9bef-41e2-b52e-3eb44443acb3" />

---

<img width="655" height="129" alt="image" src="https://github.com/user-attachments/assets/74a0ab07-f3b9-406b-bfc9-d837e258696f" />

---

<img width="659" height="228" alt="image" src="https://github.com/user-attachments/assets/3e5405ab-5ee0-4d95-a410-0549d2cc9dbf" />

# Fragmentació interna

La fragmentacio interna es tot el espai desaprofitat dintre de la particio.

Podem modificar la mida dels blocs per a canviar la mida.

# Fragmentació externa

La fragmentació externa es l'espai lliure en una memòria o sistema d'emmagatzematge que està dividit en petits blocs.

En windows tenim el desfragmentador per a rediur la fragmentacio

En linux se diu que es bo i es treballa tan be que no necesita desfrgmentado, pero tambe en te.

<img width="817" height="462" alt="image" src="https://github.com/user-attachments/assets/74cb2cf9-72e2-4d74-a9ab-20c5058ddb95" />

# Tipus de sistemes de fitxers

Un sistema de fitxers és un component fonamental en informàtica que controla com es emmagatzemen i recuperen les dades en un dispositiu d'emmagatzematge. Aquí tens una explicació més detallada:

- Organització de dades: El sistema de fitxers estructura les dades en fitxers i carpetes, facilitant la seva gestió i accés.
- Interfície entre l'usuari i el sistema operatiu: Actua com un intermediari que permet als usuaris i aplicacions interactuar amb el maquinari d'emmagatzematge.
- Gestió de l'espai: Controla com s'assigna l'espai d'emmagatzematge, incloent la creació, lectura, escriptura i eliminació de fitxers.
- Tipus de sistemes de fitxers: Hi ha diversos tipus, com ara NTFS, FAT32, ext4, entre d'altres, cadascun amb les seves característiques i avantatges.

# Tipus de formateig
El formateig és el procés de preparar un dispositiu d'emmagatzematge per a l'ús, i hi ha diverses maneres de fer-ho. Aquí tens una llista dels principals tipus de formateig:

Nivell Alt:
- Formateig complet: Aquest tipus de formateig esborra totes les dades del dispositiu i verifica si hi ha sectors defectuosos. És ideal quan vols assegurar-te que no quedi cap dada anterior i que el dispositiu estigui en perfectes condicions per a un nou ús.

Nivell Mitjà:
- Formateig ràpid: El formateig ràpid elimina la informació de la taula de fitxers, però no esborra realment les dades del disc. És útil si vols reutilitzar un dispositiu d'emmagatzematge sense necessitat de netejar completament les dades, i és molt més ràpid que el formateig complet.

Nivell Baix:
- Formateig de baixa nivell: Aquest és un procés més antic que es feia per preparar un disc dur per a l'ús, creant pistes i sectors. Actualment, no és necessari per a la majoria dels usuaris, ja que els discs durs moderns vénen preformatats.

# Particions/Volums

Una particio es una divisio del disco a nivell logic, el volum es una capa de apstraccio que es posa per damunt de la particio.

<img width="1052" height="603" alt="image" src="https://github.com/user-attachments/assets/9ddb39cb-91f2-4ce4-a91d-f18831f2942a" />

<img width="732" height="471" alt="image" src="https://github.com/user-attachments/assets/16cfb196-240b-43e5-a602-3f8812bbb928" />

<img width="946" height="473" alt="image" src="https://github.com/user-attachments/assets/cf5c5cec-b99e-4785-9d32-807a52e8fbea" />

<img width="941" height="267" alt="image" src="https://github.com/user-attachments/assets/33e69e9e-6cf0-48d5-8ac6-a5cb41485136" />

<img width="941" height="267" alt="image" src="https://github.com/user-attachments/assets/6369edbb-1f9e-48c7-aee8-3b232515438a" />

<img width="941" height="267" alt="image" src="https://github.com/user-attachments/assets/08b4adfb-8477-48f4-ad4d-2ef82211cac7" />

<img width="756" height="530" alt="image" src="https://github.com/user-attachments/assets/7fa53bb3-c5a6-45de-9306-ec15b5bd3194" />

<img width="817" height="140" alt="image" src="https://github.com/user-attachments/assets/e0b440c6-7120-447a-a99e-e69baf2c3976" />

<img width="819" height="280" alt="image" src="https://github.com/user-attachments/assets/9861318f-ca67-414c-b20d-10301a742098" />

<img width="454" height="85" alt="image" src="https://github.com/user-attachments/assets/334e2f3a-ce41-4d31-a6fc-29e67d3825a4" />

<img width="471" height="88" alt="image" src="https://github.com/user-attachments/assets/3ef01d5d-819d-4cd7-8c53-2502e2c613a8" />

<img width="734" height="483" alt="image" src="https://github.com/user-attachments/assets/94a83c2f-ddef-459f-9cec-691114a97815" />




- GPARTED
- Comandes

# Gestió d'usuaris, grups, permisos

<img width="1718" height="879" alt="image" src="https://github.com/user-attachments/assets/0bfc7abf-43a4-4a45-8ca8-58885e669088" />

<img width="1718" height="879" alt="image" src="https://github.com/user-attachments/assets/23767c59-1e6b-40a3-8382-8d9733999212" />

<img width="1718" height="879" alt="image" src="https://github.com/user-attachments/assets/e3db412e-b5d8-4b25-a1de-9cd31034277c" />

<img width="1718" height="879" alt="image" src="https://github.com/user-attachments/assets/ba0e8b63-c394-4d83-b2af-35357b6d404b" />

<img width="1718" height="879" alt="image" src="https://github.com/user-attachments/assets/7f1390b2-81ad-4116-b9f1-9d7ca6888daa" />

<img width="531" height="208" alt="image" src="https://github.com/user-attachments/assets/3a4136f3-f20c-4046-bad1-af2e9cbe5006" />

<img width="531" height="208" alt="image" src="https://github.com/user-attachments/assets/b51a16cc-4581-4433-9300-518265fce793" />

<img width="559" height="243" alt="image" src="https://github.com/user-attachments/assets/a9a97ea0-6e45-4048-8639-79723ba18685" />

<img width="558" height="465" alt="image" src="https://github.com/user-attachments/assets/c03abb52-8668-4754-92e4-e0504d1b0eb0" />



# Còpies de seguretat i automatització de tasques
# Gestió de procesos
