# privatebin
Manifests and Configuration for Privatebin - https://privatebin.info/

## How do I use this?

Clone the repo, touch the config files, and run `docker compose up -d`

```bash
# clone the repo
git clone https://github.com/wetfish/privatebin.git

# optional: for local development
# optional: enable port exposure from privatebin container
# optional: and disable traefik
$EDITOR docker-compose.yml

# change root and user pws for mariadb
cp mariadb.env.example mariadb.env
$EDITOR mariadb.env

# change letsencrypt email in static config
$EDITOR traefik/conf/static.yml

# and domain in dynamic config
$EDITOR traefik/conf/dynamic.yml

# edit privatebin config
cp privatebin/conf/conf.php.example privatebin/conf/conf.php
$EDITOR privatebin/conf/conf.php

# start the stack
docker compose up -d --force-recreate
```
