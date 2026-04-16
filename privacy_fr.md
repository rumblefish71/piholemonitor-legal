# Politique de Confidentialité pour PiHoleMonitor

Dernière mise à jour : 16 avril 2026

## 1. Informations Générales
Cette politique de confidentialité vous informe sur la nature, l'étendue et la finalité de la collecte et de l'utilisation des données personnelles lors de l'utilisation de l'application "PiHoleMonitor".

Responsable :
Christian Jurtz
Haubachstr. 48
16540 Hohen Neuendorf
Allemagne
mountainfields@jurtz.de

## 2. Principe Fondamental
L'application est conçue pour surveiller votre **propre** instance Pi-hole®.
**Nous n'avons pas accès à vos données Pi-hole.**
La communication a lieu exclusivement et directement entre votre appareil (smartphone) et votre serveur Pi-hole. Vos identifiants (jetons API, mots de passe) sont stockés de manière cryptée sur votre appareil et ne le quittent pas.

## 3. Autorisations et Traitement des Données

### 3.1 Accès Réseau (INTERNET)
L'application nécessite un accès réseau pour se connecter à votre serveur Pi-hole configuré.
* **Données :** Adresse IP, noms d'hôte, jeton API.
* **Traitement :** Les données sont traitées exclusivement localement et ne nous sont pas envoyées, ni à des tiers.
* **Base Légale :** Intérêt légitime (Art. 6 par. 1 lit. f RGPD) pour le fonctionnement de l'application.

### 3.2 Verrouillage de l'App & Biométrie (USE_BIOMETRIC)
Vous pouvez optionnellement sécuriser l'accès à l'application. Cela utilise les méthodes de sécurité configurées sur votre appareil (ex: empreinte digitale, reconnaissance faciale sécurisée ou PIN/schéma).
* **Traitement :** La vérification est effectuée exclusivement localement par le système d'exploitation Android (Android Biometric API).
* **Confidentialité :** L'application n'a mai accès à vos données biométriques brutes (comme les images d'empreintes) ou à votre PIN. Nous recevons uniquement une confirmation ("Succès" ou "Erreur") du système. Les données biométriques ne quittent jamais le stockage matériel sécurisé de votre appareil (Art. 9 RGPD).

### 3.3 Rapport d'Erreur (Crash Reporting)
Pour améliorer la stabilité, vous pouvez choisir d'envoyer un rapport d'erreur en cas de plantage.
* **Type :** Opt-In (désactivé par défaut). Vous devez consentir explicitement dans les paramètres ("Crash Reporting Consent").
* **Destinataire :** Les données sont envoyées à notre propre serveur (`https://www.mountainfields.de/crash`). **Aucun** partage avec des tiers.
* **Données Collectées :**
    * Type d'appareil, modèle, fabricant, version d'Android.
    * Utilisation de la mémoire (RAM) au moment du plantage.
    * Rapport technique d'erreur (Stacktrace).
    * Extrait du journal système (Logcat, max. 200 lignes).
* **Conservation :** Les rapports sont stockés sur notre serveur jusqu'à 30 jours pour analyse, puis supprimés. Sur l'appareil, ils sont supprimés immédiatement après transmission.
* **Base Légale :** Votre consentement (Art. 6 par. 1 lit. a RGPD). Vous pouvez le révoquer à tout moment.

### 3.4 Débogage Avancé (Session Recording)
Vous pouvez démarrer manuellement un enregistrement détaillé des erreurs ("Session Recording").
* **Type :** Manuel (Opt-In).
* **Traitement :** Le fichier (`debug_reports`) est généré **exclusivement localement**. **Il n'y a pas d'envoi automatique.** Vous décidez seul du partage de ce fichier.
* **Conservation :**
    * Les **données brutes** sont **supprimées immédiatement** après la génération du rapport.
    * Le rapport est **mis en mémoire tampon pour l'export** et est **automatiquement supprimé de l'appareil après 1 heure max**.
* **Contenu du Rapport :**
    * Version de l'app, type de build, hash Git.
    * Infos réseau (WiFi/Cellulaire/VPN).
    * **Données Masquées :** Domaine Pi-hole, **adresses IP masquées** (ex: `192.168.xxx.xxx`), adresses MAC et identifiants de session (SID).
    * État du certificat SSL.
    * Journal des activités de l'application.
* **Note :** Malgré le masquage, ce rapport peut contenir des **métadonnées techniques**. **Ne le partagez qu'avec des personnes de confiance.**

## 4. Stockage des Données Sensibles
Les jetons API et mots de passe sont stockés dans l'**Android Keystore System** et dans les `SharedPreferences` (cryptés en AES-256 GCM).

## 5. Vos Droits
Vous disposez d'un droit d'accès, de rectification, d'effacement, de limitation du traitement et de portabilité des données (Art. 15–20 RGPD).
* **Contact :** Pour exercer vos droits, contactez l'adresse e-mail ci-dessus.
* **Réclamation :** Vous avez le droit d'introduire une réclamation auprès d'une autorité de contrôle.

## 6. Sécurité des Données
Nous mettons en œuvre des mesures techniques et organisationnelles (ex: cryptage) pour protéger vos données (Art. 32 RGPD).

## 7. Modifications
Nous nous réservons le droit de mettre à jour cette politique. Les changements seront publiés ici.