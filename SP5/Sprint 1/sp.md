# Sprint 5: Instal·lació i configuració de Windows

## Fase 1 - Instal·lació del sistema operatiu

Pas 1: Crear màquina virtual amb VirtualBox. 

Pas 2: Assignar recursos (RAM mínim 4 GB, disc mínim 40 GB).

Pas 3: Carregar ISO de Windows 10 o Windows 11. 

Pas 4: Instal·lar el sistema (idioma, usuari, contrasenya). 

<img width="1007" height="750" alt="image" src="https://github.com/user-attachments/assets/ea014fad-76d3-4061-bb1b-203ab62631c8" />

Pas 5: Comprovar que arrenca correctament. 

<img width="1035" height="781" alt="image" src="https://github.com/user-attachments/assets/c65413e8-9df3-4ce5-964f-c2e47e6bb01a" />

## Fase 2 - Punts de restauració

Pas 6: Cercar "Crear un punt de restauració". 

<img width="412" height="486" alt="image" src="https://github.com/user-attachments/assets/3f8b70ea-9784-40d8-929e-3ed9d30e2912" />

Pas 7: Activar protecció del sistema al disc C:. 

<img width="477" height="517" alt="image" src="https://github.com/user-attachments/assets/aee64797-79fe-47df-a478-8cc60096e9f6" />

Pas 8: Crear un punt manual. 

<img width="477" height="517" alt="image" src="https://github.com/user-attachments/assets/114fc43b-20dc-4dcb-b84d-f6a5175c6e7a" />

Pas 9: Fer un canvi (instal·lar app o configuració). 

He instal·lat el VSCode:

<img width="387" height="373" alt="image" src="https://github.com/user-attachments/assets/1de150fd-1591-4bd6-9da3-31ad9d4a295c" />

Pas 10: Restaurar i comprovar.

<img width="559" height="455" alt="image" src="https://github.com/user-attachments/assets/427d6bf6-faef-47ba-a8bf-cb42cc83d96e" />

<img width="1030" height="771" alt="image" src="https://github.com/user-attachments/assets/18ff89eb-db08-41a8-9a3c-cce25a982e0a" />

## Fase 3 - Llicències de Windows

Pas 11: Obrir Configuració → Sistema → Activació. 

<img width="324" height="543" alt="image" src="https://github.com/user-attachments/assets/c52fb6b6-c502-4ec2-9a81-e7efa7497671" />


Pas 12: Veure si Windows està activat. 

<img width="1030" height="771" alt="image" src="https://github.com/user-attachments/assets/086c39e6-4e37-488c-bbe0-f7781bb55e73" />

Pas 13: Executar al cmd: slmgr /xpr. 

<img width="1029" height="777" alt="image" src="https://github.com/user-attachments/assets/c0db7e7d-6728-4b26-a55c-40fee40ebc55" />

Pas 14: Esbrinar llicenciament Windows i explicar breument. 

Per lo que he pogut investigar windows te per defecte el mode Notificacio fins que no actives el llicenciament i despres ho has de desactivar manualment als settings

Pas 15: Consultar preu aproximat d'una llicència Windows (web oficial o botigues).

Oficialment per part de microsoft ja no es poden comprar pero hi ha la opcio de comprar per altres venedors:

<img width="1029" height="777" alt="image" src="https://github.com/user-attachments/assets/c4bdc582-c64b-4904-beac-d22f4099f125" />


## Fase 4 - Gestor d'arrencada

Pas 16: Obrir Command Prompt com administrador. 

<img width="1029" height="777" alt="image" src="https://github.com/user-attachments/assets/d8965cf1-04cb-4111-b97b-defc0f4f786b" />

Pas 17: Executar bcdedit. 

<img width="1029" height="777" alt="image" src="https://github.com/user-attachments/assets/1f24bc87-5201-46f4-af55-cafe6d18ec4b" />

Pas 18: Identificar els blocs: Administrador de arranque de Windows (Boot Manager) i Cargador de arranque de Windows (Boot Loader). 

Boot Manager:

<img width="508" height="203" alt="image" src="https://github.com/user-attachments/assets/b7c8defa-885f-4baf-940f-2ab881a24217" />

Boot Loader:

<img width="503" height="284" alt="image" src="https://github.com/user-attachments/assets/55334e9d-8161-412f-8a69-1ae42798d6b3" />

Pas 19: Interpretar dades concretes: 

- Boot Manager: default {current} (sistema per defecte) i timeout 30 (temps d'espera). 

El defualt te indica que el sistema s'iniciara sense fer res a no ser que faigues algo, el timeout es el temps despera que tens fins que el sistema arranca de forma automatica.

<img width="273" height="89" alt="image" src="https://github.com/user-attachments/assets/8ce6afde-812c-4087-ba4d-6f989e8d15c0" />

- Boot Loader: device partition=C: (on està instal·lat), path \Windows\system32\winload.efi (fitxer de càrrega) i description Windows 11.

<img width="430" height="167" alt="image" src="https://github.com/user-attachments/assets/553cc8c9-cf56-4c1e-9ad3-483ef98432ca" />

Pas 20: Respondre preguntes sobre quin sistema arrenca, en quina partició, temps d'espera i fitxer d'inici. 

Te un temps despera de 30:

<img width="273" height="89" alt="image" src="https://github.com/user-attachments/assets/8ce6afde-812c-4087-ba4d-6f989e8d15c0" />

El sistema de arranc esta en la particio C del disco (No confundir amb osdevice), al path esta el fitxer on es executa el arranc que es un .exe i en la descripcio podem veure que es un windows 10:

<img width="430" height="167" alt="image" src="https://github.com/user-attachments/assets/553cc8c9-cf56-4c1e-9ad3-483ef98432ca" />

Pas 21: Interpretació final: Qui decideix l'arrencada (Boot Manager) i qui carrega el sistema (Boot Loader). 

El Boot Manager decideix quin sistema ha de arrancar amb les condicions que se li diu mentre que el boot loader es el que arranca el sistema una vegada se li han pasat les instruccions d'arranc.

## Fase 5 - Xarxa bàsica

Pas 22: Obrir configuració de xarxa. 

<img width="1024" height="724" alt="image" src="https://github.com/user-attachments/assets/430d37c8-3a3c-47f8-86dc-787cb525a93f" />

Pas 23: Consultar IP amb: ipconfig. 

<img width="1024" height="724" alt="image" src="https://github.com/user-attachments/assets/08330449-9934-4a03-bc78-b2feaf1de512" />

Pas 24: Configurar IP dinàmica (DHCP automàtic). 

<img width="1024" height="724" alt="image" src="https://github.com/user-attachments/assets/3a54c74e-b611-4433-ac95-5b0fb95e9b23" />

Pas 25: Configurar IP fixa (manual: IP, màscara, gateway, DNS). 

<img width="1024" height="724" alt="image" src="https://github.com/user-attachments/assets/07ca1756-22e4-4a2b-b7ca-b8daf6eae342" />

Pas 26: Comprovar connexió amb: ping google.com.

<img width="1024" height="724" alt="image" src="https://github.com/user-attachments/assets/4e2811cb-05b7-4cab-a58e-a7cc9630cd59" />

## Fase 6 - Comandes generals

Pas 27: Obrir PowerShell. 

<img width="1024" height="724" alt="image" src="https://github.com/user-attachments/assets/18ad32ba-2269-405c-8667-728590e43dba" />

Pas 28: Diferenciar cmd (comandes bàsiques) i PowerShell (treball amb objectes i automatització). 

La diferència entre el CMD (Símbol del sistema) i PowerShell es que el CMD és una eina del passat per a tasques senzilles, i PowerShell és una eina moderna i ultra-potent per a administradors.

Pas 29: Comandes bàsiques: dir (veure fitxers), cd (moure's), mkdir (crear carpeta), echo hola > fitxer.txt (crear fitxer), del (eliminar). 

Mkdir:

<img width="404" height="159" alt="image" src="https://github.com/user-attachments/assets/c5aabbc7-98c0-4dfb-8185-ea98776d5e93" />

Dir:

<img width="441" height="323" alt="image" src="https://github.com/user-attachments/assets/9057732c-3818-4684-8e23-aed4d2662bd8" />

Cd:

<img width="215" height="36" alt="image" src="https://github.com/user-attachments/assets/e128b83c-3b44-4425-839e-b40f5c892a07" />

Echo:

<img width="433" height="155" alt="image" src="https://github.com/user-attachments/assets/fbfb7634-d442-4d16-af1f-54a653041642" />

Del:

<img width="308" height="53" alt="image" src="https://github.com/user-attachments/assets/cae03ade-8866-4ed9-a1ed-83bee131f4e4" />

Pas 30: Comandes de sistema: tasklist (processos), taskkill /IM notepad.exe /F (tancar procés), systeminfo (informació sistema), hostname (nom equip), whoami (usuari). 

Tasklist:

<img width="859" height="398" alt="image" src="https://github.com/user-attachments/assets/43e05844-5e9e-4922-9422-ffbd24e794fa" />

taskkill:

<img width="421" height="159" alt="image" src="https://github.com/user-attachments/assets/acd4b881-22d5-44b0-b8ff-8c5531db31ef" />

Systeminfo:

<img width="839" height="669" alt="image" src="https://github.com/user-attachments/assets/63648f0d-5f97-4b6b-af18-b93ea364f7c3" />

Hostname:

<img width="208" height="53" alt="image" src="https://github.com/user-attachments/assets/75e40193-e887-4d82-92e0-0339bbc71392" />

Whoami:

<img width="208" height="53" alt="image" src="https://github.com/user-attachments/assets/d29f9672-0bc1-4f39-850d-18e41e12f7d4" />

Pas 31: Comandes de xarxa: ipconfig, ping google.com, netstat -an (connexions obertes). 

Ipconfig:

<img width="543" height="235" alt="image" src="https://github.com/user-attachments/assets/895791fb-e980-4448-bcff-f822e4d6ea53" />

Ping:

<img width="543" height="235" alt="image" src="https://github.com/user-attachments/assets/a0edc8b0-fce7-4408-bdc3-dd9f5d566a6f" />

Netstat:

<img width="482" height="610" alt="image" src="https://github.com/user-attachments/assets/e2c0c44e-70e2-4927-9b33-abba3bc8d4d3" />

Pas 32: Comandes avançades: tree (estructura), cls (netejar), help (ajuda), shutdown /s /t 0 (apagar). 

Tree:

<img width="314" height="317" alt="image" src="https://github.com/user-attachments/assets/c68d11bd-e31e-4105-94e6-e59d55e61d5f" />

Cls:

Es un clear

<img width="319" height="329" alt="image" src="https://github.com/user-attachments/assets/1cafdbee-72df-4efb-b764-4cb01ea21a26" />

<img width="319" height="329" alt="image" src="https://github.com/user-attachments/assets/258af0f6-6baf-4a77-b93b-17e96d7d8426" />

Help:

<img width="576" height="661" alt="image" src="https://github.com/user-attachments/assets/0df3bbed-34f1-4816-8025-678bd85c8b77" />

Shutdown:

Aqui no fare la prova de execucio ja que se me apagaria la maquina.

<img width="440" height="107" alt="image" src="https://github.com/user-attachments/assets/9a8d3214-4885-4819-a61f-f6abb221ae96" />

Pas 33: Mini interpretació de tasklist, ipconfig i systeminfo. 

Tasklist te dona una llista de tots els processos que el sistema te en funcionament en el moment, ipconfig te dona la informacio de la network i systeminfo te dona la informacio del sistema.

## Fase 7 - Instal·lació d'aplicacions

Pas 34 i 35: Descarregar i instal·lar un programa des del navegador (ex: Chrome o VS Code). 

VSCode:

<img width="1026" height="769" alt="image" src="https://github.com/user-attachments/assets/a8804c19-cf96-4b85-93d3-00c0375aacdc" />

Pas 36: Obrir-lo i comprovar que funciona. 

<img width="1026" height="769" alt="image" src="https://github.com/user-attachments/assets/54d8fe02-5c16-4dd9-8262-2ab981699551" />

Pas 37 i 38: Instal·lar i provar una aplicació des de Microsoft Store. 

Spotify:

<img width="1026" height="769" alt="image" src="https://github.com/user-attachments/assets/75ee5108-2a3f-4935-8c06-7864e6a153c1" />

<img width="1026" height="769" alt="image" src="https://github.com/user-attachments/assets/1ce33278-bb32-422c-b3ba-782a7e72a193" />

Pas 39: Desinstal·lar una aplicació des de Configuració → Aplicacions. 

<img width="1026" height="769" alt="image" src="https://github.com/user-attachments/assets/2410cae4-94f8-4000-88f7-d612be284592" />

<img width="1026" height="769" alt="image" src="https://github.com/user-attachments/assets/4ba78142-096d-433d-8810-bef2f20f63f1" />

Pas 40: Verificació final.
