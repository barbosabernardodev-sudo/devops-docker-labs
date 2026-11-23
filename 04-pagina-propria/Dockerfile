FROM ubuntu
LABEL maintainer="barbosabernardodev@gmail.com"
RUN apt-get update && apt-get install nginx curl -y && rm -rf /var/lib/apt/lists/*
COPY index.html /var/www/html 
EXPOSE 80
ENTRYPOINT ["nginx"]
CMD ["-g", "daemon off;"]
HEALTHCHECK --timeout=2s CMD curl localhost || exit 1
