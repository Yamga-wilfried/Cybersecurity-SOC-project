# 🛡️ Mise en place d’un SOC Open Source complet et fonctionnel

## 📌 Introduction
Ce projet vise à mettre en place un **SOC (Security Operations Center)** à l'aide d'outils **open source** tels que **Wazuh (SIEM), Shuffle (SOAR)**, **Suricata (IDS/IPS sur Pfsense)**, **Monitoring(kibana),Alerting et suivis(Grafana)**. L’objectif est de **centraliser les logs, détecter les menaces, automatiser les réponses aux incidents et améliorer la gestion de la cybersécurité**.

## 🚀 Objectifs du Projet
- **Déploiement d’un SOC complet et fonctionnel** avec des outils open source.
- **Détection avancée des menaces** en centralisant les logs et en corrélant les événements.
- **Automatisation des réponses aux incidents** grâce à SOAR.
- **Amélioration de la sécurité périmétrique** via un firewall avec IDS/IPS.
- **Grafana** alerting et suivis d'incidents.

## 🏗️ Infrastructure Utilisée
### 🔹 Environnement de Virtualisation : **Proxmox**
### 🔹 Composants du SOC :
- **Wazuh (SIEM)** – Collecte et analyse des logs
- **Shuffle (SOAR)** – Automatisation des incidents
- **Pfsense + Suricata (Firewall/IPS)** – Protection du réseau
- **Active Directory (AD)** – Logs d’authentification
- **Kibana** - Monitoring
- **Windows & Linux (Endpoints)** – Journaux d’audit de sécurité

## 📊 Architecture Technique
### 📌 **Schéma du SOC**

![Capture d'écran 2025-03-31 195232](https://github.com/user-attachments/assets/134ba8d5-f7e8-4f39-b7ab-fd41d0f0551d)


- **Les logs sont collectés depuis AD, Pfsense, Windows, Linux**
![Capture d'écran 2025-03-31 195010](https://github.com/user-attachments/assets/226cdd7c-bea3-4ade-b90c-8bab664b3c3c)

![Capture d'écran 2025-03-31 195043](https://github.com/user-attachments/assets/3baab0ee-de2f-4480-83dd-4b2d7aab0bf5)

  
- **Wazuh analyse et corrèle les logs**
- **Shuffle orchestre et automatise la réponse aux incidents**
- **Suricata(IPS/IDS) détecte et bloque les intrusions sur Pfsense**
- **Kibana permet la visualisation et le suivi des alertes**

## 🛠️ Implémentation
### 🔹 **Principales Étapes**
1. 📌 **Définition du périmètre et choix des outils**
2. 📌 **Installation des serveurs (Proxmox, Wazuh, Shuffle, Pfsense, Suricata, AD)**
3. **Installation des endpoints (WIN10, 11, Ubuntu)**
4. 📌 **Configuration des logs et agents Wazuh**
5. 📌 **Définition des scénarios d’attaques et règles de détection(correlation des logs)**
6. 📌 **Déploiement du SOAR pour automatiser la réponse aux incidents**
7. 📌 **Génération de logs et simulations d’attaques à partir des différentes sources**
8. 📌 **Optimisation et documentation du SOC(plan de rémediation et rapport d'investigation)**

### 🔹 **Difficultés rencontrées & Solutions**
❌ **Problème d’authentification sous Ubuntu avec AD** ➜ 🔍 Solution : Configuration de `realmd` et `sssd`.
❌ **Intégration de Pfsense avec Wazuh** ➜ 🔍 Solution : Configuration de l’exportation des logs via Syslog.

## 📈 Résultats et Bénéfices
✔ **Détection des menaces améliorée** grâce aux scénarios MITRE ATT&CK.
✔ **Réduction du temps de réponse aux incidents** avec SOAR.
✔ **Visibilité centralisée** grâce à Kibana et Wazuh.
✔ **Infrastructure modulaire et évolutive** (peut être améliorée avec d’autres outils).

## 🔮 Améliorations Futures
- 🔄 Intégration de **machine learning** pour l’analyse des logs (ex : Elastic ML).
- 🔧 Création de **nouveaux playbooks SOAR** pour automatiser plus de tâches.
- 🛠️ Optimisation des règles IDS/IPS pour une détection plus fine.

## 📸 Captures d’écran *(À ajouter progressivement)*
- **Schéma de l’architecture du SOC**
- **Dashboard Wazuh avec logs collectés**
- **Exemple d’alerte et corrélation dans Wazuh**
- **Exécution d’un playbook SOAR sur Shuffle**
- **Détection d’une menace avec Suricata**
- **Exemple de gestion d'incident de A à Z**

## 🔗 Liens Utiles
- 📖 [Documentation Wazuh](https://documentation.wazuh.com/)
- 📖 [Documentation Shuffle](https://shuffler.io/docs)
- 📖 [Documentation Suricata](https://suricata.io/documentation/)



📌 **Auteur :** *Loïc Wilfried YAMGA*  
📌 **Contact :** *www.linkedin.com/in/loïc-yamga* OR _loic-wilfried.yamga-ngeulieutou@efrei.net_
