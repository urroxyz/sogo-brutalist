# sogo-brutalist
Brutalist theme for SOGo webmail client used in Mailcow: Dockerized

## Installation
1. Download theme to `/opt/mailcow-dockerized/data/conf/sogo/`:
``` bash
cd /opt/mailcow-dockerized/data/conf/sogo/
wget https://raw.githubusercontent.com/NlightN22/sogo-dark-red/main/custom-theme.css
```

2. Create `/opt/mailcow-dockerized/docker-compose.override.yml`:
```bash
sudo nano /opt/mailcow-dockerized/docker-compose.override.yml
```

```yml
version: '2.1'

services:
  sogo-mailcow:
    volumes:
      - ./data/conf/sogo/custom-theme.css:/usr/lib/GNUstep/SOGo/WebServerResources/css/theme-default.css:z
```

3. Refresh:
```bash
cd /opt/mailcow-dockerized/ && sudo docker compose up -d
```
Restart your browser and clear the cache.
