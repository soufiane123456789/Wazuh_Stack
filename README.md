Structure du Dépôt
Le dépôt est organisé de manière claire pour faciliter la navigation :
-----

# DevOps and Cybersecurity: Building a Scalable Mini SOC


Ce dépôt contient la solution complète pour un projet de SOC Architect / DevOps Engineer.

## Aperçu du Projet

Ce projet est la concrétisation d'un **Mini SOC** automatisé et conteneurisé. Il se divise en deux parties principales :

1.  **Déploiement automatisé :** Mise en place d'un pipeline **CI/CD avec GitHub Actions** pour déployer la stack **Wazuh** (Manager, Indexer, Dashboard) sur un cluster **Docker Swarm**.
2.  **Règle de détection de menaces :** Création d'une règle **Wazuh personnalisée** pour identifier et alerter sur les tentatives de connexion SSH suspectes.

## Architecture & Déploiement

L'architecture est conçue pour être robuste et scalable, en s'appuyant sur l'orchestration de conteneurs de **Docker Swarm**. Le pipeline CI/CD assure que le déploiement est automatisé, reproductible et sécurisé grâce à des outils comme **Trivy** pour le scan des images.

Les diagrammes d'architecture, qui illustrent l'ensemble du flux de déploiement et la structure du cluster, sont disponibles dans le dossier `Architecture/`.

## Structure du Dépôt

Le dépôt est organisé de manière claire pour faciliter la navigation :


```
wazuh_Stack/
├── .github/workflows/       # Fichiers de configuration du pipeline CI/CD (GitHub Actions).
├── Architecture/            # Diagrammes d'architecture et aperçus du design.
├── Images/                  # Captures d'écran du pipeline, des alertes Wazuh et des dashboards personnalisés.
├── Trivy-Reports/           # Rapports de scan de vulnérabilités Trivy.
├── config/                  # Fichiers de configuration pour les services Wazuh, Nginx et les règles.
│   └── wazuh_rules/             # Décodeurs et règles de détection Wazuh personnalisés.
├── README.md                # Ce fichier.
├── Report.pdf               # Le rapport détaillé du projet.
├── generate-indexer-certs.yml # Script pour la génération des certificats d'indexeur.
└── stack.yml                # Fichier de déploiement Docker Swarm.
```

