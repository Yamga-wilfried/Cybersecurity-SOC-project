# 🛡️ Mise en place d’un SOC Open Source complet et fonctionnel

## 📌 Introduction
Ce projet vise à mettre en place un **SOC (Security Operations Center)** à l'aide d'outils **open source** tels que **Wazuh (SIEM), Shuffle (SOAR)**, **Suricata (IDS/IPS sur Pfsense)** et **Monitoring(kibana)**. L’objectif est de **centraliser les logs, détecter les menaces, automatiser les réponses aux incidents et améliorer la gestion de la cybersécurité**.

## 🚀 Objectifs du Projet
- **Déploiement d’un SOC complet et fonctionnel** avec des outils open source.
- **Détection avancée des menaces** en centralisant les logs et en corrélant les événements.
- **Automatisation des réponses aux incidents** grâce à SOAR.
- **Amélioration de la sécurité périmétrique** via un firewall avec IDS/IPS.

## 🏗️ Infrastructure Utilisée
### 🔹 Environnement de Virtualisation : **Proxmox**
### 🔹 Composants du SOC :
- **Wazuh (SIEM)** – Collecte et analyse des logs
- **Shuffle (SOAR)** – Automatisation des incidents
- **Pfsense + Suricata (Firewall/IPS)** – Protection du réseau
- **Active Directory (AD)** – Logs d’authentification
- **Kibana** - Monitoring(intégré à wazuh)
- **Windows & Linux (Endpoints)** – Journaux d’audit de sécurité

## 📊 Architecture Technique
### 📌 **Schéma du SOC**

![Capture d'écran 2025-03-31 195232](https://github.com/user-attachments/assets/134ba8d5-f7e8-4f39-b7ab-fd41d0f0551d)


- **Les logs sont collectés depuis AD, Pfsense, Windows, Linux**
![Capture d'écran 2025-03-31 195010](https://github.com/user-attachments/assets/226cdd7c-bea3-4ade-b90c-8bab664b3c3c)

![Capture d'écran 2025-03-31 195043](https://github.com/user-attachments/assets/3baab0ee-de2f-4480-83dd-4b2d7aab0bf5)

  
- **Wazuh centralise,analyse et corrèle les logs**
- **Shuffle orchestre et automatise la réponse aux incidents**
- **Suricata(IPS/IDS) détecte et bloque les intrusions sur Pfsense**
- **Kibana permet la visualisation et le monitoring des alertes**

## 🛠️ Implémentation
### 🔹 **Principales Étapes**
1. 📌 **Définition du périmètre et choix des outils**
2. 📌 **Installation des serveurs (Proxmox, Wazuh, Shuffle, Pfsense, Suricata, AD)**
3. **Installation des endpoints (WIN10, 11, Ubuntu)**
4. 📌 **Configuration des logs et agents Wazuh, c'est à dire intégration des outils dans wazuh**
5. 📌 **Définition des règles de détection(correlation des logs)**
6. 📌 **Création de playbooks pour automatiser la gestion des incidents**
7. 📌 **Génération de logs et simulations d’attaques à partir des différentes sources**
8. 📌 **Optimisation et documentation du SOC(plan de rémediation et rapport d'investigation)**

## 📈 Résultats et Bénéfices
✔ **Détection des menaces améliorée** grâce aux scénarios MITRE ATT&CK.
✔ **Réduction du temps de réponse aux incidents** avec SOAR.
✔ **Visibilité centralisée** grâce à Kibana et Wazuh.
✔ **Infrastructure modulaire et évolutive** (peut être améliorée avec d’autres outils).



## 🔗 Liens Utiles
- 📖 [Documentation Wazuh](https://documentation.wazuh.com/)
- 📖 [Documentation Shuffle](https://shuffler.io/docs)
- 📖 [Documentation Suricata](https://suricata.io/documentation/)



📌 **Auteur :** *Loïc Wilfried YAMGA*  
📌 **Contact :** *www.linkedin.com/in/loïc-yamga* OR wilfriedyamga@gmail.com
