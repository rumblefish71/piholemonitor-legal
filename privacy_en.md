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
Communication takes place exclusively and directly between your device (smartphone) and your Pi-hole server. Your credentials (API tokens, passwords) are stored encrypted on your device and do not leave it.

## 3. Permissions and Data Processing

### 3.1 Network Access (INTERNET)
The app requires network access to connect to your configured Pi-hole server.
* **Data:** IP address, hostnames, API token.
* **Processing:** Data is processed exclusively locally and is not sent to us or third parties.
* **Legal Basis:** Legitimate interest (Art. 6 para. 1 lit. f GDPR) in the functionality of the app.

### 3.2 Biometric Authentication (USE_BIOMETRIC)
You can optionally secure the app using fingerprint or face unlock.
* **Processing:** Verification is handled solely by the Android operating system. The app only receives a "Success" or "Error" signal. Biometric data never leaves your device's secure hardware (Art. 9 GDPR).

### 3.3 Crash Reporting
To improve app stability, you can choose to send an error report in the event of a crash.
* **Type:** Opt-In (Disabled by default). You must explicitly consent in the settings ("Crash Reporting Consent").
* **Recipient:** Data is sent to our own server (`https://www.mountainfields.de/crash`). **No** sharing with third-party providers.
* **Data Collected:**
    * Device type, model, manufacturer, Android version.
    * Memory usage (RAM) at the time of the crash.
    * Technical error report (Stacktrace).
    * Excerpt of the system log (Logcat, max. 200 lines).
* **Retention:** Reports are stored on our server for up to 30 days for error analysis and then deleted. On the device, they are deleted immediately after successful transmission.
* **Legal Basis:** Your consent (Art. 6 para. 1 lit. a GDPR). You can revoke this at any time in the app settings.

### 3.4 Advanced Debugging (Session Recording)
You can manually start a detailed error recording ("Session Recording").
* **Type:** Manual (Opt-In). Recording only starts via your specific interaction.
* **Processing:** The file (`debug_reports`) is generated **exclusively locally** on your device. **There is no automatic upload.** You decide entirely on your own whether to share this file.
* **Retention:**
    * The **raw data** of the recording is **deleted immediately** after the report is generated.
    * The generated report is **temporarily buffered for export** and is **automatically deleted from the device after max. 1 hour**.
* **Report Content:**
    * App version, build type, Git hash.
    * Network information (WiFi/Cellular/VPN status).
    * **Masked Data:** Configured Pi-hole domain, **obfuscated IP addresses** (e.g., `192.168.xxx.xxx`), MAC addresses, and Session IDs (SIDs).
    * SSL certificate status.
    * Log of app activities during the recording session.
* **Note:** Despite masking, this report may contain **technical metadata**. **Only share it with trusted persons.** You bear the sole responsibility for sharing this file with third parties.

## 4. Storage of Sensitive Data
API tokens and passwords are stored in the **Android Keystore System** and in `SharedPreferences` (AES-256 GCM encrypted). This data does not leave your device, except to authenticate against your own server.

## 5. Your Rights
You have the right to access, rectification, erasure, restriction of processing, and data portability (Art. 15–20 GDPR).
* **Contact:** To exercise your rights, please contact the email address provided above.
* **Right to lodge a complaint:** You have the right to lodge a complaint with a supervisory authority.

## 6. Data Security
We implement technical and organizational measures (e.g., encryption, access controls) to protect your data against loss, misuse, or unauthorized access (Art. 32 GDPR).

## 7. Changes to this Privacy Policy
We reserve the right to update this privacy policy. Changes will be published here.
