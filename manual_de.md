📱 PiHoleMonitor – Benutzerhandbuch

Dieses Handbuch unterstützt Sie bei der Einrichtung und Nutzung der PiHoleMonitor App. PiHoleMonitor ist ein inoffizieller, moderner Client für Pi-hole®, der speziell für Android entwickelt wurde. Er ermöglicht Ihnen die komfortable Überwachung und Verwaltung Ihrer Werbefilter-Instanzen über eine native, performante Oberfläche (Jetpack Compose).

📖 Inhaltsverzeichnis

    1. Sicherheit & Datenschutz

    2. Server-Konfiguration

    3. Dashboard

    4. Management

    5. Abfrage-Logs

    6. System

    7. Einstellungen

🛡️ 1. Sicherheit & Datenschutz

Da die App Zugriff auf Ihre Netzwerk-Infrastruktur hat, steht der Schutz Ihrer Daten an oberster Stelle.

    Verschlüsselung: Sensible Daten wie Passwörter und Session-IDs werden niemals im Klartext gespeichert. Die App nutzt eine AES-GCM Verschlüsselung innerhalb des hardwaregestützten Android KeyStores.

Authentifizierung: Die Kommunikation erfolgt über das offizielle API-Verfahren mittels sicherer Session-IDs (sid) und CSRF-Tokens.

Lokalität: PiHoleMonitor ist "Offline-First". Es findet keine Datenübertragung an externe Cloud-Server des Entwicklers statt. Alle Verbindungen erfolgen direkt zwischen Ihrem Smartphone und Ihrer Pi-hole Instanz.

Biometrie: Sie können den Zugriff auf die App optional durch Ihren Fingerabdruck oder Gesichtserkennung schützen.

⚙️ 2. Server-Konfiguration

Um die App nutzen zu können, müssen Sie Ihre Pi-hole Instanz (unterstützt die moderne API v6+) hinterlegen.

    Server Name: Ein frei wählbarer Name zur Identifikation (z. B. "Heimnetzwerk").

Domain / IP: Die Adresse Ihrer Instanz (z. B. 192.168.178.5 oder ein lokaler Hostname).

Port: Der Port der Web-Oberfläche (Standard: 80 für HTTP oder 443 für HTTPS).

Sub Route (optional):

    💡 Nginx / Reverse-Proxy: Falls Ihr Pi-hole über einen Pfad wie meinedomain.de/pihole erreichbar ist, tragen Sie hier /pihole ein. Die App ergänzt intern automatisch den notwendigen Pfad /api/.

Passwort: Ihr Pi-hole Web-Passwort.

Connection Type: Wahl zwischen HTTPS (empfohlen) oder HTTP.

Verbindung prüfen & Speichern

    Check Connection: Führt einen Testaufruf aus, um die Erreichbarkeit und die Korrektheit des Passworts sofort zu validieren.

Speichern (Disketten-Icon): Übernimmt die Daten in den verschlüsselten Speicher. Bei der ersten Einrichtung wird dieser Server automatisch als aktiver Server markiert.

📊 3. Dashboard

Das Dashboard ist das Herzstück der App und bietet eine Echtzeit-Übersicht Ihres Netzwerks.

    24h-Historie: Verfolgen Sie die DNS-Abfragen der letzten 24 Stunden in einem detaillierten Graphen.

Gesamtstatistiken: Übersicht über die gesamte Anzahl der Anfragen, wie viele davon blockiert wurden und die aktuelle Block-Rate in Prozent.

Client-Ranking: Identifizieren Sie schnell, welche Geräte (Clients) in Ihrem Netzwerk die meisten Anfragen stellen oder am häufigsten blockiert werden.

🗂️ 4. Management

Verwalten Sie die Konfiguration Ihrer Pi-hole Instanz direkt in der App.

    Clients: Anzeigen, Erstellen und Bearbeiten von Netzwerk-Clients und deren Zuordnung.

Ad-Listen (Gravity): Verwalten Sie Ihre Blocklisten-Quellen zur Filterung von Werbung.

Domains: Pflegen Sie Ihre persönlichen Whitelists und Blacklists (exakt oder via Regex).

Gruppen: Organisieren Sie Clients und Listen in logischen Gruppen für unterschiedliche Filter-Profile.

🔍 5. Abfrage-Logs

Detaillierte Einsicht in den DNS-Verkehr Ihres Netzwerks.

    Echtzeit-Ansicht: Sehen Sie sofort, welche Domains gerade angefragt werden.

Status-Filter: Filtern Sie gezielt nach erlaubten (OK), blockierten (Gravity/Blacklist) oder aus dem Cache beantworteten Anfragen.

Suche & Filter: Suchen Sie nach spezifischen Client-IPs oder Domain-Namen, um verdächtiges Verhalten zu identifizieren.

💻 6. System

Hier finden Sie technische Details zum Host-System und zur Netzwerkumgebung.

    Host-Status: Überwachung von CPU-Last, RAM-Verbrauch und Systemtemperatur des Host-Systems.

Netzwerk & DHCP: Einblick in die Netzwerktabelle (ARP) und Verwaltung von aktiven DHCP-Leases.

Verfügbare Aktionen:

    FTL Restart: Startet den DNS-Dienst Ihrer Instanz neu.

Gravity Update: Löst eine Aktualisierung der Blocklisten aus.

Flush Logs/ARP: Bereinigt die Protokolle oder leert die Netzwerktabelle.

    [!CAUTION] Warnhinweis: Das Ausführen von System-Aktionen wie der Neustart von FTL oder ein Gravity-Update führt zu einer kurzzeitigen Unterbrechung der DNS-Auflösung (Internet-Unterbrechung) für alle Geräte in Ihrem Netzwerk.

    Flush Logs & ARP: Diese Aktion löscht die kompletten Abfrage-Logs unwiderruflich und leert die Liste bekannter Netzwerkgeräte im System.

🛠️ 7. Einstellungen

Personalisieren Sie den PiHoleMonitor an Ihre persönlichen Vorlieben.

    Design & Sprache: Wählen Sie zwischen manuellem oder systembasiertem Dark/Light Mode und stellen Sie die gewünschte Sprache ein.

Benachrichtigungen: Konfiguration von System-Meldungen und Warnungen.

Widgets: Verwalten Sie die Farben und Transparenz für Ihre Homescreen-Widgets.

Wartung & Support: Aktivieren Sie optionale Absturzberichte zur App-Verbesserung oder nutzen Sie den Log-Rekorder zur Fehlersuche.
