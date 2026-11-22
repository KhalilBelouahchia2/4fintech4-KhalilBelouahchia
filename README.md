# Projet DevOps CI/CD — Gestion des Projets (4fintech4-KhalilBelouahchia)

Pipeline CI/CD complet et conteneurisé pour une application backend **Spring Boot** avec analyse statique de code et supervision en temps réel.

## Architecture & Outils
- **Gestion de version** : Git & GitHub
- **Intégration & Déploiement Continus (CI/CD)** : Jenkins (`Jenkinsfile`)
- **Qualité du code** : SonarQube (Quality Gate)
- **Conteneurisation & Orchestration** : Docker & Docker Compose (`Dockerfile`, `docker-compose.yml`)
- **Base de données** : MySQL 8.0 (`test_db`)
- **Supervision & Monitoring** : Spring Boot Actuator, Prometheus & Grafana

## Ports des services
| Service | Port | URL locale |
| :--- | :---: | :--- |
| **Application Backend (Spring Boot)** | `8085` | `http://10.0.2.15:8085` |
| **Jenkins** | `8080` | `http://10.0.2.15:8080` |
| **SonarQube** | `9000` | `http://10.0.2.15:9000` |
| **Prometheus** | `9090` | `http://10.0.2.15:9090` |
| **Grafana** | `3000` | `http://10.0.2.15:3000` |

## Lancement manuel via Docker Compose
docker-compose up -d --build
