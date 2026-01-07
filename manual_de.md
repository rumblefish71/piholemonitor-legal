# 📱 PiHoleMonitor – Handbuch

Diese Anleitung führt Sie durch die Funktionen und die Einrichtung der PiHoleMonitor App.

## 1. Funktionsumfang
* **Dashboard**: Echtzeit-Statistiken über geblockte Anfragen, Queries und Clients.
* **Management**: Verwaltung von Gruppen, Clients und Adlisten direkt in der App.
* **Query Log**: Detaillierte Ansicht der DNS-Anfragen mit Filteroptionen.
* **System-Tools**: FTL-Logs einsehen, FTL neu starten oder Gravity-Update anstoßen.

## 2. Konfiguration (Server hinzufügen)
Um die App zu nutzen, müssen Sie Ihre Pi-hole Instanz hinterlegen:
* **Server Name**: Name zur Identifikation (z. B. "Home").
* **Domain / IP**: Adresse Ihres Pi-hole (z. B. `192.168.178.2`).
* **Port**: Standardmäßig `80` oder `443`.
* **Sub Route (optional)**:
    * 💡 **Nginx Hinweis**: Falls Ihr Pi-hole unter `domain.de/pihole` erreichbar ist, tragen Sie hier `/pihole` ein.
* **Passwort**: Ihr Pi-hole Web-Passwort.

## 3. Sicherheit
Ihre Daten (Passwort, Session-ID) werden niemals im Klartext gespeichert. Die App nutzt den **Android KeyStore** mit **AES-GCM Verschlüsselung**.

## 4. Fehlerbehebung
* **Verbindung fehlgeschlagen**: Prüfen Sie, ob Sie im selben Netzwerk sind oder VPN nutzen.
* **SSL-Fehler**: Bei selbstsignierten Zertifikaten muss in den App-Einstellungen "Accept Untrusted" aktiviert werden.
