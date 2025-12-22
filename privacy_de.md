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
Die App dient der Überwachung Ihrer **eigenen** Pi-hole® Instanz.
**Wir haben keinen Zugriff auf Ihre Pi-hole Daten.**
Die Kommunikation findet ausschließlich direkt zwischen Ihrem Endgerät (Smartphone) und Ihrem Pi-hole Server statt. Ihre Zugangsdaten (API-Token, Passwörter) werden verschlüsselt auf Ihrem Gerät gespeichert.

## 3. Zugriffsrechte und Datenverarbeitung

### 3.1 Netzwerkzugriff (INTERNET)
Die App benötigt Zugriff auf das Netzwerk, um sich mit Ihrem konfigurierten Pi-hole Server zu verbinden.
* **Daten:** IP-Adresse, Hostnamen, API-Token.
* **Verarbeitung:** Die Daten werden nur lokal verarbeitet und nicht an uns oder Dritte gesendet.

### 3.2 Biometrische Authentifizierung (USE_BIOMETRIC)
Sie können die App optional mittels Fingerabdruck oder Gesichtsscan absichern.
* **Verarbeitung:** Die Prüfung erfolgt ausschließlich durch das Android-Betriebssystem. Die App erhält lediglich die Information "Erfolg" oder "Fehler". Biometrische Daten verlassen nie den sicheren Speicher Ihres Gerätes.

### 3.3 Absturzberichte (Crash Reporting)
Um die Stabilität der App zu verbessern, bieten wir die Möglichkeit, im Falle eines App-Absturzes einen Fehlerbericht zu senden.
* **Art der Funktion:** Opt-In (Standardmäßig deaktiviert). Sie müssen in den Einstellungen ("Crash Reporting Consent") explizit zustimmen.
* **Empfänger:** Die Daten werden an unseren eigenen Server (`https://www.mountainfields.de/crash`) gesendet. Es erfolgt **keine** Weitergabe an Drittanbieter wie Google oder Facebook.
* **Gespeicherte Daten:** * Gerätetyp, Modell, Hersteller, Android-Version.
    * Speicherauslastung (RAM) zum Zeitpunkt des Absturzes.
    * Der technische Fehlerbericht (Stacktrace).
    * Ein Auszug des System-Logs (Logcat, max. 200 Zeilen) zum Zeitpunkt des Fehlers.
* **Speicherdauer:** Die Berichte werden lokal auf Ihrem Gerät zwischengespeichert und nach erfolgreicher Übertragung gelöscht.

### 3.4 Erweiterte Fehleranalyse (Debug Recording)
Sie haben die Möglichkeit, manuell eine detaillierte Fehleraufzeichnung ("Session Recording") zu starten, um komplexe Probleme zu analysieren.
* **Art der Funktion:** Manuell (Opt-In). Die Aufzeichnung startet nur durch Ihre Interaktion und endet, wenn Sie diese stoppen.
* **Verarbeitung:** Die erstellte Datei (`debug_reports`) wird **lokal** auf Ihrem Gerät generiert. Es findet **kein automatischer Upload** statt. Sie entscheiden selbst, ob und wem Sie diese Datei (z.B. per E-Mail) senden.
* **Inhalt des Berichts:**
    * App-Version, Build-Typ und Git-Hash.
    * Netzwerkinformationen (WiFi/Mobilfunk/VPN Status).
    * Konfigurierte Pi-hole Domain (teilweise maskiert) und Port.
    * Status der SSL-Zertifikate.
    * Ein vollständiges Protokoll der App-Aktivitäten während der Aufzeichnung.
* **Hinweis:** Da dieser Bericht detaillierte Protokolle enthält, teilen Sie ihn bitte nur mit vertrauenswürdigen Personen zur Fehlerbehebung.

## 4. Speicherung sensibler Daten
Die App speichert API-Tokens und Passwörter im **Android Keystore System** und in den `SharedPreferences` (verschlüsselt). Diese Daten verlassen Ihr Gerät nicht, außer zur Authentifizierung gegenüber Ihrem eigenen Server.

## 5. Ihre Rechte
Sie haben das Recht auf Auskunft, Berichtigung und Löschung Ihrer Daten. Da wir keine Nutzerdaten auf unseren Servern speichern, können wir keine Auskunft über Ihre Nutzung geben – diese Daten liegen allein auf Ihrem Gerät und Ihrem Pi-hole Server.
