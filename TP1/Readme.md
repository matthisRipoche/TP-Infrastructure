# TP1 : Microservice Flask Dockerisé

Ce projet est un microservice simple construit avec le framework **Flask** et configuré pour être exécuté dans un conteneur **Docker**.

## Structure du Projet

- `app.py` : Le point d'entrée de l'application Flask. Il expose une route unique (`/`) qui renvoie un message JSON : `{"message": "Hello from Dockerized Microservice!"}`.
- `Dockerfile` : Instructions pour construire l'image Docker de l'application. Il utilise Python 3.9, installe les dépendances et lance le serveur.
- `requirements.txt` : Liste des dépendances Python nécessaires (ici, uniquement `flask`).

## Comment l'utiliser

### Avec Docker
1. **Construire l'image** :
   ```bash
   docker build -t flask-microservice .
   ```
2. **Lancer le conteneur** :
   ```bash
   docker run -p 5000:5000 flask-microservice
   ```

L'application sera alors accessible sur `http://localhost:5000`.
