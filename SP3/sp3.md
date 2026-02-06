
# Sprint 3: Gestio de Dominis i Accessos

## Instal·lacio domini LDAP i unir client al domini

Posarem les dos maquines virtuals a una mateixa xarxa NAT:

<img width="1056" height="606" alt="image" src="https://github.com/user-attachments/assets/c139ef87-ca6e-438c-bda4-adb7ea8c6ae9" />

Posarem la IP fixa del servidor a la 10.0.2.15:

<img width="1056" height="606" alt="image" src="https://github.com/user-attachments/assets/0890e9d7-3b9d-4a2d-8052-b0f7976684b8" />

Fem la prova de que la IP es fixa i te conexio a internet:

<img width="1056" height="622" alt="image" src="https://github.com/user-attachments/assets/9819b29e-e373-407d-a702-9dc0ea7e7221" />

Canviem el hostname per a crear despres el domini:

<img width="1056" height="622" alt="image" src="https://github.com/user-attachments/assets/5cee24c2-1797-4fba-915a-72babbc746b0" />

Creem aa la carpeta hosts una direccio de domini amb la IP del servidor:

<img width="701" height="187" alt="image" src="https://github.com/user-attachments/assets/5bbaf5d3-fdff-4b88-879b-d71a0e2f342f" />

Instalem el ldap per al servidor:

<img width="1128" height="579" alt="image" src="https://github.com/user-attachments/assets/6992cb6f-03ea-47c5-875a-b597d53596ce" />

Confirmem la contrasenya:

<img width="1060" height="194" alt="image" src="https://github.com/user-attachments/assets/fdbe78e4-9b8a-4d46-a850-19c6771a0f8b" />

fem un salpcat per a confirmar la instal·lacio:

<img width="565" height="308" alt="image" src="https://github.com/user-attachments/assets/93993d8b-dd8d-4920-84dd-255ac3e53e4d" />

configurem el LDAP:

<img width="728" height="479" alt="image" src="https://github.com/user-attachments/assets/b051e454-84e3-419d-a642-89b4424ebd1e" />

Li diem que si:

<img width="728" height="479" alt="image" src="https://github.com/user-attachments/assets/5d970296-9aaf-4303-b7e6-58edb43d3e56" />

Li diem que si:

<img width="728" height="479" alt="image" src="https://github.com/user-attachments/assets/4fb1ae69-1856-4ee1-a6f1-0171b6059bcc" />

Tornem a confirmar els canvis:

<img width="483" height="294" alt="image" src="https://github.com/user-attachments/assets/abd75857-a14a-48d9-9d4a-55cf0b46452a" />

Creem una unitat Organitzativa:

<img width="732" height="481" alt="image" src="https://github.com/user-attachments/assets/8fb7a896-ae7e-4461-9cf7-116ef29b29bf" />

Creem el grup de la uo:

<img width="732" height="481" alt="image" src="https://github.com/user-attachments/assets/1d7e13fe-ee9a-44a7-8272-06dd1ffdaf32" />

Creem els usuaris de la uo:

<img width="732" height="481" alt="image" src="https://github.com/user-attachments/assets/dad13006-9d42-4b54-b8e9-e104dbc7caf3" />

Apliquem els 3 fitxers:

<img width="939" height="250" alt="image" src="https://github.com/user-attachments/assets/f4986ec1-9198-4c1a-872e-c299d5cc1579" />

Comprovem que esta tot correcte amb slapcat:

<img width="928" height="776" alt="image" src="https://github.com/user-attachments/assets/0597962b-2fda-470d-aac0-a9b123b684af" />

# Unir client al domini



<img width="1085" height="380" alt="image" src="https://github.com/user-attachments/assets/e21a70e3-eda5-410f-a109-e362ddd10c60" />

<img width="1170" height="251" alt="image" src="https://github.com/user-attachments/assets/e58b3fc8-56b6-4bdb-9893-9c776239b30e" />

<img width="1170" height="251" alt="image" src="https://github.com/user-attachments/assets/f3457414-0455-4466-8577-c64f851fa936" />

<img width="1170" height="251" alt="image" src="https://github.com/user-attachments/assets/1156c525-f9f8-43d0-ba48-fec4e14882dd" />

<img width="1170" height="251" alt="image" src="https://github.com/user-attachments/assets/00509867-194a-4376-b9dd-e2211ebd82e3" />

<img width="1170" height="251" alt="image" src="https://github.com/user-attachments/assets/df3206d1-c7b7-4c6d-833b-7b0134ac4f63" />

<img width="1170" height="251" alt="image" src="https://github.com/user-attachments/assets/8e358e0f-38be-4ec4-b60b-c2c88f496634" />

<img width="1170" height="251" alt="image" src="https://github.com/user-attachments/assets/f58fce2d-27f3-40aa-948e-679f970a176f" />

<img width="1170" height="251" alt="image" src="https://github.com/user-attachments/assets/ee22672a-8568-42cf-a664-9244c44030f1" />

<img width="1200" height="408" alt="image" src="https://github.com/user-attachments/assets/dddfd627-c125-4363-92a7-ea99964a048d" />

<img width="1156" height="623" alt="image" src="https://github.com/user-attachments/assets/7a9f9ff8-eda4-4c26-b1f6-dcb8183ed327" />

<img width="1154" height="665" alt="image" src="https://github.com/user-attachments/assets/c79fc569-473b-4252-a7c6-4cbe74783ed3" />

<img width="893" height="116" alt="image" src="https://github.com/user-attachments/assets/165091c0-7acd-4005-9a87-2f66aa0f9464" />



# Servidors SAMBA i NFS

## Servidor Samba

El servidor Samba i LFS serveis per compartir arxius, el SAMBA tambe te autentificacio a nivell ldap, mentre que NFS ho fa per IP.

<img width="740" height="447" alt="image" src="https://github.com/user-attachments/assets/e0aca282-2e80-49d9-baed-7d58175d5087" />

<img width="568" height="228" alt="image" src="https://github.com/user-attachments/assets/9b3324a0-b67b-4230-87be-0e324202fbb6" />

<img width="542" height="374" alt="image" src="https://github.com/user-attachments/assets/13b7cdf2-bc22-470c-8774-4cb5df8198b4" />

<img width="508" height="234" alt="image" src="https://github.com/user-attachments/assets/6eed3478-5f08-4500-a542-325bb8a07537" />

<img width="358" height="200" alt="image" src="https://github.com/user-attachments/assets/5adbe710-44ea-43d5-8f36-9c14f1089392" />

<img width="1112" height="727" alt="image" src="https://github.com/user-attachments/assets/c21df93d-0b2f-4b1a-8ef9-70ce7b1ad8b9" />

## Prova amb client

<img width="710" height="336" alt="image" src="https://github.com/user-attachments/assets/eab11f15-9a0e-425d-9ede-d9390c7a0dda" />

<img width="885" height="551" alt="image" src="https://github.com/user-attachments/assets/facaafdf-8eab-4277-91f9-ff60edb8e343" />

<img width="885" height="551" alt="image" src="https://github.com/user-attachments/assets/5806b7d7-016f-4c6d-a350-363c1923f6a8" />

<img width="885" height="551" alt="image" src="https://github.com/user-attachments/assets/b5d7c902-215d-4423-9a30-77febbd4abfa" />

<img width="885" height="551" alt="image" src="https://github.com/user-attachments/assets/4aa31f0a-a0db-44af-9afa-611cb4c6090e" />

<img width="885" height="551" alt="image" src="https://github.com/user-attachments/assets/01dfc6d3-efc9-4cb0-a169-4ced55ac2bf8" />

<img width="885" height="551" alt="image" src="https://github.com/user-attachments/assets/30779bbf-bcaa-4609-9e29-ee690138d197" />

<img width="885" height="551" alt="image" src="https://github.com/user-attachments/assets/f68df77b-0937-4135-ab78-7f3691e0d700" />

<img width="885" height="551" alt="image" src="https://github.com/user-attachments/assets/c170f590-1c91-4172-8fc5-b331535c9bf1" />

## Servidor NFS

<img width="725" height="272" alt="image" src="https://github.com/user-attachments/assets/857c5cf3-0709-4a9a-bc76-7916938ab052" />

<img width="735" height="257" alt="image" src="https://github.com/user-attachments/assets/4502218f-a5dd-4011-a174-6ba166e8da32" />

<img width="722" height="330" alt="image" src="https://github.com/user-attachments/assets/fdfdd187-1a94-4350-9f36-9b4b7575c555" />

<img width="722" height="330" alt="image" src="https://github.com/user-attachments/assets/68dca35c-52c1-4162-b1ad-1e2bef5f3150" />

<img width="722" height="330" alt="image" src="https://github.com/user-attachments/assets/e2b2a3dd-26d0-472c-be01-da4b2e6fe422" />

## Prova amb client

<img width="874" height="372" alt="image" src="https://github.com/user-attachments/assets/a8c54e33-85ca-4492-99b3-c13b78146c0a" />

<img width="874" height="372" alt="image" src="https://github.com/user-attachments/assets/843f639f-c7c1-4bd2-91be-2f91dbd96574" />

<img width="1202" height="400" alt="image" src="https://github.com/user-attachments/assets/93066c0d-b7ad-4a2f-91cf-5dbf22f0371e" />

<img width="534" height="135" alt="image" src="https://github.com/user-attachments/assets/f4962267-c943-42c0-b3dd-64f73818dede" />

<img width="782" height="243" alt="image" src="https://github.com/user-attachments/assets/d7c7f114-9a4b-428d-8048-b1540332492a" />

<img width="1010" height="318" alt="image" src="https://github.com/user-attachments/assets/1a372182-7da8-4e7d-ba21-3aa4fee5dfa6" />

<img width="1042" height="399" alt="image" src="https://github.com/user-attachments/assets/968c03ad-7c16-42ad-a0b4-a695ffa6f35d" />

<img width="565" height="181" alt="image" src="https://github.com/user-attachments/assets/e4d126fe-39f8-4ebe-9571-882e3424c817" />

<img width="727" height="304" alt="image" src="https://github.com/user-attachments/assets/bdc18c07-ea42-411a-9b51-cc7ee877ca25" />

<img width="727" height="304" alt="image" src="https://github.com/user-attachments/assets/fa9d180b-dbad-4f58-a669-772374b3d5c4" />

<img width="727" height="304" alt="image" src="https://github.com/user-attachments/assets/a6deccf7-1124-41d1-84ce-33d53d13f264" />

<img width="727" height="304" alt="image" src="https://github.com/user-attachments/assets/71c8c884-46a6-4d63-a5e8-5a29359672ca" />

<img width="731" height="428" alt="image" src="https://github.com/user-attachments/assets/b5dd858c-9275-4950-9104-5f5754620541" />

<img width="906" height="172" alt="image" src="https://github.com/user-attachments/assets/bea1790a-ab20-4304-8dec-2ddac3c89882" />

<img width="898" height="137" alt="image" src="https://github.com/user-attachments/assets/e510cdb6-beaa-4492-b756-2cae3d844940" />


## Exercici

Agarrar un windows i conectarnos a la carpeta compartida:

