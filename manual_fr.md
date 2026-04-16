# 📱 PiHoleMonitor – Guide de l'utilisateur

Ce manuel vous aide à configurer et à utiliser l'application **PiHoleMonitor**. PiHoleMonitor est un client non officiel pour **Pi-hole®**, vous permettant de surveiller et de gérer facilement vos instances de filtrage publicitaire via una interface native construite avec Jetpack Compose.

---

### 📖 Table des matières
* [1. Sécurité et confidentialité](#1-sécurité--confidentialité)
* [2. Configuration du serveur](#2-configuration-du-serveur)
* [3. Tableau de bord](#3-tableau-de-bord)
* [4. Gestion](#4-gestion)
* [5. Journaux de requêtes](#5-journaux-de-requêtes)
* [6. Système](#6-système)
* [7. Paramètres](#7-paramètres)

---

## 🛡️ 1. Sécurité et confidentialité
Puisque l'application interagit con votre infrastructure réseau, la protection des données est notre priorité absolue.

* **Chiffrement** : Les données sensibles telles que les mots de passe et les identifiants de session ne sont jamais stockées en texte clair. L'application utilise le **chiffrement AES-GCM** au sein de l'**Android KeyStore** sécurisé par le matériel.
* **Authentification** : La communication suit le protocole API officiel utilisant des identifiants de session sécurisés (`sid`) et des jetons CSRF.
* **Localité** : PiHoleMonitor est "Offline-First". **Aucune donnée n'est transmise** à des serveurs cloud externes appartenant au développeur. Toutes les connexions s'effectuent directement entre votre smartphone et votre instance Pi-hole.
* **Biométrie** : Vous pouvez optionnellement protéger l'accès à l'application en utilisant votre empreinte digitale, la reconnaissance faciale ou un code PIN.

---

## ⚙️ 2. Configuration du serveur
Pour utiliser l'application, vous devez enregistrer votre instance Pi-hole (support API v6+).

* **Nom du serveur** : Un nom librement définissable pour l'identification dans l'application.
* **Domaine / IP** : L'adresse de votre instance (ex: `192.168.178.5`).
* **Port** : Le port de l'interface web (Par défaut : `80` pour HTTP ou `443` pour HTTPS).
* **Sous-route (Optionnel)** :
    > 💡 **Nginx / Reverse-Proxy** : Si votre Pi-hole est accessible via un sous-chemin comme `domaine.com/pihole`, entrez `/pihole` ici. L'application ajoute automatiquement le suffixe `/api/` requis.
* **Mot de passe** : Le mot de passe de votre interface web Pi-hole.
* **Type de connexion** : Choisissez entre **HTTPS** (recommandé) ou **HTTP**.

### Test de connexion et sauvegarde
* **Vérifier la connexion** : Effectue une requête de test pour valider l'accessibilité et l'exactitude du mot de passe.
* **Enregistrer (Icône Disquette)** : Enregistre les données dans le stockage chiffré. Lors de la configuration initiale, ce serveur est automatiquement marqué comme instance active.

![Screenshot Server Setup](screenshots/new_server.jpg)
---

## 📊 3. Tableau de bord
Le tableau de bord fournit une vue d'ensemble en temps réel de la santé de votre réseau.

* **Historique 24h** : Suivez les requêtes DNS des dernières 24 heures via un graphique détaillé.
* **Statistiques totales** : Résumé du nombre total de requêtes, des requêtes bloquées et du taux de blocage actuel.
* **Classement des clients** : Identifiez les clients les plus actifs sur votre réseau.

---

## 🗂️ 4. Gestion
Gérez votre configuration Pi-hole directement dans l'application.

* **Clients** : Visualisez, créez et modifiez les clients réseau.
* **Listes de blocage (Gravity)** : Gérez les sources de listes de blocage utilisées pour filtrer les publicités.
* **Domaines** : Gérez les listes blanches et les listes noires (exactes ou basées sur regex).
* **Groupes** : Organisez les clients et les listes en groupes logiques.

---

## 🔍 5. Journaux de requêtes
Aperçu approfondi du trafic DNS de votre réseau.

* **Filtre d'état** : Filtrez spécifiquement les requêtes autorisées, bloquées ou mises en cache.
* **Recherche** : Recherchez des domaines spécifiques ou des adresses IP de clients.

---

## 💻 6. Système
Surveillance du matériel et de l'environnement réseau.

* **Système hôte** : Affiche les informations sur l'hôte, la charge CPU, l'utilisation de la RAM et l'état du processus `pihole-FTL`.
* **Pi-hole** : Activez/désactivez le filtre DNS, surveillez l'utilisation du cache DNS, exécutez des actions Pi-hole et consultez les notifications système.
* **Réseau** : Vue d'ensemble détaillée des passerelles, interfaces et routes.
* **DHCP** : Gestion des baux DHCP actifs.

### Actions disponibles :
* **Redémarrage FTL** : Redémarre le service DNS sur votre instance.
* **Mise à jour Gravity** : Déclenche une mise à jour des listes de blocage.
* **Flush Logs/ARP** : Efface les journaux de requêtes DNS ou vide la table réseau.

> [!CAUTION]
> **Avertissement** : L'exécution d'actions Pi-hole comme le redémarrage de FTL ou la mise à jour de Gravity entraînera une brève interruption de la résolution DNS pour l'ensemble de votre réseau.
> 
> **Flush Logs & ARP** : Ces actions suppriment définitivement tous les journaux de requêtes et effacent la liste des périphériques réseau connus.

---

## 🛠️ 7. Paramètres
Personnalisez votre expérience PiHoleMonitor.

* **Thème et langue** : Basculez entre le mode sombre/clair et sélectionnez la langue du système.
* **Notifications** : Configurez les alertes au niveau du système.
* **Widgets** : Personnalisez l'apparence des widgets de votre écran d'accueil.
* **Sécurité** : Configurez les paramètres de connexion biométrique.
* **Maintenance** : Activez ou désactivez le rapport d'erreurs.
* **Enregistreur de rapports de debug** : Utilisez l'enregistreur pour aider au dépannage.
