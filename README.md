# Patching automatizzato con Ansible

## Patching Unix

Questo progetto utilizza Ansible per automatizzare il processo di aggiornamento sui sistemi Unix, riducendo al minimo i tempi di intervento manuale e garantendo maggiore sicurezza.
Una volta avviato, il sistema esegue automaticamente le seguenti operazioni:

Sospensione del monitoraggio in Zabbix
Per evitare falsi allarmi durante il patching, viene creata una manutenzione temporanea su Zabbix per i server coinvolti.

Snapshot delle VM su Proxmox
Prima di applicare gli aggiornamenti, il sistema esegue uno snapshot a freddo su Proxmox, spegnendo temporaneamente le macchine virtuali, scattando un'istantanea e riavviandole.

Applicazione delle patch sui sistemi Unix
Gli aggiornamenti di sicurezza vengono scaricati e installati con dnf, e il sistema viene riavviato solo se è stato aggiornato il kernel.

## Patching Windows

TBD
