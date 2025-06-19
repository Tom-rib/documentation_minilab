# MINILAB

Déploiement complet d'une infrastructure réseau pour une association : VPN, LDAP, NFS, DNS/DHCP en haute disponibilité, clients légers avec Debian MATE, supervision, sécurité avancée et interface web d'administration.

## Sommaire

1. [🔍 Introduction](#1-introduction)  
2. [🌐 Architecture du réseau](#2-architecture-du-réseau)  
3. [🛠️ Configuration des serveurs](#3-configuration-des-serveurs)  
   - [Serveur principal](#31-serveur-principal)  
   - [Serveurs DHCP/DNS/LDAP](#32-serveurs-dhcpdnssldap)  
   - [Serveur NFS](#33-serveur-nfs)  
4. [💻 Configuration des clients](#4-configuration-des-clients)  
5. [🔐 Sécurisation de l'infrastructure](#5-sécurisation-de-linfrastructure)  
6. [🖥 Interface de gestion](#6-interface-de-gestion)  
7. [✅ Tests et validation](#7-tests-et-validation)  
8. [📚 Documentation utilisateur](#8-documentation-utilisateur)

---

## 1. Introduction

- Objectif : mettre en place une infrastructure réseau complète, sécurisée et simple à maintenir pour une association à but pédagogique.
- [Détails du contexte et des besoins](docs/1_introduction.md)

## 2. Architecture du réseau

- Schéma global et composants (DHCP, DNS, NFS, VPN, LDAP).
- Plan IP et nommage.
- [Voir la topologie et l’architecture détaillée](docs/2_architecture.md)

## 3. Configuration des serveurs

### 3.1 Serveur principal
- Installation, interfaces WAN/LAN, pare-feu, VPN (OpenVPN).
- [Voir les étapes](docs/3.1_serveur_principal.md)

### 3.2 Serveurs DHCP/DNS/LDAP
- Mise en place des serveurs DHCP en failover.
- Configuration DNS maître/esclave.
- Installation LDAP sécurisé.
- [Voir la configuration](docs/3.2_dhcp_dns_ldap.md)

### 3.3 Serveur NFS
- RAID 5 logiciel, installation et export de `/home`.
- [Voir la configuration du NFS](docs/3.3_serveur_nfs.md)

## 4. Configuration des clients

- Installation de Debian 12 + MATE.
- Authentification LDAP via PAM.
- Montage NFS automatique.
- [Voir les étapes clients](docs/4_clients.md)

## 5. Sécurisation de l'infrastructure

### 5.1 Sécurité réseau
- Pare-feu, accès VPN uniquement, LDAP sécurisé (StartTLS).
### 5.2 Authentification
- MFA, politique de mot de passe, gestion des comptes.
### 5.3 Maintenance et supervision
- Scripts d’update, sauvegarde, monitoring (ex. Netdata, Zabbix).
- [Voir sécurité et supervision](docs/5_securisation.md)

## 6. Interface de gestion

- UI Web pour gérer : NFS, LDAP, DNS/DHCP, supervision.
- Basé sur des outils comme Cockpit, phpLDAPadmin, Webmin...
- [Voir le détail](docs/6_interface_gestion.md)

## 7. Tests et validation

- Tests des profils itinérants, failover DHCP/DNS/LDAP.
- Vérification des accès VPN.
- [Voir le plan de test](docs/7_tests.md)

## 8. Documentation utilisateur

- Guide formateur (création utilisateur, gestion de session).
- Guide administrateur (maintenance, dépannage).
- [Voir la documentation utilisateur](docs/8_docs_utilisateur.md)

---
