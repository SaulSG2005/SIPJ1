# Sprint 5: Instal·lació i configuració de Windows

## Fase 1 - Instal·lació del sistema operatiu

Pas 1: Crear màquina virtual amb VirtualBox. 



Pas 2: Assignar recursos (RAM mínim 4 GB, disc mínim 40 GB).



Pas 3: Carregar ISO de Windows 10 o Windows 11. 



Pas 4: Instal·lar el sistema (idioma, usuari, contrasenya). 

<img width="1007" height="750" alt="image" src="https://github.com/user-attachments/assets/ea014fad-76d3-4061-bb1b-203ab62631c8" />

Pas 5: Comprovar que arrenca correctament. 



## Fase 2 - Punts de restauració

Pas 6: Cercar "Crear un punt de restauració". 


Pas 7: Activar protecció del sistema al disc C:. 


Pas 8: Crear un punt manual. 


Pas 9: Fer un canvi (instal·lar app o configuració). 


Pas 10: Restaurar i comprovar.

## Fase 3 - Llicències de Windows

Pas 11: Obrir Configuració → Sistema → Activació. 


Pas 12: Veure si Windows està activat. 


Pas 13: Executar al cmd: slmgr /xpr. 


Pas 14: Esbrinar llicenciament Windows i explicar breument. 


Pas 15: Consultar preu aproximat d'una llicència Windows (web oficial o botigues).

## Fase 4 - Gestor d'arrencada

Pas 16: Obrir Command Prompt com administrador. 

Pas 17: Executar bcdedit. 

Pas 18: Identificar els blocs: Administrador de arranque de Windows (Boot Manager) i Cargador de arranque de Windows (Boot Loader). 

Pas 19: Interpretar dades concretes: 

- Boot Manager: default {current} (sistema per defecte) i timeout 30 (temps d'espera). 

- Boot Loader: device partition=C: (on està instal·lat), path \Windows\system32\winload.efi (fitxer de càrrega) i description Windows 11. 

Pas 20: Respondre preguntes sobre quin sistema arrenca, en quina partició, temps d'espera i fitxer d'inici. 

Pas 21: Interpretació final: Qui decideix l'arrencada (Boot Manager) i qui carrega el sistema (Boot Loader). 

## Fase 5 - Xarxa bàsica

Pas 22: Obrir configuració de xarxa. 


Pas 23: Consultar IP amb: ipconfig. 


Pas 24: Configurar IP dinàmica (DHCP automàtic). 


Pas 25: Configurar IP fixa (manual: IP, màscara, gateway, DNS). 


Pas 26: Comprovar connexió amb: ping google.com.

## Fase 6 - Comandes generals

Pas 27: Obrir PowerShell. 

Pas 28: Diferenciar cmd (comandes bàsiques) i PowerShell (treball amb objectes i automatització). 

Pas 29: Comandes bàsiques: dir (veure fitxers), cd (moure's), mkdir (crear carpeta), echo hola > fitxer.txt (crear fitxer), del (eliminar). 

Pas 30: Comandes de sistema: tasklist (processos), taskkill /IM notepad.exe /F (tancar procés), systeminfo (informació sistema), hostname (nom equip), whoami (usuari). 

Pas 31: Comandes de xarxa: ipconfig, ping google.com, netstat -an (connexions obertes). 

Pas 32: Comandes avançades: tree (estructura), cls (netejar), help (ajuda), shutdown /s /t 0 (apagar). 

Pas 33: Mini interpretació de tasklist, ipconfig i systeminfo. 

## Fase 7 - Instal·lació d'aplicacions

Pas 34 i 35: Descarregar i instal·lar un programa des del navegador (ex: Chrome o VS Code). 


Pas 36: Obrir-lo i comprovar que funciona. 


Pas 37 i 38: Instal·lar i provar una aplicació des de Microsoft Store. 


Pas 39: Desinstal·lar una aplicació des de Configuració → Aplicacions. 


Pas 40: Verificació final.
