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


- GPARTED
- Comandes
# Còpies de seguretat i automatització de tasques
# Gestió d'usuaris, grups, permisos
# Gestió de procesos
