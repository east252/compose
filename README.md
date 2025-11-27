# compose
My docker compose repository

## Typical Compose
```
# Typical information line about the docker
services:
  my_application:
    image: my_application_author/my_application_name-my:version
    container_name: my_application
    restart: unless-stopped
    ports:
      - "1234:1234"
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=America/Chicago
    volumes:
      - volume1_0_name: /config
      - volume1_1_name: /data
      - volume1_2_name: /whateverelse

volumes:
  volume1_0_name:
  volume1_1_name:
  volume1_2_name:
```
