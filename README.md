# 🧪 MINILAB – Infrastructure Réseau Associative

Projet de déploiement d'une infrastructure réseau complète, sécurisée et maintenable pour une association : services centralisés (LDAP, NFS, DNS, DHCP), postes clients légers Debian, supervision, VPN, sécurité renforcée et interface de gestion web.

---

## 📑 Sommaire

1. [🔍 Introduction](#1-introduction)  
2. [🌐 Architecture du réseau](#2-architecture-du-réseau)  
3. [🛠️ Configuration des serveurs](#3-configuration-des-serveurs)  
4. [💻 Configuration des clients](#4-configuration-des-clients)  
5. [🔐 Sécurisation de l'infrastructure](#5-sécurisation-de-linfrastructure)  
6. [🖥 Interface de gestion](#6-interface-de-gestion)  
7. [✅ Tests et validation](#7-tests-et-validation)  
8. [📘 Documentation utilisateur](#8-documentation-utilisateur)  
9. [📎 Annexes](#9-annexes)  
10. [🚀 Évolutions futures](#10-évolutions-futures)

---

## 1. Introduction

- **1.1 Contexte et objectifs** : répondre aux besoins pédagogiques et administratifs de l'association.  
- **1.2 Besoins de l'association** : centralisation des comptes, mobilité des utilisateurs, sécurité des données.  
- **1.3 Vue d'ensemble** : aperçu des composants (VPN, LDAP, NFS, supervision, etc.).  

## 2. Architecture du réseau

- **2.1 Schéma global** : diagramme du réseau et des flux.  
- **2.2 Composants** : rôle de chaque serveur (VPN, NFS, LDAP, DNS, etc.).  
- **2.3 Plan IP/Nommage** : cohérence et simplicité d'administration.  

## 3. Configuration des serveurs

- **3.1 Serveur principal** : configuration réseau, VPN, pare-feu.  
- **3.2 DHCP/DNS/LDAP (master/slave)** : haute dispo, failover, synchronisation LDAP.  
- **3.3 Serveur NFS** : RAID5, partage /home pour roaming.  

## 4. Configuration des clients

- **4.1 Debian 12 + MATE** : installation minimale + bureau léger.  
- **4.2 Authentification LDAP** : PAM/SSSD.  
- **4.3 NFS automatique** : montage au login.  
- **4.4 UX personnalisée** : fond d’écran, raccourcis, scripts init.  

## 5. Sécurisation de l'infrastructure

- **5.1 Réseau** : pare-feu strict, accès distant uniquement via VPN.  
- **5.2 Authentification** : MFA, OTP, politique de mots de passe.  
- **5.3 Supervision et MAJ** : monitoring, scripts de backup automatiques.  

## 6. Interface de gestion

- **6.1 Outils retenus** : Cockpit, Webmin, phpLDAPadmin.  
- **6.2 Fonctionnalités** : gestion LDAP/NFS/DNS/DHCP + supervision.  

## 7. Tests et validation

- **7.1 Plan de tests** : roaming, défaillance serveur, continuité de service.  
- **7.2 VPN** : validation des accès distants sécurisés.  

## 8. Documentation utilisateur

- **8.1 Guide formateurs** : création de compte LDAP, accès aux fichiers.  
- **8.2 Guide admins** : dépannage rapide, restauration de données.  

## 9. Annexes

- **9.1 Exemples de conf** : DHCP, DNS, LDAP, PAM, systemd.  
- **9.2 Références** : liens vers tutoriels, outils utilisés.  
- **9.3 Glossaire** : définitions utiles.  

## 10. Évolutions futures (Bonus)

- **10.1 Impression centralisée** : mise en place de CUPS.  
- **10.2 Sauvegardes cloud** : Borg, Rsync, stockage distant.  
- **10.3 Réplication NFS** : solutions haute dispo ou synchronisation offsite.  

---


