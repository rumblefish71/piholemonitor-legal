# 📱 PiHoleMonitor – User Guide & Documentation

Welcome to the official documentation hub for the **PiHoleMonitor** Android App. This application provides a modern, native interface for managing your Pi-hole® instances (v6+), built entirely with Jetpack Compose.

---

## 📖 User Guides

Please select your preferred language for the full manual:

| Language | Document |
|:--- |:--- |
| 🇬🇧 **English** | [Full App Manual](manual_en.md) |
| 🇩🇪 **Deutsch** | [Vollständiges Handbuch](manual_de.md) |
| 🇪🇸 **Español** | [Manual de Usuario](manual_es.md) |
| 🇫🇷 **Français** | [Guide de l'Utilisateur](manual_fr.md) |
| 🇮🇹 **Italiano** | [Guida Utente](manual_it.md) |
| 🇳🇱 **Nederlands** | [Gebruikershandleiding](manual_nl.md) |
| 🇵🇱 **Polski** | [Instrukcja Obsługi](manual_pl.md) |
| 🇵🇹 **Português** | [Guia do Usuário](manual_pt.md) |

---

> [!IMPORTANT]
> **Privacy & Connectivity:** PiHoleMonitor communicates directly with your Pi-hole's API. No data is stored or processed on external cloud servers owned by the developer. All credentials remain stored locally on your device.
>
> *PiHoleMonitor kommuniziert direkt mit der Pi-hole API deiner Instanz. Es werden keine Daten auf externen Cloud-Servern des Entwicklers gespeichert oder verarbeitet.*

---

### 🛠️ Project Information

* **Developer**: Christian Jurtz
* **Package ID**: `de.mountainfields.piholemonitor`
* **Technology Stack**:
    * **Language**: Kotlin 2.3.20 
    * **UI**: Jetpack Compose & Material 3 
    * **Architecture**: MVVM / Clean Architecture 
    * **Dependency Injection**: Hilt 
* **Security**: Sensitive data is stored using **AES-GCM encryption** within the hardware-backed **Android KeyStore**.

---

### ⚖️ Legal Disclaimer
*Pi-hole® is a registered trademark of Pi-hole L.L.C. This app is an independent tool and is not officially affiliated with the Pi-hole project.*
