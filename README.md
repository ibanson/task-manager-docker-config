# 🐳 Activity Messenger – Docker Config

Configuration **Docker** pour le projet _Activity Messenger_.
Ce dépôt contient les fichiers nécessaires pour lancer l’environnement complet (API, Frontend, Base de données, Nginx, etc.) à l’aide de **Docker Compose**.

---

## Structure du dépôt

activity-messenger/
├─ docker-compose.yml                 # Orchestration principale (API, Frontend, DB, Nginx, Adminer)
│
├─ docker-config/                     # Configurations Docker partagées
│   ├─ api/
│   │   └─ Dockerfile                 # Image du backend (Laravel)
│   │
│   ├─ nginx/
│   │   ├─ Dockerfile                 # Image Nginx (reverse proxy)
│   │   └─ default.conf               # Configuration du serveur Nginx
│   │
│   └─ ssl/                           # (Optionnel) Certificats SSL de développement
│
├─ api/                               # Dépôt cloné depuis activity-messenger-demo-api
│   ├─ .env.example
│   └─ (Code source du backend Laravel)
│
├─ frontend/                          # Dépôt cloné depuis activity-messenger-demo-frontend
│   └─ (Code source Vue.js 2)
│
├─ pg-data/                           # Volume local persistant pour PostgreSQL (non versionné)
│
└─ .gitignore                         # Ignore volumes, certificats, builds, etc.