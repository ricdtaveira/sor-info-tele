
# Fazer Push de uma Imagem para o Docker Hub
Após o `commit` das alterações em uma imagem no repositório local é prudente fazer uma cópia dessa
imagem para um serviço na nuvem onde se preserva todo o trabalho na configuração dessa imagem. 
O Docker Hub permite a criação de repositórios públicos e/ou privados que hospedam imagens que poderão ser usadas posteriormente.  
Os passos apresentados a seguir definem um ciclo envolvendo as operações necessárias a obtenção de uma imagem som até o upload de uma versao modificada para o Docker Hub

## 1) Criar um repositório no Docker Hub 

A criação de uma no Docker Hub antecede a criação de um repositório para que se possa fazer o `push` de uma imagem alterada. Portanto, é necessário proceder da seguinte forma: 
1) Acessar o site do Docker Hub. [Docker Hub](https://hub.docker.com/)
2) Criar uma cona no Docker Hub. [Criar Conta](https://hub.docker.com/signup)
3) Criar um repositório no Docker Hub.
4) Fazer o `push` de imagens obedecendo a seguinte nomenclatura: <conta>/<repositorio>:tag    

## 2) Fazer um Pull de uma imagem hospedada no GitHub

Antes de fazer uma alteração na imagem é necessária baixá-la do Docker Hub.

```bash 
  $ docker search ubuntu
  $ docker pull ricdtaveira/ubuntu:latest
  $ docker images
```

## 3) Alterar a imagem no Repositório Local

Para alterar uma imagem  


## 4) Criar imagem com Tag compatível com o repositório no Docker Hub


  
## 5) Upload da Imagem local para o repositório no Docker Hub



Etapas da instalação:
1) Instalar o pacote  Docker a partir de um script de instalação baixado do site do Docker. Adiciona na maquina local um repositório Docker e inicia a instalação do Docker.
2) Inicializar a execução do Docker 
3) Verificar se o Docker está executando com o comando ps
4) Verificar os containers que estão executando localmente.


```bash 
  curl -sSL https://get.docker.com | sh 
  /etc/init.d/docker start
  ps -ef | grep docker
  docker ps
```

  
 