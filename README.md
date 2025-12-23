# compose
My docker compose repository

## Getting Started

### Setting up Environment Variables

This repository uses environment variables to avoid hard-coding secrets in the compose files. Before running the services:

1. Copy `.env.example` to `.env`:
   ```bash
   cp .env.example .env
   ```

2. Edit `.env` and fill in your secure passwords and secrets:
   - `SIYUAN_AUTH_CODE` - Authentication code for SiYuan editor
   - `POSTGRES_PASSWORD` - Password for PostgreSQL database

3. The `.env` file is git-ignored to prevent accidentally committing secrets.

## Port Tracker
2000 - Portainer  
2001 - NPM http  
2002 - NPM management  
2003 - NPM https  
2004 - Postgres DB  
2005 - SiYuan Markdown Editor  
2006 - Ubuntu  
2007 - n8n  
2008 - OpenWebUI  

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
