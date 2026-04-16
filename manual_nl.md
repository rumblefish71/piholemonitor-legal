# 📱 PiHoleMonitor – Gebruikershandleiding

Deze handleiding helpt u bij het instellen en gebruiken van de **PiHoleMonitor** app. PiHoleMonitor is een onofficiële client voor **Pi-hole®**, waarmee u uw advertentiefilter-instanties eenvoudig kunt monitoren en beheren via een native interface gebouwd met Jetpack Compose.

---

### 📖 Inhoudsopgave
* [1. Veiligheid & Privacy](#1-veiligheid--privacy)
* [2. Serverconfiguratie](#2-serverconfiguratie)
* [3. Dashboard](#3-dashboard)
* [4. Beheer](#4-beheer)
* [5. Query-logs](#5-query-logs)
* [6. Systeem](#6-systeem)
* [7. Instellingen](#7-instellingen)

---

## 🛡️ 1. Veiligheid & Privacy
Omdat de app communiceert met uw netwerkinfrastructuur, is gegevensbeveiliging onze hoogste prioriteit.

* **Versleuteling**: Gevoelige gegevens zoals wachtwoorden en sessie-ID's worden nooit als platte tekst opgeslagen. De app maakt gebruik van **AES-GCM versleuteling** binnen de hardware-ondersteunde **Android KeyStore**.
* **Authenticatie**: Communicatie verloopt via het officiële API-protocol met gebruik van beveiligde sessie-ID's (`sid`) en CSRF-tokens.
* **Locatie**: PiHoleMonitor is "Offline-First". **Er worden geen gegevens verzonden** naar externe cloudservers van de ontwikkelaar. Alle verbindingen vinden rechtstreeks plaats tussen uw smartphone en uw Pi-hole instantie.
* **Biometrie**: U kunt de toegang tot de app optioneel beveiligen met uw vingerafdruk, gezichtsherkenning of PIN.

---

## ⚙️ 2. Serverconfiguratie
Om de app te gebruiken, moet u uw Pi-hole instantie registreren (API v6+ ondersteund).

* **Servernaam**: Een vrij te definiëren naam voor identificatie binnen de app.
* **Domein / IP**: Het adres van uw instantie (bijv. `192.168.178.5`).
* **Poort**: De webinterface-poort (Standaard: `80` voor HTTP of `443` for HTTPS).
* **Subroute (Optioneel)**:
    > 💡 **Nginx / Reverse-Proxy**: Als uw Pi-hole bereikbaar is via een subpad zoals `domein.com/pihole`, voer hier dan `/pihole` in. De app voegt intern automatisch het vereiste `/api/` achtervoegsel toe.
* **Wachtwoord**: Het wachtwoord van uw Pi-hole webinterface.
* **Verbindingstype**: Kies tussen **HTTPS** (aanbevolen) of **HTTP**.

### Verbindingstest & Opslaan
* **Verbinding controleren**: Voert een testverzoek uit om de bereikbaarheid en de juistheid van het wachtwoord te valideren.
* **Opslaan (Schijf-icoon)**: Slaat de gegevens op in de versleutelde opslag. Bij de eerste installatie wordt deze server automatisch als de actieve instantie gemarkeerd.

---

## 📊 3. Dashboard
Het Dashboard biedt een real-time overzicht van de gezondheid van uw netwerk.

* **24-uurs geschiedenis**: Volg DNS-query's van de afgelopen 24 uur in een gedetailleerde grafiek.
* **Totale statistieken**: Samenvatting van het totaal aantal query's, geblokkeerde verzoeken en het huidige blokkeringspercentage.
* **Cliënt-ranking**: Identificeer de meest actieve cliënten in uw netwerk.

---

## 🗂️ 4. Beheer
Beheer uw Pi-hole configuratie rechtstreeks in de app.

* **Cliënten**: Bekijk, maak en bewerk netwerkcliënten.
* **Ad-lijsten (Gravity)**: Beheer de bronnen van uw blokkeerlijsten die worden gebruikt voor het filteren van advertenties.
* **Domeinen**: Beheer whitelists en blacklists (exact of op basis van regex).
* **Groepen**: Organiseer cliënten en lijsten in logische groepen.

---

## 🔍 5. Query-logs
Diepgaand inzicht in het DNS-verkeer van uw netwerk.

* **Statusfilter**: Filter specifiek op toegestane, geblokkeerde of gecachte query's.
* **Zoeken**: Zoek naar specifieke domeinen of IP-adressen van cliënten.

---

## 💻 6. Systeem
Monitoring van hardware en netwerkomgeving.

* **Host Systeem**: Toont hostinformatie, CPU-belasting, RAM-gebruik en de status van het `pihole-FTL` proces.
* **Pi-hole**: Schakel het DNS-filter in/uit, monitor het gebruik van de DNS-cache, voer Pi-hole acties uit en bekijk systeemmeldingen.
* **Netwerk**: Gedetailleerd overzicht van gateways, interfaces en routes.
* **DHCP**: Beheer van actieve DHCP-leases.

### Beschikbare acties:
* **FTL Herstarten**: Herstart de DNS-service op uw instantie.
* **Gravity Update**: Start een update van de blokkeerlijsten.
* **Logs/ARP wissen**: Wast de DNS-querylogs of wist de netwerktabel.

> [!CAUTION]
> **Waarschuwing**: Het uitvoeren van Pi-hole acties zoals het herstarten van FTL of het bijwerken van Gravity veroorzaak een korte onderbreking van de DNS-resolutie voor uw gehele netwerk.
> 
> **Logs & ARP wissen**: Deze acties verwijderen permanent alle query-logs en wissen de lijst met bekende netwerkapparaten (netwerktabel).

---

## 🛠️ 7. Instellingen
Personaliseer uw PiHoleMonitor ervaring.

* **Thema & Taal**: Schakel tussen Donkere/Lichte modus en selecteer uw voorkeurstaal.
* **Meldingen**: Configureer waarschuwingen op systeemniveau.
* **Widgets**: Pas het uiterlijk van uw homescreen-widgets aan.
* **Beveiliging**: Configureer instellingen voor biometrische login.
* **Onderhoud**: Schakel crashrapportage in of uit.
* **Debug Log Recorder**: Gebruik de logrecorder om te helpen bij het oplossen van problemen.