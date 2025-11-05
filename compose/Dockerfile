FROM docker.io/traefik:v3.5
RUN mkdir -p /etc/traefik/acme \
  && touch /etc/traefik/acme/acme.json \
  && chmod 600 /etc/traefik/acme/acme.json
COPY ./compose/traefik.yml /etc/traefik/traefik.yml
