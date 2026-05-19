# Exercici 1. Monitorització bàsica de

## 1. Obrir el Monitor de recursos

Al servidor, obre:

Administrador de tasques → Rendiment → Obre el Monitor de recursos

<img width="1024" height="728" alt="image" src="https://github.com/user-attachments/assets/4dcea1cd-8a5f-4b6c-b229-04889c68a303" />

## 2. Revisar l’ús de CPU

Comprova:

● processos que consumeixen més CPU

● percentatge total d’ús

<img width="788" height="329" alt="image" src="https://github.com/user-attachments/assets/1fbebbbd-f011-44be-9fdd-326938c2c1c0" />

## 3. Revisar la memòria RAM

Accedeix a la pestanya “Memòria”.

Comprova:

● memòria utilitzada

● memòria lliure

<img width="784" height="200" alt="image" src="https://github.com/user-attachments/assets/352f5a87-2391-4a09-96a8-b531e7e8b457" />

## 4. Revisar el disc

Accedeix a “Disc”.

Comprova:

● processos amb més lectura/escriptura

● activitat del disc

<img width="784" height="450" alt="image" src="https://github.com/user-attachments/assets/e684635a-48be-4da4-a120-e464d2c540e2" />

## 5. Revisar la xarxa

Accedeix a “Xarxa”.

Comprova:

● programes que utilitzen la xarxa

● velocitat d’enviament i recepció

<img width="784" height="450" alt="image" src="https://github.com/user-attachments/assets/89371f86-b386-4eef-8b84-3361b3993fa0" />

## 6. Revisar els esdeveniments del sistema

Obre:

Administrador del servidor → Eines → Visor d’esdeveniments

Consulta:

● Errors del sistema

● Advertiments

● Errors d’aplicació

<img width="833" height="529" alt="image" src="https://github.com/user-attachments/assets/b7ac3315-7996-43ea-abf3-431ae6653dcc" />

# Exercici 2. Connexió remota a Windows
Server
Objectiu
Configurar i utilitzar l’Escriptori remot per connectar-se a un Windows Server des d’un altre
equip.

Part 1. Configuració del servidor

1. Obrir la configuració d’Escriptori remot

Al servidor:

Inici → Configuració → Sistema → Escriptori remot

2. Activar l’Escriptori remot

Activa:

Habilitar Escriptori remot

Prem: Confirmar

3. Permetre usuaris remots

A la mateixa finestra, prem:

Selecciona els usuaris que poden accedir remotament

Prem:

Afegir

Escriu el nom de l’usuari que podrà connectar-se.

Prem:

Comprova els noms

Si l’usuari existeix correctament, prem:

Acceptar

4. Comprovar el nom del servidor

Obre el símbol del sistema:

hostname

Anota el nom del servidor.

5. Comprovar la direcció IP del servidor

Al símbol del sistema executa:

ipconfig

Busca:

Adreça IPv4

Anota la direcció IP.

6. Comprovar el Firewall

Obre:

Panell de control → Sistema i seguretat → Firewall de Windows Defender

Prem:

Permetre una aplicació o característica a través del Firewall

Comprova que:

Escriptori remot

està permès.

Part 2. Connexió des del client

7. Obrir Connexió a Escriptori remot

Al client:

Win + R

Escriu:

mstsc

Prem Enter.

8. Escriure el nom o la IP del servidor

Introdueix:

● el nom del servidor

o

● la direcció IP del servidor

Prem:

Connecta

9. Introduir les credencials

Escriu:

● nom d’usuari

● contrasenya

Prem:

Acceptar

10. Acceptar l’avís de connexió

Si apareix un avís de seguretat:

● marca l’opció per no tornar a mostrar-lo

● prem “Sí”

11. Verificar la connexió

Comprova que:

● apareix l’escriptori del servidor

● pots obrir carpetes

● pots obrir l’Administrador del servidor

Fes una captura de pantalla.

Part 3. Tancar la sessió

12. Tancar la connexió remota

Al servidor remot:

Inici → Tanca sessió

No apagar el servidor.

# Exercici 3. Consulta de llicències de Windows Server i equips units al domini

Una empresa disposa de:

● 1 servidor Windows Server

● 25 ordinadors

● 10 portàtils

● 32 usuaris

● tots els equips units al domini

L’empresa necessita calcular el cost aproximat de les llicències necessàries per al servidor i
per als equips o usuaris que accedeixen al domini.

## Tasques

1. Busca el preu aproximat de:

○ Windows Server Standard

○ Windows Server Datacenter

○ User CAL

○ Device CAL

Els preus indicats són aproximats (MSRP oficial de Microsoft per a la versió de 16 Cores o llicències individuals), expressats en euros segons el canvi de mercat actual.

Windows Server Standard (base de 16 cores): ~1.100 € - 1.180 €

Windows Server Datacenter (base de 16 cores): ~6.200 € - 6.700 €

User CAL (Client Access License): ~40 € - 55 € (per usuari)

Device CAL (Client Access License): ~38 € - 45 € (per dispositiu)

2. Explica:

○ què és una CAL

○ diferència entre User CAL i Device CAL

Una CAL (Client Access License) no és un programari, sinó una llicència legal que atorga a un usuari o a un dispositiu el dret legítim d'accedir i utilitzar els serveis que ofereix un servidor amb Windows Server (com ara l'Active Directory, compartir fitxers, impressions, DNS, etc.). El servidor requereix la seva llicència de sistema operatiu, i els clients requereixen les seves corresponents CALs per connectar-s'hi.

La diferència fonamental entre una User CAL i una Device CAL es basa en què és el que estàs llicenciant per donar-li permís d'accés al servidor: si a una persona o a un aparell.

-- User CAL (Per Usuari): Aquesta llicència es vincula directament a una persona concreta (un usuari de la xarxa). Aquell empleat rep un nom d'usuari i contrasenya i, a partir d'aquí, té dret a connectar-se al servidor des de qualsevol lloc i des de qualsevol dispositiu que vulgui. És la millor opció si un treballador fa servir, per exemple, el seu ordinador d'escriptori, el portàtil de l'empresa, la tauleta i el telèfon mòbil per consultar el correu o accedir als fitxers del servidor. Amb una sola llicència d'usuari ho té tot cobert.

-- Device CAL (Per Dispositiu): Aquesta llicència es vincula a un aparell físic concret (un ordinador, un terminal de punt de venda, una PDA de magatzem, etc.), independentment de qui el faci servir. Qualsevol persona de l'empresa pot asseure's en aquell ordinador i connectar-se al servidor legalment. És l'opció ideal per a llocs on es treballa per torns (com ara una fàbrica, una recepció d'hotel o un servei d'atenció al client), on un mateix ordinador és compartit per diversos empleats al llarg del dia. D'aquesta manera, només pagues per la màquina i no per cada treballador.

3. Calcula:

○ cost aproximat amb User CAL

○ cost aproximat amb Device CAL

-- Escenari A: Cost aproximat amb User CAL (50 Usuaris)Llicència Windows Server Standard: 1.150 €User CALs: 50 usuaris $\times$ 45 € = 2.250 €Cost Total Aproximat: 3.400 €

-- Escenari B: Cost aproximat amb Device CAL (30 Dispositius)Llicència Windows Server Standard: 1.150 €Device CALs: 30 dispositius $\times$ 40 € = 1.200 €Cost Total Aproximat: 2.350 €

4. Indica quin model és més adequat per a aquesta empresa i justifica la resposta.

Criteri de decisió: El model ideal depèn estrictament de la ràtio Usuaris vs. Dispositius.

-- Opció A: Tria User CAL si l'empresa té un model d'oficina modular o teletreball, on cada empleat té un portàtil, un mòbil de l'empresa i un PC d'escriptori (més usuaris que dispositius). Justificació: Surt més a compte llicenciar la persona que no pas els 3 aparells que utilitza.

-- Opció B: Tria Device CAL si l'empresa funciona amb torns de treball (per exemple, una fàbrica, un call center o un hospital) on 30 empleats utilitzen un total de només 10 ordinadors en diferents horaris. Justificació: Estalvies gairebé un 60% en llicències ja que només pagues pels equips físics sense importar qui s'hi assegui.

5. Mostra els equips del domini des de:

○ Active Directory
○ PowerShell
