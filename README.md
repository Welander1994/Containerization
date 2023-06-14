# Containerization

## Dokumentation til hvordan man bygger docker images og starter docker swarm

### Byg docker images til frontend og backend
 
1. Skift til backend-mappen ved at køre følgende kommando:
```
cd backend
```
2. Byg docker image til backend med følgende kommando:
```
docker build -t backend-image .
```
3. Skift til frontend-mappen ved at køre følgende kommando:
```
cd ../frontend
```
4. Byg docker image til frontend med følgende kommando:
```
docker build -t frontend-image .
```
<br>

## Opsæt docker swarm

1. Initialisér docker swarm på din pc ved at køre følgende kommando:
```
docker swarm init
```
2. Deploy stacken ved hjælp af docker-compose.yml-filen.
```
docker stack deploy -c docker-compose.yml simpleApp
```
3. Kontroller, om stacken kører korrekt ved at køre følgende kommando:
```
docker service ls
```
4. Stop stacken ved at køre følgende kommando:
```
docker stack rm simpleApp
```