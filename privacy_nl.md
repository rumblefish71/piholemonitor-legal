# Privacybeleid voor PiHoleMonitor

Laatst bijgewerkt: 16 april 2026

## 1. Algemene Informatie
Dit privacybeleid informeert u over de aard, omvang en het doel van de verzameling en het gebruik van persoonsgegevens bij het gebruik van de app "PiHoleMonitor".

Verantwoordelijke:
Christian Jurtz
Haubachstr. 48
16540 Hohen Neuendorf
Duitsland
mountainfields@jurtz.de

## 2. Basisprincipe
De app is ontworpen om uw **eigen** Pi-hole®-instantie te monitoren.
**Wij hebben geen toegang tot uw Pi-hole gegevens.**
Communicatie vindt uitsluitend en rechtstreeks plaats tussen uw apparaat (smartphone) en uw Pi-hole server. Uw inloggegevens (API-tokens, wachtwoorden) worden versleuteld op uw apparaat opgeslagen en verlaten dit niet.

## 3. Machtigingen en Gegevensverwerking

### 3.1 Netwerktoegang (INTERNET)
De app vereist netwerktoegang om verbinding te maken met uw geconfigureerde Pi-hole server.
* **Gegevens:** IP-adres, hostnamen, API-token.
* **Verwerking:** Gegevens worden uitsluitend lokaal verwerkt en niet naar ons of derden verzonden.
* **Juridische grondslag:** Gerechtvaardigd belang (Art. 6 lid 1 sub f AVG) bij de functionaliteit van de app.

### 3.2 App-vergrendeling & Biometrie (USE_BIOMETRIC)
U kunt optioneel de toegang tot de app beveiligen. Dit maakt gebruik van de beveiligingsmethoden die op uw apparaat zijn ingesteld (bijv. vingerafdruk, gezichtsherkenning of PIN/patroon).
* **Verwerking:** Verificatie wordt uitsluitend lokaal uitgevoerd door het Android-besturingssysteem (Android Biometric API).
* **Privacy:** De app heeft nooit toegang tot uw ruwe biometrische gegevens of uw PIN. We ontvangen alleen een bevestiging ("Succes" of "Fout") van het systeem. Biometrische gegevens verlaten nooit de beveiligde hardwareopslag van uw apparaat (Art. 9 AVG).

### 3.3 Crashrapportage
Om de stabiliteit van de app te verbeteren, kunt u ervoor kiezen om bij een crash een foutrapport te verzenden.
* **Type:** Opt-In (standaard uitgeschakeld). U moet expliciet toestemming geven in de instellingen ("Crash Reporting Consent").
* **Ontvanger:** Gegevens worden verzonden naar onze eigen server (`https://www.mountainfields.de/crash`). **Geen** deling met externe partijen.
* **Verzamelde gegevens:**
    * Apparaattype, model, fabrikant, Android-versie.
    * Geheugengebruik (RAM) op het moment van de crash.
    * Technisch foutrapport (Stacktrace).
    * Fragment van het systeemlogboek (Logcat, max. 200 regels).
* **Bewaartermijn:** Rapporten worden maximaal 30 dagen bewaard voor analyse en daarna verwijderd. Op het apparaat worden ze direct na verzending verwijderd.
* **Juridische grondslag:** Uw toestemming (Art. 6 lid 1 sub a AVG). U kunt dit op elk gewenst moment intrekken.

### 3.4 Geavanceerd Foutopsporing (Session Recording)
U kunt handmatig een gedetailleerde foutopname starten ("Session Recording").
* **Type:** Handmatig (Opt-In).
* **Verwerking:** Het bestand (`debug_reports`) wordt **uitsluitend lokaal** gegenereerd. **Er is geen automatische upload.** U beslist zelf of u dit bestand deelt.
* **Bewaartermijn:**
    * De **ruwe gegevens** worden **direct na generatie** van het rapport verwijderd.
    * Het rapport wordt **tijdelijk gebufferd voor export** en na **max. 1 uur automatisch van het apparaat verwijderd**.
* **Inhoud rapport:**
    * App-versie, build-type, Git-hash.
    * Netwerkinformatie (WiFi/Mobiel/VPN-status).
    * **Gemaskeerde gegevens:** Geconfigureerd Pi-hole domein, **geanonimiseerde IP-adressen** (bijv. `192.168.xxx.xxx`), MAC-adressen en sessie-ID's (SID's).
    * Status SSL-certificaat.
    * Logboek van app-activiteiten tijdens de sessie.
* **Opmerking:** Ondanks maskering kan dit rapport **technische metadata** bevatten. **Deel het alleen met vertrouwde personen.**

## 4. Opslag van Gevoelige Gegevens
API-tokens en wachtwoorden worden opgeslagen in het **Android Keystore Systeem** en in `SharedPreferences` (AES-256 GCM versleuteld).

## 5. Uw Rechten
U heeft recht op inzage, rectificatie, wissing, beperking van de verwerking en overdraagbaarheid van gegevens (Art. 15–20 AVG).
* **Contact:** Neem contact op via het bovenstaande e-mailadres om uw rechten uit te oefenen.
* **Klachtrecht:** U heeft het recht om een klacht in te dienen bij een toezichthoudende autoriteit.

## 6. Gegevensbeveiliging
Wij implementeren technische en organisatorische maatregelen (bijv. versleuteling) om uw gegevens te beschermen (Art. 32 AVG).

## 7. Wijzigingen
Wij behouden ons het recht voor om dit privacybeleid bij te werken. Wijzigingen worden hier gepubliceerd.