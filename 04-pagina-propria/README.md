##LAB 04 - PÁGINA PRÓPIA E CONTAINERS TEMPORÁRIOS

##OBJETIVO 
criar uma imagem nginx com minha própia página (COPY) e entender que mudanças feitas dentro do container com exec são temporárias.

##COMANDOS USADOS 
-docker build -t moura-nginx:1.0
-docker container run -d -p 8082:80 --name moura-site moura-nginx:1.0
-docker container exec -it moura-site bash
-echo <h1>"Mudei pelo exec"</h1> > var/www/html/index.html
-docker container rm -f moura-site

##O QUE APRENDI
-COPY leva leva arquivos do meu computador pra dentro da imagem no build
-Mudanças feitas no exec ficam só na camada de escrita do container e somem quando ele é apagado
-Pra mudar de forma permanente: alterar o Dockerfile/arquivos e fazer uma nova build






