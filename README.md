<p align="center">
  <img src="https://files.catbox.moe/zcg6kh.jpg" alt="SADNESS-MD - Bot WhatsApp" width="100%" style="border-radius: 12px; border: 2px solid #e0e0e0;">
</p>

<h1 align="center">
  <span style="font-family: Georgia, 'Times New Roman', serif; font-style: italic; color: #2c3e50;">SADNESS-MD</span>
</h1>
<p align="center" style="font-family: Georgia, 'Times New Roman', serif; font-style: italic; color: #7f8c8d; font-size: 1.2rem;">
  Une solution robuste et modulaire pour l'automatisation WhatsApp
</p>

<p align="center">
  <a href="https://nodejs.org" target="_blank">
    <img src="https://img.shields.io/badge/Node.js-18.x%2B-339933?style=flat-square&logo=node.js&logoColor=white" alt="Node.js">
  </a>
  <a href="https://github.com/adiwajshing/Baileys" target="_blank">
    <img src="https://img.shields.io/badge/Baileys_MD-Latest-FF6B6B?style=flat-square&logo=github&logoColor=white" alt="Baileys MD">
  </a>
  <a href="LICENSE" target="_blank">
    <img src="https://img.shields.io/badge/License-MIT-3D7BBA?style=flat-square&logo=opensourceinitiative&logoColor=white" alt="License">
  </a>
  <a href="https://github.com/KleinDev91/SADNESS-MD/issues" target="_blank">
    <img src="https://img.shields.io/github/issues/KleinDev91/SADNESS-MD?style=flat-square&logo=github&color=2E86C1" alt="Issues">
  </a>
</p>

<p align="center">
  <a href="#fonctionnalités">Fonctionnalités</a> •
  <a href="#installation">Installation</a> •
  <a href="#configuration">Configuration</a> •
  <a href="#documentation">Documentation</a> •
  <a href="#contribuer">Contribuer</a>
</p>

---

## 📋 Présentation

**SADNESS-MD** est un framework pour bot WhatsApp, construit sur **Baileys**, conçu pour être stable, modulaire et facile à maintenir. Il est destiné aux développeurs souhaitant créer des systèmes d'automatisation, d'assistance ou d'interaction via WhatsApp, avec une architecture claire et extensible.

> **Note :** Ce projet est à but éducatif et technique. L'utilisateur est seul responsable de son utilisation et doit se conformer aux Conditions d'Utilisation de WhatsApp.

---

## ✨ Fonctionnalités

**Fonctions principales :**
- 🧩 **Architecture Modulaire** : Commandes et fonctionnalités séparées en modules.
- 🔌 **Support Multi-appareils (MD)** : Utilisation de la connexion multi-appareils officielle.
- 📦 **Gestionnaire de plugins** : Ajout ou retrait de fonctions sans modifier le cœur du projet.
- 🛡️ **Système de sécurité basique** : Filtrage de requêtes et gestion des permissions.
- 💾 **Support de bases de données** : Exemples fournis pour MongoDB et systèmes basés sur JSON.

**Fonctions techniques :**
- ✅ Connexion par QR Code ou Pair Code.
- 🖥️ Interface de monitoring Web optionnelle (via `dashboard.js`).
- 🔄 Gestion propre des erreurs et reconnections.
- 📝 Logging structuré pour le débogage.

---

## 🚀 Installation et Démarrage

### Prérequis
- [Node.js](https://nodejs.org/) (version 18 ou supérieure)
- [Git](https://git-scm.com/)
- Un compte WhatsApp
- Un terminal (Bash, PowerShell, etc.)

### Étapes d'installation

```bash
# 1. Clonez le dépôt
git clone https://github.com/KleinDev91/SADNESS-MD.git

# 2. Accédez au dossier du projet
cd SADNESS-MD

# 3. Installez les dépendances
npm install

# 4. Configurez votre environnement
# Copiez le fichier d'exemple de configuration
cp config.example.json config.json

# 5. Éditez le fichier config.json avec vos préférences
# (Voir section Configuration ci-dessous)

# 6. Lancez le bot
npm start
# ou
node index.js
