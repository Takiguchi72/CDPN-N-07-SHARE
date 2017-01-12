# Docker
## Pré requis
- Docker engine + compose (inclus dans le package de base)
- Mettre les sources dans les dossiers adéquats
- Générer le .war dans crowdfunding-api/out

## Lancer l'api (et toutes les composantes liées)
- `docker-compose up api` pour builder les images et lancer les containers dans la foulée
- `docker-compose up -d api` pour "masquer" les logs
- go [http://localhost:9990/] pour l'interface admin ou [http://localhost:8080/crowdfunding-api/...] pour vos WS
- `docker restart <CONTAINER_ID>` pour relancer le container en prenant en compte le nouveau .war

## Lancer le frontal
- `docker-compose up -d http`

## Configs
utilisateur wildfly: `admin`, mdp: `pass`

## Documentation
- Docker engine: [https://docs.docker.com/engine/reference/commandline/]
- Dockerfiles: [https://docs.docker.com/engine/reference/builder/]
- Compose files: [https://docs.docker.com/compose/compose-file/]