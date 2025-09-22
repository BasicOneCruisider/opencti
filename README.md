# 🛡️ OpenCTI - Plateforme de Cyber Threat Intelligence

Bienvenue sur le dépôt **OpenCTI** !  
Ce projet propose une plateforme collaborative pour la gestion, l’analyse et le partage de la Cyber Threat Intelligence (CTI).

---

## 🚀 Objectif du projet

OpenCTI vise à centraliser et structurer les informations sur les menaces cyber, afin de faciliter leur exploitation par les équipes de sécurité, les analystes et les partenaires.

- **Collecte** : Intégration de multiples sources de données (connecteurs).
- **Analyse** : Visualisation et corrélation des menaces.
- **Partage** : Diffusion des indicateurs et rapports auprès des parties prenantes.

---

## 🏗️ Architecture

Le projet utilise **Docker Compose** pour orchestrer les différents services :

- **OpenCTI** : Plateforme principale (Node.js)
- **Elasticsearch** : Moteur de recherche et d’indexation
- **Redis** : Cache et gestion des files d’attente
- **MinIO** : Stockage d’objets compatible S3
- **RabbitMQ** : Message broker pour les connecteurs
- **Connecteurs** : Modules d’import/export et d’enrichissement (CrowdSec, STIX, CSV, TXT, etc.)

---

## 📦 Installation rapide

1. **Clonez le dépôt**

   ```bash
   git clone https://github.com/BasicOneCruisider/opencti.git
   cd opencti
   ```

2. **Configurez les variables d’environnement**  
   Modifiez le fichier `.env` pour adapter les mots de passe, tokens et clés API à votre environnement.

3. **Lancez la plateforme**

   ```bash
   docker compose up -d
   ```

4. **Accédez à l’interface**  
   Ouvrez [http://localhost:8080](http://localhost:8080) dans votre navigateur.

---

## 🔌 Connecteurs disponibles

- **CrowdSec** : Enrichissement des adresses IP avec la CTI CrowdSec
- **Export STIX/CSV/TXT** : Export des données dans différents formats
- **Import STIX/Document** : Import de fichiers structurés ou non
- **Worker** : Traitement asynchrone des tâches

---

---

## ⚙️ Configuration

- Les mots de passe et tokens sont à définir dans le fichier `.env`
- Les volumes Docker assurent la persistance des données
- Les ports exposés permettent l’accès aux interfaces web et API

---

## 📝 Contribution

Les contributions sont les bienvenues !  
N’hésitez pas à ouvrir une issue ou une pull request pour proposer des améliorations ou signaler des bugs.

---

## 📚 Documentation

- [Documentation officielle OpenCTI](https://www.opencti.io/docs)
- [Docker Compose](https://docs.docker.com/compose/)
- [CrowdSec CTI](https://www.crowdsec.net/)

---

## 💡 Bonnes pratiques

- Changez tous les mots de passe et tokens par défaut avant la mise en production
- Utilisez un réseau Docker dédié pour isoler les services
- Sauvegardez régulièrement vos volumes de données

---

## 🛠️ Licence

Ce projet est distribué sous licence MIT.

---

## 🤝 Remerciements

Merci à tous les contributeurs et à la communauté OpenCTI !  
Pour toute question, contactez-nous via GitHub.

---
