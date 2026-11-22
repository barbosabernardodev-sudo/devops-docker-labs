03 - Desafio: Dockerfile com debian e Healthcheck

OBJETIVO
criar uma imagem nginx a partir do Debian com tag fixa, ENTRYPOINT

DOCKERFILE
FROM debian:12
RUN apt-get update && apt-get install nginx curl -y &&  rm -rf /var/lib/apt/lists/*
EXPOSE 80
LABEL maintainer="bemourajf420@gmail.com"
ENTRYPOINT["nginx"]
CMD ["-g", "daemon off;"]
HEALTHCHECK --timeout=2s CMD curl localhost || exit 1
