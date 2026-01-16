```markdown
# 🤖 SADNESS-MD - WhatsApp Bot Next-Gen

> Un bot WhatsApp professionnel, stable et performant basé sur Node.js et Baileys

<p align="center">
  <img src="https://files.catbox.moe/zcg6kh.jpg" alt="SADNESS-MD" width="600" style="border-radius: 10px; border: 1px solid #ddd;">
</p>

## 📋 Table des matières
- [Présentation](#présentation)
- [Fonctionnalités](#fonctionnalités)
- [Prérequis](#prérequis)
- [Installation](#installation)
- [Configuration](#configuration)
- [Déploiement](#déploiement)
- [Utilisation](#utilisation)
- [Sécurité](#sécurité)
- [FAQ](#faq)
- [Contribuer](#contribuer)
- [License](#license)
- [Avertissement](#avertissement)

## 🎯 Présentation

**SADNESS-MD** est un bot WhatsApp développé avec **Node.js** et la bibliothèque **Baileys**. Conçu pour être stable, performant et facile à maintenir, il offre une solution robuste pour l'automatisation de tâches sur WhatsApp.

### Caractéristiques principales
- ✅ **Multi-plateforme** : Fonctionne sur Windows, Linux, macOS
- ✅ **Session persistante** : Reconnexion automatique
- ✅ **Modulaire** : Architecture extensible
- ✅ **Documentation complète** : Guides détaillés inclus
- ✅ **Communauté active** : Support et mises à jour régulières

## ✨ Fonctionnalités

### Fonctionnalités de base
- **Gestion des messages** : Envoi, réception, traitement
- **Gestion des groupes** : Administration, modération
- **Commandes personnalisables** : Système de commandes modulaire
- **Support multi-appareils** : Compatible avec le nouveau protocole WhatsApp

### Fonctionnalités avancées
- **Système de plugins** : Extensions personnalisables
- **Base de données** : Support MongoDB et SQLite
- **API REST** : Interface pour intégrations externes
- **Logging avancé** : Suivi détaillé des activités
- **Sauvegarde automatique** : Prévention de perte de données

## 📋 Prérequis

Avant de commencer, assurez-vous d'avoir :

- **Node.js** version 16 ou supérieure
- **npm** ou **yarn** pour la gestion des dépendances
- **Git** pour le contrôle de version
- **Un compte WhatsApp** actif
- **Accès terminal/commande** sur votre machine

## 🚀 Installation

### 1. Cloner le dépôt
```bash
git clone https://github.com/yourusername/sadness-md.git
cd sadness-md
```

2. Installer les dépendances

```bash
npm install
# ou
yarn install
```

3. Configuration initiale

```bash
cp config.example.json config.json
# Éditez config.json avec vos paramètres
```

⚙️ Configuration

Fichier de configuration principal (config.json)

```json
{
  "sessionName": "session",
  "ownerNumber": "1234567890@s.whatsapp.net",
  "ownerName": "VotreNom",
  "botName": "SADNESS-MD",
  
  "mongooseConnectionString": "mongodb://localhost:27017/sadness-md",
  
  "maxUploadSize": 100,
  "messageLimit": 100,
  
  "timezone": "Africa/Casablanca",
  "language": "fr",
  
  "autoRead": false,
  "alwaysOnline": true,
  
  "multiDevice": true,
  "pairingCode": false
}
```

Variables d'environnement (optionnel)

```bash
export SESSION_NAME="your_session"
export MONGODB_URI="your_mongodb_uri"
export PORT=3000
```

☁️ Déploiement

Option 1 : Déploiement sur VPS/Dédié

```bash
# 1. Mettre à jour le système
sudo apt update && sudo apt upgrade -y

# 2. Installer Node.js
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs

# 3. Installer PM2 pour la gestion des processus
npm install -g pm2

# 4. Démarrer le bot
pm2 start index.js --name "sadness-md"
pm2 save
pm2 startup
```

Option 2 : Déploiement avec Docker

```bash
# Construire l'image
docker build -t sadness-md .

# Lancer le conteneur
docker run -d \
  --name sadness-md \
  -p 3000:3000 \
  -v $(pwd)/session:/app/session \
  sadness-md
```

Option 3 : Plateformes cloud recommandées

· Heroku : Guide de déploiement
· Railway : Guide de déploiement
· Replit : Guide de déploiement

📱 Utilisation

Démarrer le bot

```bash
npm start
# ou
node index.js
```

Commandes de base

```
!help - Affiche l'aide
!ping - Test de réponse
!status - Statut du bot
!restart - Redémarre le bot
!backup - Sauvegarde des données
```

Structure des dossiers

```
sadness-md/
├── src/
│   ├── commands/     # Commandes du bot
│   ├── plugins/      # Plugins additionnels
│   ├── libs/         # Bibliothèques internes
│   └── database/     # Gestion de la base de données
├── session/          # Sessions WhatsApp
├── config.json       # Configuration
├── index.js          Point d'entrée
└── package.json      Dépendances
```

🔒 Sécurité

Bonnes pratiques recommandées

1. Ne jamais partager votre fichier de session
2. Utiliser des variables d'environnement pour les données sensibles
3. Mettre à jour régulièrement les dépendances
4. Restreindre les permissions sur les fichiers de configuration
5. Activer l'authentification pour l'API si exposée publiquement

Configuration de sécurité recommandée

```json
{
  "security": {
    "allowedNumbers": ["1234567890@s.whatsapp.net"],
    "blockedNumbers": [],
    "maxFileSize": 50,
    "antivirusScan": true,
    "rateLimit": {
      "windowMs": 60000,
      "max": 30
    }
  }
}
```

❓ FAQ

Questions fréquentes

Q : Le bot peut-il être banni par WhatsApp ?
R : Tout usage automatisé de WhatsApp viole leurs conditions d'utilisation. Utilisez à vos risques et avec modération.

Q : Comment résoudre les problèmes de connexion ?
R : Consultez le guide de dépannage

Q : Puis-je ajouter mes propres commandes ?
R : Oui, consultez le guide de développement

Q : Le bot supporte-t-il les groupes ?
R : Oui, avec des fonctionnalités de modération et d'administration.

🤝 Contribuer

Les contributions sont les bienvenues ! Veuillez suivre ces étapes :

1. Fork le projet
2. Créer une branche (git checkout -b feature/AmazingFeature)
3. Commit vos changements (git commit -m 'Add some AmazingFeature')
4. Push vers la branche (git push origin feature/AmazingFeature)
5. Ouvrir une Pull Request

Standards de code

· Utiliser ESLint avec la configuration fournie
· Écrire des tests pour les nouvelles fonctionnalités
· Documenter les nouvelles API et commandes
· Suivre la convention de commits conventionnels

📄 License

Ce projet est sous licence MIT. Voir le fichier LICENSE pour plus de détails.

⚠️ Avertissement

Ce projet n'est pas affilié, associé, autorisé, approuvé par WhatsApp ou toute de ses filiales. WhatsApp est une marque déposée de Meta Platforms, Inc.

Responsabilités

· Ce bot est fourni à des fins éducatives uniquement
· L'utilisateur est seul responsable de son utilisation
· Respectez les conditions d'utilisation de WhatsApp
· Ne pas utiliser pour le spam ou activités malveillantes

Limitations

· Pas de support pour les appels vocaux/vidéo
· Pas de garantie de stabilité à 100%
· Dépend de l'API WhatsApp Web qui peut changer sans préavis

📞 Support

Documentation

· Documentation complète
· Guide d'installation détaillé
· Liste des commandes

Communauté

· Groupe WhatsApp - Support communautaire
· GitHub Issues - Rapports de bugs
· Discussions GitHub - Questions générales

Contact développeur

· Email : dev@example.com
· Telegram : @yourusername
· Site web : https://yourwebsite.com

---

<div align="center">
  <p>
    <strong>Dernière mise à jour :</strong> Janvier 2024<br>
    <strong>Version :</strong> 2.0.0<br>
    <strong>Mainteneur :</strong> CRAZY KLEIN TECH
  </p>

  <p>
    <a href="https://github.com/yourusername/sadness-md/stargazers">
      <img src="https://img.shields.io/github/stars/yourusername/sadness-md" alt="Stars">
    </a>
    <a href="https://github.com/yourusername/sadness-md/network/members">
      <img src="https://img.shields.io/github/forks/yourusername/sadness-md" alt="Forks">
    </a>
    <a href="https://github.com/yourusername/sadness-md/issues">
      <img src="https://img.shields.io/github/issues/yourusername/sadness-md" alt="Issues">
    </a>
    <a href="https://github.com/yourusername/sadness-md/blob/master/LICENSE">
      <img src="https://img.shields.io/github/license/yourusername/sadness-md" alt="License">
    </a>
  </p>
</div>
```
