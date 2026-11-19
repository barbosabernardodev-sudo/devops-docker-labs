OBJETIVO
Praticar o ciclo de vida de um container nginx:criar, iniciar, ver logs, entrar e remover


COMANDOS USADOS
docker container run -d -p 8080:80 -name meu-nginx nginx
docker container ls -a
docker container stop meu-nginx
docker container start meu-nginx
docker contaier logs meu-nginx
docker container exec -it meu-nginx bash
docker container rm -f meu-nginx

** O que aprendi
- -d roda em segundo plano e -p publica a porta
- stop desliga e start liga de novo, pause congela e unpause desliga
- logs mostra o que aconteceu dentro do container
- exec entrar num container que já está rodando
- Exited (0)- encerrou normal
