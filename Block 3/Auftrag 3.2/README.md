# Auftrag 3.2: Webserver mit Docker

## Befehle

### Docker Image bauen

```Docker
docker build -t ghcr.io/marzonev/htmlapp
```
### Docker Container starten

```Docker
docker run -p 8080:80 -d --name ayri ghcr.io/marzonev/htmlapp
```
