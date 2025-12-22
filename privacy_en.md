# Privacy Policy for PiHoleMonitor

Last updated: December 22, 2025

## 1. General Information
This privacy policy informs you about the nature, scope, and purpose of the collection and use of personal data when using the app "PiHoleMonitor".

Responsible:
Christian Jurtz
Haubachstr.48
16540 Hohen Neuendorf
Germany
support@mountainfields.de

## 2. Basic Principle
The app is designed to monitor your **own** Pi-hole® instance.
**We do not have access to your Pi-hole data.**
Communication takes place exclusively and directly between your device and your Pi-hole server. Your credentials (API tokens, passwords) are stored encrypted on your device.

## 3. Permissions and Data Processing

### 3.1 Network Access (INTERNET)
The app requires network access to connect to your configured Pi-hole server.
* **Data:** IP address, hostnames, API token.
* **Processing:** Data is processed locally and is not sent to us or third parties.

### 3.2 Biometric Authentication (USE_BIOMETRIC)
You can optionally secure the app using fingerprint or face unlock.
* **Processing:** Verification is handled solely by the Android operating system. The app only receives a "Success" or "Error" signal. Biometric data never leaves your device's secure hardware.

### 3.3 Crash Reporting (App Stability)
To improve app stability, we offer an option to send error reports in the event of a crash.
* **Type:** Opt-In (Disabled by default). You must explicitly consent in the settings ("Crash Reporting Consent").
* **Recipient:** Data is sent to our own server (`https://www.mountainfields.de/crash`). No data is shared with third-party trackers like Google Firebase or Facebook.
* **Data collected:** Device type, model, Android version, RAM usage, the technical stack trace, and a short excerpt of the system log (max. 200 lines) at the time of the crash.
* **Retention:** Reports are buffered locally and deleted after successful transmission.

### 3.4 Advanced Debugging (Session Recording)
You have the option to manually start a detailed error recording ("Session Recording") to analyze complex issues.
* **Type:** Manual (Opt-In). Recording only starts via your interaction and ends when you stop it.
* **Processing:** The generated report file is created **locally** on your device. There is **no automatic upload**. You decide if and with whom (e.g., via Email) you share this file.
* **Report Content:** App version, network status (WiFi/VPN), masked Pi-hole domain/port, SSL certificate status, and a full log of app activities during the recording session.

## 4. Storage of Sensitive Data
The app stores API tokens and passwords in the **Android Keystore System** and `SharedPreferences` (encrypted). This data does not leave your device, except to authenticate against your own server.

## 5. Your Rights
You have the right to access, rectify, and delete your data. Since we do not store user data on our servers (other than anonymous crash reports if consented), we cannot provide information about your usage – this data resides solely on your device and your Pi-hole server.
