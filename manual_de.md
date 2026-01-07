# 📱 PiHoleMonitor – Benutzerhandbuch

Dieses Handbuch unterstützt Sie bei der Einrichtung und Nutzung der PiHoleMonitor App.

---

## ⚙️ 1. Server-Konfiguration

Um eine Verbindung herzustellen, müssen Sie Ihre Pi-hole Instanz im Bereich "Add New Server" konfigurieren.

* **Server Name**: Name zur Identifikation in der App.
* **Domain / IP**: Die Netzwerkadresse Ihrer Instanz (z. B. `192.168.178.5`).
* **Port**: Der Port der Web-Oberfläche (Standard: `80` oder `443`).
* **Sub Route (optional)**:
    > 💡 **Nginx / Reverse-Proxy**: Wenn Ihr Pi-hole unter `domain.de/pihole` erreichbar ist, tragen Sie hier `/pihole` ein. Die App ergänzt intern automatisch den Pfad `/api/`.
* **Passwort**: Ihr Pi-hole Web-Passwort.
* **Connection Type**: Wählen Sie zwischen **HTTPS** oder **HTTP**.

![Screenshot Server Setup](screenshots/new_server.jpg)

---

## 🛠️ 2. System-Tools & Management

Die App erlaubt die Steuerung zentraler Pi-hole Funktionen über die API.

### Verfügbare Aktionen:
* **FTL Restart**: Startet den DNS-Dienst neu.
* **Gravity Update**: Aktualisiert Ihre Adlisten.
* **Flush Logs/ARP**: Bereinigt Log-Dateien oder den Netzwerk-Cache.

> [!CAUTION]
> **Warnhinweis**: Das Ausführen von System-Aktionen wie der Neustart von FTL oder ein Gravity-Update führt zu einer kurzzeitigen Unterbrechung der DNS-Auflösung in Ihrem gesamten Netzwerk.

---

## 🛡️ 3. Sicherheit & Datenschutz

* **Verschlüsselung**: Passwörter werden niemals im Klartext gespeichert. Die App nutzt AES-GCM Verschlüsselung.
* **Sitzungen**: Die Authentifizierung erfolgt über sichere Session-IDs (`sid`).
* **Lokalität**: Es findet keine Datenübertragung an externe Server des Entwicklers statt.
