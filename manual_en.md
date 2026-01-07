# 📱 PiHoleMonitor – Manual

This guide covers the features and setup of the PiHoleMonitor app.

## 1. Features
* **Dashboard**: Real-time statistics on blocked queries, total queries, and active clients.
* **Management**: Manage groups, clients, and adlists directly from your phone.
* **Query Log**: Detailed view of DNS requests with advanced filtering.
* **System Tools**: View FTL logs, restart FTL, or trigger a Gravity update.

## 2. Configuration (Adding a Server)
To start using the app, you need to add your Pi-hole instance:
* **Server Name**: Any name for identification (e.g., "Home").
* **Domain / IP**: Your Pi-hole's address (e.g., `192.168.1.5`).
* **Port**: Default is `80` or `443`.
* **Sub Route (optional)**:
    * 💡 **Nginx Note**: If your Pi-hole is hosted under `domain.com/pihole`, enter `/pihole` here.
* **Password**: Your Pi-hole web interface password.

## 3. Security
Your sensitive data (password, session ID) is never stored in plain text. The app uses the **Android KeyStore** with **AES-GCM encryption**.

## 4. Troubleshooting
* **Connection Failed**: Ensure you are on the same network or using a VPN.
* **SSL Errors**: For self-signed certificates, enable "Accept Untrusted" in the app settings.
