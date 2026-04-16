# Informativa sulla Privacy per PiHoleMonitor

Ultimo aggiornamento: 16 aprile 2026

## 1. Informazioni Generali
La presente informativa sulla privacy descrive la natura, l'ambito e la finalità della raccolta e dell'uso dei dati personali durante l'utilizzo dell'app "PiHoleMonitor".

Responsabile:
Christian Jurtz
Haubachstr. 48
16540 Hohen Neuendorf
Germania
mountainfields@jurtz.de

## 2. Principio Fondamentale
L'app è progettata per monitorare la **propria** istanza Pi-hole®.
**Non abbiamo accesso ai tuoi dati Pi-hole.**
La comunicazione avviene esclusivamente e direttamente tra il tuo dispositivo (smartphone) e il tuo server Pi-hole. Le tue credenziali (token API, password) sono memorizzate in modo criptato sul tuo dispositivo e non lo lasciano mai.

## 3. Autorizzazioni e Trattamento dei Dati

### 3.1 Accesso alla Rete (INTERNET)
L'app richiede l'accesso alla rete per connettersi al server Pi-hole configurato.
* **Dati:** Indirizzo IP, nomi host, token API.
* **Trattamento:** I dati vengono elaborati esclusivamente a livello locale e non vengono inviati a noi o a terze parti.
* **Base Giuridica:** Legittimo interesse (Art. 6 par. 1 lett. f GDPR) nella funzionalità dell'app.

### 3.2 Blocco App e Biometria (USE_BIOMETRIC)
È possibile proteggere opzionalmente l'accesso all'app. Vengono utilizzati i metodi di sicurezza configurati sul dispositivo (es. impronta digitale, riconoscimento facciale o PIN/sequenza).
* **Trattamento:** La verifica viene eseguita esclusivamente a livello locale dal sistema operativo Android (Android Biometric API).
* **Privacy dei Dati:** L'app non ha mai accesso ai dati biometrici grezzi (come le immagini delle impronte) o al PIN. Riceviamo solo una conferma ("Successo" o "Errore") dal sistema. I dati biometrici non lasciano mai l'hardware sicuro del dispositivo (Art. 9 GDPR).

### 3.3 Segnalazione arresti anomali (Crash Reporting)
Per migliorare la stabilità dell'app, è possibile scegliere di inviare un rapporto in caso di arresto anomalo.
* **Tipo:** Opt-In (disabilitato per impostazione predefinita). È necessario acconsentire esplicitamente nelle impostazioni ("Crash Reporting Consent").
* **Destinatario:** I dati vengono inviati al nostro server (`https://www.mountainfields.de/crash`). **Nessuna** condivisione con fornitori terzi.
* **Dati Raccolti:**
    * Tipo di dispositivo, modello, produttore, versione di Android.
    * Utilizzo della memoria (RAM) al momento del crash.
    * Rapporto tecnico sull'errore (Stacktrace).
    * Estratto del log di sistema (Logcat, max 200 righe).
* **Conservazione:** I rapporti sono conservati sul nostro server per un massimo di 30 giorni per l'analisi e poi eliminati. Sul dispositivo, vengono eliminati subito dopo la trasmissione.
* **Base Giuridica:** Il tuo consenso (Art. 6 par. 1 lett. a GDPR). Puoi revocarlo in qualsiasi momento nelle impostazioni dell'app.

### 3.4 Debug Avanzato (Session Recording)
È possibile avviare manualmente una registrazione dettagliata degli errori ("Session Recording").
* **Tipo:** Manuale (Opt-In). La registrazione inizia solo tramite interazione specifica.
* **Trattamento:** Il file (`debug_reports`) viene generato **esclusivamente in locale** sul dispositivo. **Non esiste un caricamento automatico.** L'utente decide autonomamente se condividere questo file.
* **Conservazione:**
    * I **dati grezzi** della registrazione vengono **eliminati immediatamente** dopo la generazione del rapporto.
    * Il rapporto generato è **temporaneamente memorizzato per l'esportazione** e viene **eliminato automaticamente dal dispositivo dopo massimo 1 ora**.
* **Contenuto del Rapporto:**
    * Versione app, tipo di build, hash Git.
    * Informazioni di rete (stato WiFi/Cellulare/VPN).
    * **Dati Mascherati:** Dominio Pi-hole configurato, **indirizzi IP offuscati** (es. `192.168.xxx.xxx`), indirizzi MAC e ID sessione (SID).
    * Stato del certificato SSL.
    * Log delle attività dell'app durante la sessione di registrazione.
* **Nota:** Nonostante il mascheramento, il rapporto può contenere **metadati tecnici**. **Condividilo solo con persone fidate.** L'utente è l'unico responsabile della condivisione di questo file con terzi.

## 4. Archiviazione di Dati Sensibili
I token API e le password sono memorizzati nell'**Android Keystore System** e nelle `SharedPreferences` (criptati con AES-256 GCM). Questi dati non lasciano il dispositivo, se non per l'autenticazione verso il proprio server.

## 5. I Tuoi Diritti
Hai il diritto di accesso, rettifica, cancellazione, limitazione del trattamento e portabilità dei dati (Art. 15–20 GDPR).
* **Contatto:** Per esercitare i tuoi diritti, contatta l'indirizzo email sopra indicato.
* **Reclamo:** Hai il diritto di proporre reclamo a un'autorità di controllo.

## 6. Sicurezza dei Dati
Implementiamo misure tecniche e organizzative (es. crittografia, controlli di accesso) per proteggere i dati da perdita, uso improprio o accesso non autorizzato (Art. 32 GDPR).

## 7. Modifiche alla presente Informativa
Ci riserviamo il diritto di aggiornare questa informativa. Le modifiche saranno pubblicate qui.
