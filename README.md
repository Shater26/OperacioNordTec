# Fernando Afonso
## Operació NordTec
### índex
---
1. Comprovar els canvis amb `git status`.
2. Afegir els fitxers amb `git add`.
3. Crear un commit amb `git commit -m "Inserta texte"`.
4. Pujar els canvis amb `git push`.

## Arquitectura de Xarxa
La xarxa de la màquina d’Isard es divideix en tres segments: Kali (`10.0.0.1/24`), DMZ (`192.168.10.1/24`) i LAN (`192.168.20.1/24`). Les interfícies `enp1s0` i `enp2s0` obtenen la IP automàticament.

També hem configurat les màquines:
- **Servidor (DMZ):** `192.168.10.11/24`, amb el Netplan configurat correctament. Fa ping a `8.8.8.8` i a `192.168.10.1`.
- **Client (LAN):** `192.168.20.10/24`, amb el Netplan configurat correctament. Fa ping a `8.8.8.8` i a `192.168.20.1`.

## Configuracions — Fase 1: connexió a Internet
Hem configurat el client Ubuntu (`192.168.20.10/24`) i el servidor (`192.168.10.1`), i hem habilitat la redirecció IPv4 a la màquina firewall. Així, els equips poden connectar-se a la xarxa i sortir a Internet. També hem documentat la configuració al fitxer `yaml/xarxa_maquines.yaml`. Cada equip té o tindrà el seu xml identificatiu. Fase 1 completada.
## Incidències i solucions:
1. xml mal configurat:
<?xml version="1.0" encoding="UTF-8"?>
<maquina rol=web>
   <nom>nortec-lan</nom>
   <ip>192.168.10.10
   <codi>0F2A</Codi>
<\maquina>

## Missatge d'error exacte
1. XML MAL CONFIGURAT
isard@ubuntu-server:~$ xmllint -noout maquina_wrong.xml
maquina_wrong.xml:5: parser error : Opening and ending tag mismatch: codi line 5 and Codi
  <codi>0F2A</Codi>
                   ^
maquina_wrong.xml:6: parser error : StartTag: invalid element name
<\maquina>
 ^
maquina_wrong.xml:7: parser error : Premature end of data in tag ip line 4

^
isard@ubuntu-server:~$ sudo nano maquina_wrong.xml
isard@ubuntu-server:~$ xmllint -noout maquina_wrong.xml
maquina_wrong.xml:5: parser error : Opening and ending tag mismatch: codi line 5 and Codi
  <codi>0F2A</Codi>
                   ^
maquina_wrong.xml:6: parser error : Opening and ending tag mismatch: ip line 4 and maquina
</maquina>
          ^
maquina_wrong.xml:7: parser error : Premature end of data in tag maquina line 2

^
isard@ubuntu-server:~$ sudo nano maquina_wrong.xml
isard@ubuntu-server:~$ xmllint -noout maquina_wrong.xml
maquina_wrong.xml:5: parse
2. 
## Quan: fase i context.
Fase 1: els primers equips de NordTec han arribat a l’oficina i necessiten connexió a la xarxa i accés a Internet. La configuració s’ha de documentar i preparar per poder ampliar la xarxa.
## Causa: per què passava.
## Solució: què vam fer.
## Detectada per: @usuari
## Decisions tècniques (què heu triat, per què, alternatives)
## Reflexions tècniques
