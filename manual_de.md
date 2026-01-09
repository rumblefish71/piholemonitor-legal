# 📱 PiHoleMonitor – Benutzerhandbuch

Dieses Handbuch unterstützt Sie bei der Einrichtung und Nutzung der **PiHoleMonitor** App. [cite_start]PiHoleMonitor ist ein inoffizieller, moderner Client für **Pi-hole®**[cite: 3]. [cite_start]Die App ermöglicht Ihnen die komfortable Überwachung und Verwaltung Ihrer Werbefilter-Instanzen über eine native Oberfläche auf Basis von Jetpack Compose[cite: 3].

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

* [cite_start]**Verschlüsselung**: Sensible Daten wie Passwörter und Session-IDs werden niemals im Klartext gespeichert[cite: 2]. [cite_start]Die App nutzt eine **AES-GCM Verschlüsselung** [cite: 2] [cite_start]innerhalb des hardwaregestützten **Android KeyStores**[cite: 2].
* [cite_start]**Authentifizierung**: Die Kommunikation erfolgt über das offizielle API-Verfahren mittels sicherer Session-IDs (`sid`) und CSRF-Tokens[cite: 2].
* **Lokalität**: PiHoleMonitor ist "Offline-First". [cite_start]Es findet **keine Datenübertragung** an externe Cloud-Server des Entwicklers statt[cite: 2]. [cite_start]Alle Verbindungen erfolgen direkt zwischen Ihrem Smartphone und Ihrer Pi-hole Instanz[cite: 4, 8].
* [cite_start]**Biometrie**: Sie können den Zugriff auf die App optional durch Ihren Fingerabdruck oder Gesichtserkennung schützen[cite: 2].

---

## ⚙️ 2. Server-Konfiguration
[cite_start]Um die App nutzen zu können, müssen Sie Ihre Pi-hole Instanz (unterstützt die moderne API v6+) hinterlegen[cite: 2, 4].

* [cite_start]**Server Name**: Ein frei wählbarer Name zur Identifikation in der App[cite: 2].
* [cite_start]**Domain / IP**: Die Adresse Ihrer Instanz (z. B. `192.168.178.5`)[cite: 2].
* [cite_start]**Port**: Der Port der Web-Oberfläche (Standard: `80` für HTTP oder `443` für HTTPS)[cite: 2, 4].
* **Sub Route (optional)**:
    > [cite_start]💡 **Nginx / Reverse-Proxy**: Falls Ihr Pi-hole über einen Pfad wie `domain.de/pihole` erreichbar ist, tragen Sie hier `/pihole` ein[cite: 2, 8]. [cite_start]Die App ergänzt intern automatisch den notwendigen Pfad `/api/`[cite: 4].
* [cite_start]**Passwort**: Ihr Pi-hole Web-Passwort[cite: 2].
* [cite_start]**Connection Type**: Wahl zwischen **HTTPS** (empfohlen) oder **HTTP**[cite: 2, 4].

### Verbindung prüfen & Speichern
* [cite_start]**Check Connection**: Führt einen Testaufruf aus, um die Erreichbarkeit und die Korrektheit des Passworts via `authenticateWithSid` zu validieren[cite: 2].
* [cite_start]**Speichern (Disketten-Icon)**: Übernimmt die Daten in den verschlüsselten Speicher[cite: 2]. [cite_start]Bei der ersten Einrichtung wird dieser Server automatisch als aktiver Server markiert[cite: 2].

![Screenshot Server Setup](docs/screenshots/grafik.jpg)

---

## 📊 3. Dashboard
[cite_start]Das Dashboard bietet eine Echtzeit-Übersicht über den Zustand Ihres Netzwerks[cite: 1].

* [cite_start]**24h-Historie**: Verfolgen Sie die DNS-Abfragen der letzten 24 Stunden in einem detaillierten Graphen[cite: 1].
* [cite_start]**Gesamtstatistiken**: Übersicht über die gesamte Anzahl der Anfragen, blockierte Anfragen und die aktuelle Block-Rate[cite: 1].
* [cite_start]**Client-Ranking**: Identifizieren Sie die aktivsten Clients in Ihrem Netzwerk[cite: 1].

---

## 🗂️ 4. Management
[cite_start]Verwalten Sie Ihre Pi-hole Konfiguration direkt in der App[cite: 1, 3].

* [cite_start]**Clients**: Anzeigen, Erstellen und Bearbeiten von Netzwerk-Clients[cite: 1].
* **Ad-Listen (Gravity)**: Verwalten Sie Ihre Blocklisten-Quellen zur Filterung von Werbung.
* [cite_start]**Domains**: Pflegen Sie Whitelists und Blacklists (exakt oder via Regex)[cite: 1].
* [cite_start]**Gruppen**: Organisieren Sie Clients und Listen in logischen Gruppen[cite: 1].

---

## 🔍 5. Abfrage-Logs
[cite_start]Detaillierte Einsicht in den DNS-Verkehr Ihres Netzwerks[cite: 1].

* [cite_start]**Status-Filter**: Filtern Sie gezielt nach erlaubten, blockierten oder aus dem Cache beantworteten Anfragen[cite: 3].
* **Suche**: Suchen Sie nach spezifischen Domains oder Client-IPs.

---

## 💻 6. System
[cite_start]Überwachung der Hardware und Netzwerkumgebung[cite: 1].

* [cite_start]**Host-System**: Anzeige von CPU-Last, RAM-Verbrauch und Systemtemperatur[cite: 1].
* [cite_start]**DHCP**: Verwaltung von aktiven DHCP-Leases[cite: 1].

### Verfügbare Aktionen:
* **FTL Restart**: Startet den DNS-Dienst Ihrer Instanz neu.
* **Gravity Update**: Löst eine Aktualisierung der Blocklisten aus.
* **Flush Logs/ARP**: Bereinigt Protokolle oder leert die Netzwerktabelle.

> [!CAUTION]
> **Warnhinweis**: Das Ausführen von System-Aktionen wie der Neustart von FTL oder ein Gravity-Update führt zu einer kurzzeitigen Unterbrechung der DNS-Auflösung für Ihr gesamtes Netzwerk.
> 
> **Flush Logs & ARP**: Diese Aktion löscht die kompletten Abfrage-Logs unwiderruflich und leert die Liste bekannter Netzwerkgeräte (Netzwerktabelle).

---

## 🛠️ 7. Einstellungen
[cite_start]Personalisieren Sie den PiHoleMonitor[cite: 1, 3].

* [cite_start]**Design & Sprache**: Einstellungen für Dark/Light Mode und die Systemsprache[cite: 1, 2].
* [cite_start]**Benachrichtigungen**: Konfiguration von System-Meldungen[cite: 1].
* [cite_start]**Widgets**: Verwalten Sie das Erscheinungsbild Ihrer Homescreen-Widgets[cite: 2].
* [cite_start]**Sicherheit**: Konfiguration des biometrischen Logins[cite: 2].
* [cite_start]**Wartung**: Zugriff auf Absturzberichte und den Debug-Log-Rekorder[cite: 2].
