# Datenschutzerklärung für PiHoleMonitor

Stand: 22.12.2025

## 1. Allgemeine Hinweise
Diese Datenschutzerklärung klärt Sie über die Art, den Umfang und Zwecke der Erhebung und Verwendung personenbezogener Daten bei der Nutzung der App "PiHoleMonitor" (im Folgenden "App") auf.

Verantwortlicher:
Christian Jurtz
Haubachstr. 48
16540 Hohen Neuendorf
support@mountainfields.de

## 2. Grundprinzip
Die App dient der Überwachung Ihrer **eigenen** Pi-hole®-Instanz.
**Wir haben keinen Zugriff auf Ihre Pi-hole-Daten.**
Die Kommunikation findet ausschließlich direkt zwischen Ihrem Endgerät (Smartphone) und Ihrem Pi-hole-Server statt. Ihre Zugangsdaten (API-Token, Passwörter) werden verschlüsselt auf Ihrem Gerät gespeichert und verlassen dieses nicht.

## 3. Zugriffsrechte und Datenverarbeitung

### 3.1 Netzwerkzugriff (INTERNET)
Die App benötigt Zugriff auf das Netzwerk, um sich mit Ihrem konfigurierten Pi-hole-Server zu verbinden.
* **Daten:** IP-Adresse, Hostnamen, API-Token.
* **Verarbeitung:** Die Daten werden ausschließlich lokal verarbeitet und nicht an uns oder Dritte gesendet.
* **Rechtsgrundlage:** Berechtigtes Interesse (Art. 6 Abs. 1 lit. f DSGVO) an der Funktionalität der App.

### 3.2 Biometrische Authentifizierung (USE_BIOMETRIC)
Sie können die App optional mittels Fingerabdruck oder Gesichtsscan absichern.
* **Verarbeitung:** Die Prüfung erfolgt ausschließlich durch das Android-Betriebssystem. Die App erhält lediglich die Information "Erfolg" oder "Fehler". Biometrische Daten verlassen nie den sicheren Speicher Ihres Geräts (Art. 9 DSGVO).

### 3.3 Absturzberichte (Crash Reporting)
Um die Stabilität der App zu verbessern, können Sie im Falle eines Absturzes einen Fehlerbericht senden.
* **Art der Funktion:** Opt-In (Standardmäßig deaktiviert). Sie müssen in den Einstellungen ("Crash Reporting Consent") explizit zustimmen.
* **Empfänger:** Die Daten werden an unseren eigenen Server (`https://www.mountainfields.de/crash`) gesendet. **Keine** Weitergabe an Drittanbieter.
* **Gespeicherte Daten:**
    * Gerätetyp, Modell, Hersteller, Android-Version.
    * Speicherauslastung (RAM) zum Zeitpunkt des Absturzes.
    * Technischer Fehlerbericht (Stacktrace).
    * Auszug des System-Logs (Logcat, max. 200 Zeilen).
* **Speicherdauer:** Die Berichte werden bis zu 30 Tage auf unserem Server zur Fehleranalyse gespeichert und anschließend gelöscht. Auf dem Gerät werden sie nach erfolgreichem Versand sofort gelöscht.
* **Rechtsgrundlage:** Ihre Einwilligung (Art. 6 Abs. 1 lit. a DSGVO). Sie können diese jederzeit in den App-Einstellungen widerrufen.

### 3.4 Erweiterte Fehleranalyse (Debug Recording)
Sie können manuell eine detaillierte Fehleraufzeichnung starten („Session Recording“).
* **Art der Funktion:** Manuell (Opt-In). Die Aufzeichnung startet nur durch Ihre Interaktion.
* **Verarbeitung:** Die Datei (`debug_reports`) wird **ausschließlich lokal** auf Ihrem Gerät generiert. **Es erfolgt kein automatischer Upload.** Sie entscheiden selbst, ob Sie die Datei teilen.
* **Speicherdauer:**
    * Die **Rohdaten** der Aufzeichnung werden **sofort nach Erstellung des Berichts gelöscht**.
    * Der generierte Bericht wird **temporär für den Export zwischengespeichert** und **automatisch nach max. 1 Stunde** vom Gerät gelöscht.
* **Inhalt des Berichts:**
    * App-Version, Build-Typ, Git-Hash.
    * Netzwerkinformationen (WiFi/Mobilfunk/VPN-Status).
    * **Maskierte Daten:** Konfigurierte Pi-hole-Domain, **unkenntlich gemachte IP-Adressen** (z. B. `192.168.xxx.xxx`), MAC-Adressen und Session-IDs (SIDs).
    * SSL-Zertifikatsstatus.
    * Protokoll der App-Aktivitäten während der Aufzeichnung.
* **Hinweis:** Trotz Maskierung kann dieser Bericht **technische Metadaten** enthalten. **Teilen Sie ihn nur mit vertrauenswürdigen Personen.** Sie tragen die Verantwortung für die Weitergabe an Dritte.

## 4. Speicherung sensibler Daten
API-Tokens und Passwörter werden im **Android Keystore System** und in den `SharedPreferences` (AES-256 GCM verschlüsselt) gespeichert. Diese Daten verlassen Ihr Gerät nicht, außer zur Authentifizierung gegenüber Ihrem eigenen Server.

## 5. Ihre Rechte
Sie haben das Recht auf Auskunft, Berichtigung, Löschung, Einschränkung der Verarbeitung und Datenübertragbarkeit (Art. 15–20 DSGVO).
* **Kontakt:** Zur Geltendmachung Ihrer Rechte wenden Sie sich bitte an die oben genannte E-Mail-Adresse.
* **Beschwerderecht:** Sie haben das Recht, sich bei einer Datenschutz-Aufsichtsbehörde zu beschweren.

## 6. Sicherheit der Daten
Wir treffen technische und organisatorische Maßnahmen (z. B. Verschlüsselung, Zugriffskontrollen), um Ihre Daten vor Verlust, Missbrauch oder unbefugtem Zugriff zu schützen (Art. 32 DSGVO).

## 7. Änderungen dieser Datenschutzerklärung
Wir behalten uns vor, diese Datenschutzerklärung anzupassen. Änderungen werden an dieser Stelle veröffentlicht.
