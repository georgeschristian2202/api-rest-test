# API REST Test

Une API REST simple construite avec Express.js qui renvoie en écho les requêtes reçues.

## Description

Cette API permet de tester des requêtes HTTP en renvoyant les détails de chaque requête (méthode, headers, body, etc.).

## Fonctionnalités

- **GET /health** - Endpoint de santé pour vérifier que l'API fonctionne
- **ALL /echo** - Renvoie les détails de la requête (méthode, path, query, headers, body)
- Support de JSON, URL-encoded et texte brut

## Installation

```bash
npm install
```

## Utilisation

### Démarrage local

```bash
npm start
```

L'API sera accessible sur `http://localhost:3000`

### Avec Docker

```bash
docker-compose up
```

## Exemples de requêtes

```bash
# Health check
curl http://localhost:3000/health

# Echo GET
curl http://localhost:3000/echo?test=value

# Echo POST avec JSON
curl -X POST http://localhost:3000/echo \
  -H "Content-Type: application/json" \
  -d '{"message": "Hello World"}'
```

## Technologies

- Node.js
- Express.js
- Docker
