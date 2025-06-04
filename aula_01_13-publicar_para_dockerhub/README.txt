1) Logar no https://hub.docker.com
2) Criar um token:
- Ir em user -> account settings
- Clicar em Personal access token
- Clicar em generate new token
- Siga as instruções para logar o docker cli na conta do docker hub
3) Troque o nome da imagem para adicionar o usuario do docker hub, caso não esteja já assim.
    Ex: docker tag minha-imagem-docker antoineem/minha-imagem-docker
4) Publique a imagem renomeada para o docker hub (se não tiver o formato user/tag, não funciona a publicação)
    Ex: docker push antoineem/minha-imagem-docker
    OBS: A imagem pode ser publicada também com outra tag
    Ex: docker build -t antoineem/minha-imagem-docker:v1 
        docker push antoineem/minha-imagem-docker:v1