- Pesquisar imagens no docker hub
    docker search <text>

- Criar um container com nome especifico:
    docker run --name teste ubuntu

- Excluir um container pelo nome:
    docker rm teste

- Rodar um container e depois da execução, exclui-lo automaticamente:
    docker run --rm openjdk:17-alpine

- Criar um container a partir de uma imagem sem executar:
    docker create openjdk:21

- Executar um container já criado:
    docker start 1234

- Parar a execução de um container:
    docker stop 1234

- Renomear um container:
    docker rename 1234 novo-nome

- Remover todos os containers parados:
    docker rm $(docker ps -qa) -f

- Remover todas as imagens:
    docker rmi $(docker images -qa) -f

- Rodar um container em modo detached:
    docker run -d --name proxy-nginx nginx

- Acessar o log de um container:
    docker logs -f proxy-nginx

- Rodar comandos dentro de um container:
    docker exec proxy-nginx ls
    docker exec wildfly ps -ef
    docker exec wildfly jstack -l 1 // dump de threads
    docker exec wildfly jmap -dump:live,format=b,file=headdump.hprof 1 // dump de memoria

- Copiar arquivos do container para o host ou vice versa:
    docker cp wildfly:/home/file.txt .       // do container para o host
    docker cp ~/file.txt wildfly:./file.txt  // do host para o container

