# 📱 PiHoleMonitor – Guida Utente

Questo manuale ti aiuta a configurare e utilizzare l'app **PiHoleMonitor**. PiHoleMonitor è un client non ufficiale per **Pi-hole®**, che ti consente di monitorare e gestire comodamente le tue istanze di filtraggio pubblicitario attraverso un'interfaccia nativa realizzata con Jetpack Compose.

---

### 📖 Sommario
* [1. Sicurezza e Privacy](#1-sicurezza--privacy)
* [2. Configurazione del Server](#2-configurazione-del-server)
* [3. Dashboard](#3-dashboard)
* [4. Gestione](#4-gestione)
* [5. Log delle Query](#5-log-delle-query)
* [6. Sistema](#6-sistema)
* [7. Impostazioni](#7-impostazioni)

---

## 🛡️ 1. Sicurezza e Privacy
Poiché l'app interagisce con la tua infrastruttura di rete, la protezione dei dati è la nostra massima priorità.

* **Crittografia**: I dati sensibili come password e ID sessione non vengono mai memorizzati in testo semplice. L'app utilizza la **crittografia AES-GCM** all'interno dell'**Android KeyStore** protetto da hardware.
* **Autenticazione**: La comunicazione segue il protocollo ufficiale API utilizzando ID sessione sicuri (`sid`) e token CSRF.
* **Località**: PiHoleMonitor è "Offline-First". **Nessun dato viene trasmesso** a server cloud esterni del produttore. Tutte le connessioni avvengono direttamente tra il tuo smartphone e la tua istanza Pi-hole.
* **Biometria**: Puoi opzionalmente proteggere l'accesso all'app tramite impronta digitale, riconoscimento facciale o PIN.

---

## ⚙️ 2. Configurazione del Server
Per utilizzare l'app, devi registrare la tua istanza Pi-hole (supporta API v6+).

* **Nome Server**: Un nome a tua scelta per l'identificazione nell'app.
* **Dominio / IP**: L'indirizzo della tua istanza (es. `192.168.178.5`).
* **Porta**: La porta dell'interfaccia web (Default: `80` per HTTP o `443` per HTTPS).
* **Sottopercorso (Opzionale)**:
    > 💡 **Nginx / Reverse-Proxy**: Se il tuo Pi-hole è raggiungibile tramite un sottopercorso come `dominio.com/pihole`, inserisci qui `/pihole`. L'app aggiunge automaticamente il suffisso `/api/` necessario.
* **Password**: La password della tua interfaccia web Pi-hole.
* **Tipo di Connessione**: Scegli tra **HTTPS** (raccomandato) o **HTTP**.

### Test di Connessione e Salvataggio
* **Verifica Connessione**: Esegue una richiesta di test per validare la raggiungibilità e la correttezza della password.
* **Salva (Icona Disco)**: Memorizza i dati nell'archivio crittografato. Alla prima configurazione, questo server viene contrassegnato automaticamente come istanza attiva.

![Screenshot Server Setup](screenshots/new_server.jpg)
---

## 📊 3. Dashboard
La Dashboard offre una panoramica in tempo reale dello stato della tua rete.

* **Cronologia 24 ore**: Monitora le query DNS delle ultime 24 ore in un grafico dettagliato.
* **Statistiche Totali**: Riepilogo delle query totali, richieste bloccate e tasso di blocco attuale.
* **Classifica Client**: Identifica i client più attivi nella tua rete.

---

## 🗂️ 4. Gestione
Gestisci la configurazione di Pi-hole direttamente dall'app.

* **Client**: Visualizza, crea e modifica i client di rete.
* **Liste Ad (Gravity)**: Gestisci le sorgenti delle liste di blocco utilizzate per filtrare la pubblicità.
* **Domini**: Gestisci whitelist e blacklist (esatte o basate su regex).
* **Gruppi**: Organizza client e liste in gruppi logici.

---

## 🔍 5. Log delle Query
Approfondimenti dettagliati sul traffico DNS della tua rete.

* **Filtro Stato**: Filtra specificamente per query consentite, bloccate o memorizzate nella cache.
* **Ricerca**: Cerca domini specifici o indirizzi IP dei client.

---

## 💻 6. Sistema
Monitoraggio dell'hardware e dell'ambiente di rete.

* **Sistema Ospite**: Mostra informazioni sull'host, carico CPU, utilizzo RAM e stato del processo `pihole-FTL`.
* **Pi-hole**: Attiva/disattiva il filtro DNS, monitora l'utilizzo della cache DNS, esegui azioni Pi-hole e visualizza le notifiche di sistema.
* **Rete**: Panoramica dettagliata di gateway, interfacce e rotte.
* **DHCP**: Gestione dei lease DHCP attivi.

### Azioni Disponibili:
* **Riavvio FTL**: Riavvia il servizio DNS sulla tua istanza.
* **Aggiornamento Gravity**: Avvia un aggiornamento della lista di blocco.
* **Flush Log/ARP**: Cancella i log delle query DNS o pulisce la tabella di rete.

> [!CAUTION]
> **Attenzione**: L'esecuzione di azioni come il riavvio di FTL o l'aggiornamento di Gravity causerà una breve interruzione della risoluzione DNS per l'intera rete.
> 
> **Flush Log & ARP**: Queste azioni eliminano permanentemente tutti i log delle query e cancellano l'elenco dei dispositivi di rete noti.

---

## 🛠️ 7. Impostazioni
Personalizza la tua esperienza con PiHoleMonitor.

* **Tema e Lingua**: Passa tra modalità Chiara/Scura e seleziona la lingua di sistema preferita.
* **Notifiche**: Configura gli avvisi a livello di sistema.
* **Widget**: Personalizza l'aspetto dei widget nella schermata iniziale.
* **Sicurezza**: Configura le impostazioni di accesso biometrico.
* **Manutenzione**: Attiva o disattiva l'invio di rapporti sugli arresti anomali.
* **Registratore Log di Debug**: Utilizza il registratore di log per aiutare nella risoluzione dei problemi.
