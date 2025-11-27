# compose
My docker compose repository

## Typical Compose
```
# Typical information line about the docker
services:
  portainer:
    image: portainer/portainer-ce:2.20.2
    container_name: portainer
    restart: always
    ports:
      - "9443:9443"
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=America/Chicago
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock
      - portainer:/data

volumes:
  portainer:
```
