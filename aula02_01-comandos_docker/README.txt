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