# Traefik dockerized

---

#### The repository is intended to create a web server for not dockerized apps running on a server
#### Traefik will request, store, and renew the SSL certificate directly from *Let's Encrypt*

---

## Before move forward
+ Make sure you have *Docker Engine* installed and running
+ The service will use the host's network, make sure you don't have additional services that could cause conflicts

## How to...
1. Clone the repository in your server.
2. Replace the  required values in the `/compose/traefik.yml` file 
   2. The values to replace will be between double curly braces `{{value-to-replace}}`, you should ride off the curly braces 

Eg. From:
``` text
rule: 'Host(`{{domain}}`)'`
```

To
``` text
rule: 'Host(`api.domain.com`)'`
```

## Commands:
Run the service in detached mode
``` shell
docker-compose --build -d
```

Check the logs
```shell
docker-compose logs
```