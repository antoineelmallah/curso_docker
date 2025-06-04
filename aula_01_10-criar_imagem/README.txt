Criar imagem docker

1) Criar um arquivo Dockerfile
2) Adicionar o comando obrigatório FROM que especifica a imagem base. Escolher imagens base pequenas
3) Adicionar o comando opcional RUN para executar comandos do shell no container. Executado em tempo de build.
4) Adicionar o comando opcional CMD. Executado em tempo de execução (Quando o container for rodado).

Comandos:
1) docker images -> lista todas as imagens docker da maquina
2) docker build -t <tag> <caminho relativo para o Dockerfile>
    Ex: docker build -t minha-imagem-docker .
    OBS: Caso o arquivo descritor da imagem tiver um nome diferente de Dockerfile, deve ser passado
    o parâmetro -f seguido do nome do arquivo, no momento do build da imagem.
3) para rodar a imagem criada no exemplo acima:
docker run minha-imagem-docker:latest
ou simplesmente:
docker run minha-imagem-docker
4) docker rmi <tag ou id> -> para excluir uma imagem
    Ex:  docker rmi minha-imagem-docker
    Ex2: docker rmi minha-imagem-docker:latest
    Ex3: docker rmi 538