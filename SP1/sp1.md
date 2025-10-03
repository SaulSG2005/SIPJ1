---
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
Anirem al seguent directori per la terminal i farem un ls:
<img width="861" height="272" alt="image" src="https://github.com/user-attachments/assets/0b13d093-6e86-48db-bfe2-92d280d221f6" />

## Particions i punts de restauració
## Instal·lacions duals i gestors d'arrancada
a
<img width="1070" height="701" alt="image" src="https://github.com/user-attachments/assets/38004a0d-12fb-43dc-8e4c-ebcf17d180d6" />

---

a
<img width="1070" height="701" alt="image" src="https://github.com/user-attachments/assets/3c6beae5-015b-4377-b3f9-f5b7e212e3a8" />

---

a
<img width="1070" height="701" alt="image" src="https://github.com/user-attachments/assets/1592db24-ff7b-4b51-ab03-73593e4b0978" />

---

a
<img width="1029" height="765" alt="image" src="https://github.com/user-attachments/assets/3e260f4d-9bfd-4376-bd4c-68cf57bfb124" />

---

a
<img width="933" height="394" alt="image" src="https://github.com/user-attachments/assets/56c3f568-8efe-4fbf-9655-0a2e8c2a0d3c" />

---

a
<img width="1065" height="478" alt="image" src="https://github.com/user-attachments/assets/e00e8601-51b2-4001-9862-6267d72cc7e3" />

---

a
<img width="1065" height="478" alt="image" src="https://github.com/user-attachments/assets/9a804ad4-6a00-4d46-8356-1bfd48cc8bc5" />

---

a
<img width="642" height="621" alt="image" src="https://github.com/user-attachments/assets/fb5af60b-8396-4be9-afd7-d3746377e3af" />

---

a
<img width="642" height="621" alt="image" src="https://github.com/user-attachments/assets/0446bd50-d32f-4167-8c8d-59baf7df2e93" />

---

a
<img width="878" height="611" alt="image" src="https://github.com/user-attachments/assets/7bf36ed8-d728-4a16-8fb7-398825b7e8bb" />

---

a
<img width="878" height="611" alt="image" src="https://github.com/user-attachments/assets/16f509b3-cb43-404c-8f8f-4250aaebc3fd" />

---

a
<img width="878" height="611" alt="image" src="https://github.com/user-attachments/assets/2a559cec-2b02-4f3f-9075-697af7228a1a" />

---

a
<img width="878" height="611" alt="image" src="https://github.com/user-attachments/assets/c6613904-1f07-421f-9bf4-abe90177485b" />

---

a
<img width="878" height="611" alt="image" src="https://github.com/user-attachments/assets/140325d3-7394-4aa8-adfe-bb5fe3e27d13" />

---

a
<img width="1020" height="841" alt="image" src="https://github.com/user-attachments/assets/d0635b20-3bb3-4338-ac23-b5cb397d6ef7" />


## Configuració bàsica de la xarxa
## Comandes generals i instal·lació d'aplicacions
