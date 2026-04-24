# Sprint 4: Monitorització, connexió remota i llicenciament

## Monitoritzacio

Primerament farem una comprovacio en los logs en la maquina local amb dues terminals:

<img width="1272" height="796" alt="Captura de pantalla de 2026-03-13 12-29-22" src="https://github.com/user-attachments/assets/5b77010b-9c3d-49f6-9d11-3b49e5ac762c" />
<img width="1272" height="796" alt="Captura de pantalla de 2026-03-13 12-21-38" src="https://github.com/user-attachments/assets/ad867b24-140c-4fdf-b078-aaf1a6faa3f3" />
<img width="1272" height="796" alt="Captura de pantalla de 2026-03-13 12-19-38" src="https://github.com/user-attachments/assets/fecbe1e8-e387-4474-9941-e394eaeb86cf" />
<img width="1282" height="745" alt="Captura de pantalla de 2026-03-13 12-18-40" src="https://github.com/user-attachments/assets/d1c68c0d-928e-49ea-9449-6e6d249e51bf" />

A la carpeta /etc/rsyslog.d/50-default.conf podrem configurar el tipus de log del sistema:

<img width="1282" height="745" alt="Captura de pantalla de 2026-03-13 12-17-54" src="https://github.com/user-attachments/assets/698c4f9a-72f9-48df-b25a-9a9be65f8987" />

Farem una proba amb la modificacio feta anteriorment:

<img width="1198" height="561" alt="Captura de pantalla de 2026-03-13 12-16-31" src="https://github.com/user-attachments/assets/d7493d68-0acb-4807-87f0-baf1da2b0b79" />

En /etc/logrotate.conf podem manipular els log, ara crearem un fitxer log cada 4 setmanes per a que queden reguistrat:

<img width="734" height="483" alt="Captura de pantalla de 2026-03-13 12-04-09" src="https://github.com/user-attachments/assets/c2af659d-1566-46c8-9c00-b106bad1326a" />

El directori /etc/logrotate.d/ és una carpeta a Linux on s'emmagatzemen els fitxers de configuració específics de cada aplicació per a la utilitat:

<img width="723" height="119" alt="Captura de pantalla de 2026-03-13 12-03-21" src="https://github.com/user-attachments/assets/e74b24cc-9b39-4170-8945-1f11bdbcf301" />

Aqui podem veure tots els tipus de logs:

<img width="727" height="225" alt="Captura de pantalla de 2026-03-13 12-00-44" src="https://github.com/user-attachments/assets/dfea88dd-66bb-4ece-85ab-e86a84175852" />


## Prova SSH

<img width="730" height="348" alt="image" src="https://github.com/user-attachments/assets/550c3597-e495-4d61-aba6-8d703e29fe9a" />

<img width="1195" height="383" alt="image" src="https://github.com/user-attachments/assets/db34d37c-2f5f-4cf4-9398-c2e1ebc041a2" />

## Prova VNC

<img width="651" height="77" alt="image" src="https://github.com/user-attachments/assets/ae8a3e6f-550c-40cf-b087-2ced71a6e1cd" />

<img width="499" height="361" alt="image" src="https://github.com/user-attachments/assets/678da3a8-00db-457f-878c-8cf00a32d807" />

<img width="691" height="235" alt="image" src="https://github.com/user-attachments/assets/59e75e47-3a1b-4580-9b9b-dad4ed9f6bf4" />

<img width="395" height="85" alt="image" src="https://github.com/user-attachments/assets/d35b5e2b-4d5d-4825-861d-a48f992d17dd" />

<img width="806" height="632" alt="image" src="https://github.com/user-attachments/assets/59764b97-cb86-44d5-b127-7f076ef33cc1" />

<img width="1047" height="206" alt="image" src="https://github.com/user-attachments/assets/930ddf10-4a8b-4bc2-8759-3dbf10246428" />

## Windows 10

<img width="1007" height="750" alt="image" src="https://github.com/user-attachments/assets/ea014fad-76d3-4061-bb1b-203ab62631c8" />




