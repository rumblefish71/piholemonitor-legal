# 📱 PiHoleMonitor – Benutzerhandbuch

Dieses Handbuch unterstützt Sie bei der Einrichtung und Nutzung der **PiHoleMonitor** App. PiHoleMonitor ist ein inoffizieller Client für **Pi-hole®**. Die App ermöglicht Ihnen die komfortable Überwachung und Verwaltung Ihrer Werbefilter-Instanzen über eine native Oberfläche auf Basis von Jetpack Compose.

---

### 📖 Inhaltsverzeichnis
* [1. Sicherheit & Datenschutz](#1-sicherheit--datenschutz)
* [2. Server-Konfiguration](#2-server-konfiguration)
* [3. Dashboard](#3-dashboard)
* [4. Management](#4-management)
* [5. Abfrage-Logs](#5-abfrage-logs)
* [6. System](#6-system)
* [7. Einstellungen](#7-einstellungen)

---

## 🛡️ 1. Sicherheit & Datenschutz
Da die App Zugriff auf Ihre Netzwerk-Infrastruktur hat, steht der Schutz Ihrer Daten an oberster Stelle.

* **Verschlüsselung**: Sensible Daten wie Passwörter und Session-IDs werden niemals im Klartext gespeichert. Die App nutzt eine **AES-GCM Verschlüsselung** innerhalb des hardwaregestützten **Android KeyStores**.
* **Authentifizierung**: Die Kommunikation erfolgt über das offizielle API-Verfahren mittels sicherer Session-IDs (`sid`) und CSRF-Tokens.
* **Lokalität**: PiHoleMonitor ist "Offline-First". Es findet **keine Datenübertragung** an externe Cloud-Server des Entwicklers statt. Alle Verbindungen erfolgen direkt zwischen Ihrem Smartphone und Ihrer Pi-hole Instanz.
* **Biometrie**: Sie können den Zugriff auf die App optional durch Ihren Fingerabdruck, Gesichtserkennung oder PIN schützen.

---

## ⚙️ 2. Server-Konfiguration
Um die App nutzen zu können, müssen Sie Ihre Pi-hole Instanz (unterstützt API v6+) hinterlegen.

* **Server Name**: Ein frei wählbarer Name zur Identifikation in der App.
* **Domain / IP**: Die Adresse Ihrer Instanz (z. B. `192.168.178.5`).
* **Port**: Der Port der Web-Oberfläche (Standard: `80` für HTTP oder `443` für HTTPS).
* **Sub Route (optional)**:
    > 💡 **Nginx / Reverse-Proxy**: Falls Ihr Pi-hole über einen Pfad wie `domain.de/pihole` erreichbar ist, tragen Sie hier `/pihole` ein. Die App ergänzt intern automatisch den notwendigen Pfad `/api/`.
* **Passwort**: Ihr Pi-hole Web-Passwort.
* **Connection Type**: Wahl zwischen **HTTPS** (empfohlen) oder **HTTP**.

### Verbindung prüfen & Speichern
* **Check Connection**: Führt einen Testaufruf aus, um die Erreichbarkeit und die Korrektheit des Passworts via `authenticateWithSid` zu validieren.
* **Speichern (Disketten-Icon)**: Übernimmt die Daten in den verschlüsselten Speicher. Bei der ersten Einrichtung wird dieser Server automatisch als aktiver Server markiert.

![Screenshot Server Setup](screenshots/new_server.jpg)

---

## 📊 3. Dashboard
Das Dashboard bietet eine Echtzeit-Übersicht über den Zustand Ihres Netzwerks.

* **24h-Historie**: Verfolgen Sie die DNS-Abfragen der letzten 24 Stunden in einem detaillierten Graphen.
* **Gesamtstatistiken**: Übersicht über die gesamte Anzahl der Anfragen, blockierte Anfragen und die aktuelle Block-Rate.
* **Client-Ranking**: Identifizieren Sie die aktivsten Clients in Ihrem Netzwerk.

---

## 🗂️ 4. Management
Verwalten Sie Ihre Pi-hole Konfiguration direkt in der App.

* **Clients**: Anzeigen, Erstellen und Bearbeiten von Netzwerk-Clients.
* **Ad-Listen (Gravity)**: Verwalten Sie Ihre Blocklisten-Quellen zur Filterung von Werbung.
* **Domains**: Pflegen Sie Whitelists und Blacklists (exakt oder via Regex).
* **Gruppen**: Organisieren Sie Clients und Listen in logischen Gruppen.

---

## 🔍 5. Abfrage-Logs
Detaillierte Einsicht in den DNS-Verkehr Ihres Netzwerks.

* **Status-Filter**: Filtern Sie gezielt nach erlaubten, blockierten oder aus dem Cache beantworteten Anfragen.
* **Suche**: Suchen Sie nach spezifischen Domains oder Client-IPs.

---

## 💻 6. System
Überwachung der Hardware und Netzwerkumgebung.

* **Host-System**: Anzeige von Host-Informationen, CPU-Last, RAM-Verbrauch und pihole-FTL Prozess.
* **Pi-hole**: Aktivierung oder Deaktivierung des DNS-Filters, Auslastung des DNS-Caches, Ausführung von Pi-hole Aktionen, Benachrichtigungen von Pi-hole
* **Netzwerk**: Detailierte Übersicht der Gateways, Schnittstellen und Routen.
* **DHCP**: Verwaltung von aktiven DHCP-Leases.

### Verfügbare Aktionen:
* **FTL Restart**: Startet den DNS-Dienst Ihrer Instanz neu.
* **Gravity Update**: Löst eine Aktualisierung der Blocklisten aus.
* **Flush Logs/ARP**: Bereinigt Protokolle oder leert die Netzwerktabelle.

> [!CAUTION]
> **Warnhinweis**: Das Ausführen von Pi-hole Aktionen wie der Neustart von FTL oder ein Gravity-Update führt zu einer kurzzeitigen Unterbrechung der DNS-Auflösung für Ihr gesamtes Netzwerk.
> 
> **Flush Logs & ARP**: Diese Aktion löscht die kompletten Abfrage-Logs unwiderruflich und leert die Liste bekannter Netzwerkgeräte (Netzwerktabelle).

---

## 🛠️ 7. Einstellungen
Personalisieren Sie den PiHoleMonitor.

* **Design & Sprache**: Einstellungen für Dark/Light Mode und die Systemsprache.
* **Benachrichtigungen**: Konfiguration von System-Meldungen.
* **Widgets**: Verwalten Sie das Erscheinungsbild Ihrer Homescreen-Widgets.
* **Sicherheit**: Konfiguration des biometrischen Logins.
* **Wartung**: Aktivierung oder Deaktivierung von Absturzberichten
* **Debug-Log-Rekorder**: Nutzung des Log-Rekorders bei Problemen 
