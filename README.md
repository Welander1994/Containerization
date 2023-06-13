# Containerization

## Dokumentation til hvordan man bygger docker images og start docker swarm

### Byg Docker-images til frontend og backend
 
1. Skift til backend-mappen ved at køre følgende kommando:
```
cd backend
```
2. Byg Docker-image til backend med følgende kommando:
```
docker build -t backend-image .
```
3. Skift til frontend-mappen ved at køre følgende kommando:
```
cd ../frontend
```
4. Byg Docker-image til frontend med følgende kommando:
```
docker build -t frontend-image .
```
<br>

## Opsæt Docker Swarm

1. Initialisér Docker Swarm på din pc ved at køre følgende kommando:
```
docker swarm init
```
2. Deploy stacken ved hjælp af docker-compose.yml-filen. Sørg for, at du har en passende docker-compose.yml-fil klar i dit repository.
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